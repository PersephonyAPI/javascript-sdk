Calls
======

get(callId)
^^^^^^^^^^^

    Retrieve a single call from Persephony.

    :callId: {string} The :code:`callId` of the desired call.

    :returns: {Promise<object>} Returns a promise that resolves to the call matching the :code:`callId` provided.
    :throws: Will throw an error on a failed response.

update(callId, status)
^^^^^^^^^^^^^^^^^^^^^^^^

    Update the existing call associated with the :code:`callId`

    :callId: {string} The :code:`callId` of the desired call.
    :status: {string} The status to set the target call to. Can be either :ref:`Enums-callStatus-label`.CANCELED or :ref:`Enums-callStatus-label`.COMPLETED.

    :returns: {Promise<null>} Returns a promise that resolves to null on success
    :throws: Will throw an error on a failed response.

getList(filters)
^^^^^^^^^^^^^^^^^

    Retrieve a list of calls associated with the :code:`accountId`

    :[filters]: {object} Optional filters containing a number of possible ways to filter the calls returned by Persephony.

    :returns: {Promise<object>} Returns a promise that resolves to a list of call instances matching the filters if provided.
    :throws: Will throw an error on a failed response.

getNextPage(nextPageUri)
^^^^^^^^^^^^^^^^^^^^^^^^^

    Retrieve the next page of list results

    :nextPageUri: {string} The URL to the next page of results.

    :returns: {Promise<oobject>} Returns a promise that resolves to the next page of calls
    :throws: Will throw an error on a filed response.

create(to, from, options)
^^^^^^^^^^^^^^^^^^^^^^^^^^

    Create a new call through the Persephony API.

    :to: {string} The number to call out to (DNIS). This can be any valid phone number formatted in E.164 format in Persephony's service area.
    :from: {string} The number to call from (ANI). This must be a number purchased from Persephony or a verified phone number owned by the user.
    :options: {object} Additional properties to set the behavior of the call to be placed. Must include either :code:`callConnectUrl` or :code:`applicationId`.

    :returns: {Promise<object>} returns a promise that resolves to the newly placed call.
    :throws: Will throw an error on a failed response.
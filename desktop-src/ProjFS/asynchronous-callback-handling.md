---
title: Conclusão de retorno de chamada assíncrono
description: Descreve como o provedor pode atender a retornos de chamada de serviço de forma assíncrona.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/12/2018
ms.topic: article
ms.openlocfilehash: 8ec23f5ea6e8ec55be2eaa2811d9dee8b1870edc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105754304"
---
# <a name="asynchronous-callback-handling"></a>Manipulação de retorno de chamada assíncrono

Quando um cliente interage com os arquivos e diretórios abaixo da raiz de virtualização do provedor, essas interações normalmente resultam na invocação de retornos de chamada do provedor.  O ProjFS invoca os retornos de chamada do provedor enviando uma mensagem do modo kernel para a biblioteca de modo de usuário ProjFS, em que um thread de trabalho recebe a mensagem e chama o retorno de chamada apropriado.  Depois que o retorno de chamada for retornado, o thread de trabalho aguardará que outra mensagem chegue do modo kernel.  Se todos os threads de trabalho estiverem ocupados executando o código de retorno de chamada do provedor, qualquer e/s adicional do cliente que dispara um retorno de chamada até que um thread de trabalho fique disponível para receber a mensagem e invocar o retorno de chamada relevante.  Quando um provedor é iniciado, ele pode especificar o número de threads de trabalho que ele quer que ProjFS crie para os retornos de chamada de serviço por meio do parâmetro _Options_ de **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)**.  Um provedor pode melhorar a eficiência dos threads de trabalho de recebimento de mensagens ao atender a seus retornos de chamada de forma assíncrona.

> Se o provedor não especificar o parâmetro _Options_ para **PrjStartVirtualizing**, ou se ele especificar 0 para o membro ConcurrentThreadCount do parâmetro _Options_ , ProjFS usará o número de processadores lógicos no sistema para o valor de ConcurrentThreadCount.
>
> Se o provedor não especificar o parâmetro _Options_ para **PrjStartVirtualizing**, ou se ele especificar 0 para o membro PoolThreadCount do parâmetro _Options_ , ProjFS usará o dobro do valor de ConcurrentThreadCount para o valor de PoolThreadCount.

Um provedor fornece retornos de chamada de forma assíncrona, retornando HRESULT_FROM_WIN32 (ERROR_IO_PENDING) de seus retornos de chamada e depois concluindo-os usando **[PrjCompleteCommand](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjcompletecommand)**.  Um provedor que processa retornos de chamada assincronamente também deve dar suporte ao cancelamento de retorno de chamada implementando o **[PRJ_CANCEL_COMMAND_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb)** retorno de chamada.

Quando o ProjFS chama o retorno de chamada de um provedor, ele identifica a invocação específica do retorno de chamada usando o membro CommandId do parâmetro _callbackdata_ do retorno de chamada.  Se o provedor decidir processar esse retorno de chamada de forma assíncrona, ele deverá armazenar o valor do membro CommandId e retornar HRESULT_FROM_WIN32 (ERROR_IO_PENDING) do retorno de chamada.  Depois que o provedor terminar de processar o retorno de chamada, ele chamará **PrjCompleteCommand**, passando o identificador armazenado no parâmetro _commandId_ .  Isso informa ao ProjFS qual invocação de retorno de chamada foi concluída.

Um provedor que implementa o retorno de chamada **PRJ_CANCEL_COMMAND_CB** deve controlar quais retornos de chamada ainda não foram concluídos.  Se o provedor receber esse retorno de chamada, ele indica que a e/s que causou a chamada de um desses retornos de chamada foi cancelada explicitamente ou porque o thread em que ele foi emitido foi encerrado. O provedor deve cancelar o processamento da invocação de retorno de chamada identificada pela CommandId assim que possível.

> Embora ProjFS invocará **PRJ_CANCEL_COMMAND_CB** para um determinado CommandID somente depois que o retorno de chamada a ser cancelado for invocado, o cancelamento e a invocação original poderão ser executados simultaneamente em um provedor multi-threaded.  O provedor deve ser capaz de lidar normalmente com essa situação.

O exemplo a seguir é uma versão do exemplo fornecido para o tópico [enumerando arquivos e diretórios](enumerating-files-and-directories.md) , modificado para ilustrar o tratamento de retorno de chamada assíncrono.

```C++
typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

typedef struct MY_ENUM_ENTRY {
    MY_ENUM_ENTRY* Next;
    PWSTR Name;
    BOOLEAN IsDirectory;
    INT64 FileSize;
} MY_ENUM_ENTRY;

typedef struct MY_ENUM_SESSION {
    GUID EnumerationId;
    PWSTR SearchExpression;
    USHORT SearchExpressionMaxLen;
    BOOLEAN SearchExpressionCaptured;
    MY_ENUM_ENTRY* EnumHead;
    MY_ENUM_ENTRY* LastEnumEntry;
    BOOLEAN EnumCompleted;
} MY_ENUM_SESSION;

typedef struct MY_ENUM_PARAMS {
    GUID EnumerationId;
    PRJ_DIR_ENTRY_BUFFER_HANDLE DirEntryBufferHandle;
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT NamespaceVirtualizationContext;
    INT32 CommandId;
    PRJ_CALLBACK_DATA_FLAGS Flags;
    WCHAR SearchExpression[1];
} MY_ENUM_PARAMS;

// Prototype for the enumeration worker routine.  In this example this is a
// ThreadProc.  See https://msdn.microsoft.com/library/windows/desktop/ms686736.aspx
DWORD WINAPI MyGetEnumCallbackWorker(_In_ LPVOID parameter);

#define ROLLBACK_NONE           0
#define ROLLBACK_PARAM_ALLOC    1
#define ROLLBACK_TRACK_ENUM     2

HRESULT
MyGetEnumCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ const GUID* enumerationId,
    _In_opt_z_ PCWSTR searchExpression,
    _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
    )
{
    UINT rollback = ROLLBACK_NONE;

    // This example creates a thread to run the enumeration in.  The provider
    // can access callbackData only while the callback is running, so we copy
    // out the fields that the worker thread will need.
    MY_ENUM_PARAMS* enumParams = NULL;
    size_t bufSize = sizeof(MY_ENUM_PARAMS);

    // Allocate enough space for the parameter buffer and the search expression
    // string plus a terminating NULL character.
    if (searchExpression != NULL)
    {
        bufSize += (wcslen(searchExpression) + 1) * sizeof(WCHAR);
    }
    else
    {
        // We'll store "*" as the search expression in this case.
        bufSize += 2 * sizeof(WCHAR);
    }

    enumParams = (MY_ENUM_PARAMS*) calloc(1, bufSize);

    if (enumParams == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto RollbackOnError;
    }

    // enumParams allocated.
    rollback = ROLLBACK_PARAM_ALLOC;

    // Copy the search expression into our parameter buffer.
    if (searchExpression != NULL)
    {
        wcsncpy_s(enumParams->SearchExpression,
                  wcslen(searchExpression),
                  searchExpression,
                  wcslen(searchExpression));
    }
    else
    {
        wcsncpy_s(enumParams->SearchExpression, 1, "*", 1);
    }

    // Copy the other parameters into our parameter buffer.
    enumParams->EnumerationId = enumerationId;
    enumParams->DirEntryBufferHandle = dirEntryBufferHandle;
    enumParams->NamespaceVirtualizationContext = callbackData->NamespaceVirtualizationContext
    enumParams->CommandId = callbackData->CommandId;
    enumParams->Flags = callbackData->Flags;

    // MyTrackEnumForCancellation is a routine the provider might implement to
    // track active enumeration callbacks in case they are cancelled.  It stores
    // the CommandId for the callback in some structure.
    hr = MyTrackEnumForCancellation(callbackData->CommandId);

    if (FAILED(hr))
    {
        goto RollbackOnError;
    }

    // Enum callback tracked.
    rollback = ROLLBACK_TRACK_ENUM;

    // Create the worker thread.
    HANDLE workerThread = NULL;
    workerThread = CreateThread(NULL,
                                0,
                                MyGetEnumCallbackWorker,
                                enumParams,
                                0
                                NULL);

    // We'll treat failure to create the thread as a low-resources error.
    if (workerThread == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto RollbackOnError;
    }

    // Return pending to signal that we'll complete the enumeration later.
    return HRESULT_FROM_WIN32(ERROR_IO_PENDING);

RollbackOnError:

    // Clean up manually.  Note the fall-through structure of the switch, and that
    // we clean up in reverse order.
    switch(rollback)
    {
    case ROLLBACK_TRACK_ENUM:
        // MyUntrackEnumForCancellation removes the CommandId for the callback
        // from the structure that MyTrackEnumForCancellation put it in.
        MyUntrackEnumForCancellation(callbackData->CommandId);

    case ROLLBACK_PARAM_ALLOC:
        free(enumParams);

    default:
        break;
    }

    return hr;
}

DWORD
WINAPI
MyGetEnumCallbackWorker(
    _In_ LPVOID parameter
)
{
    HRESULT hr = S_OK;
    MY_ENUM_PARAMS* enumParams = (MY_ENUM_PARAMS*) parameter;

    // MyCheckEnumForCancellation is a routine the provider might implement to
    // check whether a pended enumeration callback has been cancelled.  Even
    // though the enumeration has been cancelled, ProjFS will still call the
    // provider's end-enumeration callback.  This allows general cleanup, such
    // as tearing down the enumeration session, to always happen in that callback.
    if (MyCheckEnumForCancellation(enumParams->CommandId))
    {
        // The operation has been cancelled.  Clean up and get out.
        free(enumParams);
        return 0;
    }

    // MyGetEnumSession is a routine the provider might implement to find
    // information about the enumeration session that it first stored
    // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
    //
    // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
    // already retrieved a list of the items in the backing store located at
    // callbackData->FilePathName, sorted them using PrjFileNameCompare()
    // to determine collation order, and stored the list in session->EnumHead.
    MY_ENUM_SESSION* session = NULL;
    session = MyGetEnumSession(enumParams->EnumerationId);

    if (session == NULL)
    {
        hr = HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        goto CompleteCallback;
    }

    if (!session->SearchExpressionCaptured ||
        (enumParams->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
    {
        if (wcsncpy_s(session->SearchExpression,
                      session->SearchExpressionMaxLen,
                      enumParams->SearchExpression,
                      wcslen(enumParams->SearchExpression)))
        {
            // Failed to copy the search expression; perhaps the provider
            // could try reallocating session->SearchExpression.
        }

        session->SearchExpressionCaptured = TRUE;
    }

    MY_ENUM_ENTRY* enumHead = NULL;

    // We have to start the enumeration from the beginning if we aren't
    // continuing an existing session or if the caller is requesting a restart.
    if (((session->LastEnumEntry == NULL) &&
         !session->EnumCompleted) ||
        (enumParams->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
    {
        // Ensure that if the caller is requesting a restart we reset our
        // bookmark of how far we got in the enumeration.
        session->LastEnumEntry = NULL;

        // In case we're restarting ensure we don't think we're done.
        session->EnumCompleted = FALSE;

        // We need to start considering items from the beginning of the list
        // retrieved from the backing store.
        enumHead = session->EnumHead;
    }
    else
    {
        // We are resuming an existing enumeration session.  Note that
        // session->LastEnumEntry may be NULL.  That is okay; it means
        // we got all the entries the last time this callback was invoked.
        // Returning S_OK without adding any new entries to the
        // enumParams->DirEntryBufferHandle buffer signals ProjFS that the
        // enumeration has returned everything it can.
        enumHead = session->LastEnumEntry;
    }

    if (enumHead == NULL)
    {
        // There are no items to return.  Remember that we've returned everything
        // we can.
        session->EnumCompleted = TRUE;
    }
    else
    {
        MY_ENUM_ENTRY* thisEntry = enumHead;
        while (thisEntry != NULL)
        {
            // We'll insert the entry into the return buffer if it matches
            // the search expression captured for this enumeration session.
            if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
            {
                PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                fileBasicInfo.FileSize = thisEntry->FileSize;

                // Format the entry for return to ProjFS.
                if (S_OK != PrjFillDirEntryBuffer(thisEntry->Name,
                                                  &fileBasicInfo,
                                                  enumParams->DirEntryBufferHandle))
                {
                    // We couldn't add this entry to the buffer; remember where we left
                    // off for the next time we're called for this enumeration session.
                    session->LastEnumEntry = thisEntry;
                    hr = S_OK;

                    goto CompleteCallback;
                }
            }

            thisEntry = thisEntry->Next;
        }

        // We reached the end of the list of entries; remember that we've returned
        // everything we can.
        session->EnumCompleted = TRUE;
    }

CompleteCallback:

    // Signal ProjFS that we've completed this callback.  Since this is an enumeration
    // we use the extendedParameters parameter to PrjCompleteCommand.
    PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS extendedParams = {};
    extendedParams.CommandType = PRJ_COMPLETE_COMMAND_TYPE_ENUMERATION;
    extendedParams.enumeration.DirEntryBufferHandle = enumParams->DirEntryBufferHandle;

    PrjCompleteCommand(enumParams->NamespaceVirtualizationContext,
                       enumParams->CommandId,
                       hr,
                       &extendedParams);

    MyUntrackEnumForCancellation(enumParams->CommandId);

    free(enumParams);

    // ThreadProc returns 0 on successful completion.
    return 0;
}
```

E aqui está um breve exemplo PRJ_CANCEL_COMMAND_CB que funciona com o código de exemplo anterior.

```C++
void
MyCancelCommandCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
)
{
    // MyMarkEnumForCancellation is a routine the provider might implement to
    // mark a pended enumeration callback as cancelled.  If the given CommandId
    // is not found, it is not an error.  It may not yet have been tracked or
    // it may already have completed and been untracked.
    MyMarkEnumForCancellation(callbackData->CommandId);
}
```
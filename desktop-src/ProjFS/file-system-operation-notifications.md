---
title: Notificações de operação do sistema de arquivos
description: Descreve como um provedor pode receber notificações de operações do sistema de arquivos.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/04/2018
ms.topic: article
ms.openlocfilehash: 2e09efcc9d1a1aea99f79b70446162df5e3ef924067ac6619a443aa15e06e9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031236"
---
# <a name="file-system-operation-notifications"></a>Notificações de operação do sistema de arquivos

Além dos retornos de chamada necessários para lidar com enumeração, retornar metadados **[]()** de arquivo e conteúdo de arquivo, um provedor pode, opcionalmente, registrar um retorno de chamada PRJ_NOTIFICATION_CB em sua chamada para **[PrjStartVirtualizing]()**.  Esse retorno de chamada recebe notificações de operações do sistema de arquivos executadas em arquivos e diretórios abaixo da raiz de virtualização da instância.  Algumas das notificações são notificações de "pós-operação", que dizem ao provedor que uma operação acabou de ser concluída.  As outras notificações são notificações de "pré-operação", o que significa que o provedor é notificado antes que a operação ocorra.  Em uma notificação de pré-operação, o provedor pode vetar a operação retornando um código de erro do retorno de chamada.  Isso faz com que a operação falhe com o código de erro retornado.

## <a name="how-to-specify-notifications-to-receive"></a>Como especificar notificações a receber

Se o provedor fornece uma implementação **de PRJ_NOTIFICATION_CB** quando inicia uma instância de virtualização, ele também deve especificar quais notificações deseja receber.  As notificações para as quais o provedor pode se registrar são definidas [na PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) enum.

Quando o provedor especifica as notificações que deseja receber, ele faz isso usando uma matriz de uma ou [mais PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) estruturas.  Eles definem "mapeamentos de notificação".  Um mapeamento de notificação é um emparelhamento entre um diretório, conhecido como "raiz de notificação" e um conjunto de notificações, expresso como uma máscara de bit, que o ProjFS deve enviar para esse diretório e seus descendentes.  Um mapeamento de notificação também pode ser estabelecido para um único arquivo.  Um arquivo ou diretório especificado em um mapeamento de notificação não precisa existir no momento em que o provedor chama **PrjStartVirtualizing**, o provedor pode especificar qualquer caminho e o mapeamento será aplicado a ele se ele for criado.

Se o provedor especificar vários mapeamentos de notificação e alguns são descendentes de outros, os mapeamentos deverão ser especificados em profundidade decrescente.  Mapeamentos de notificação em níveis mais profundos substituem os de nível superior para seus descendentes.

Se o provedor não especificar um conjunto de mapeamentos de notificação, o ProjFS padrão enviará PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED e PRJ_NOTIFY_FILE_OVERWRITTEN para todos os arquivos e diretórios abaixo da raiz de virtualização.

O snippet de código a seguir ilustra como registrar um conjunto de notificações ao iniciar uma instância de virtualização.

```C++
PRJ_CALLBACKS callbackTable;

// Supply required callbacks.
callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
callbackTable.GetFileDataCallback = MyGetFileDataCallback;

// The rest of the callbacks are optional.  We want notifications, so specify
// our notification callback.
callbackTable.QueryFileNameCallback = nullptr;
callbackTable.NotificationCallback = MyNotificationCallback;
callbackTable.CancelCommandCallback = nullptr;

// Assume the provider has created a new virtualization root at C:\VirtRoot and
// initialized it with this layout:
//
//     C:\VirtRoot
//     +--- baz
//     \--- foo
//          +--- subdir1
//          \--- subdir2
//
// The provider wants these notifications:
// * Notification of new file/directory creates for all locations within the
//   virtualization root that are not subject to one of the following more
//   specific notification mappings.
// * Notification of new file/directory creates, file opens, post-renames, and
//   pre- and post-deletes for C:\VirtRoot\foo
// * No notifications for C:\VirtRoot\foo\subdir1
PRJ_STARTVIRTUALIZING_OPTIONS startOpts = {};
PRJ_VIRTUALIZATION_MAPPING notificationMappings[3];

// Configure default notifications - notify of new files for most of the tree.
notificationMappings[0].NotificationRoot = L"";
notificationMappings[0].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED;

// Override default notifications - notify of new files, opened files, and file
// deletes for C:\VirtRoot\foo and its descendants.
notificationMappings[1].NotificationRoot = L"foo";
notificationMappings[1].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED |
                                              PRJ_NOTIFY_FILE_OPENED |
                                              PRJ_NOTIFY_PRE_DELETE |
                                              PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED |
                                              PRJ_NOTIFY_FILE_RENAMED;

// Override all notifications for C:\VirtRoot\foo\subdir1 and its descendants.
notificationMappings[2].NotificationRoot = L"foo\\subdir1";
notificationMappings[2].NotificationBitMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;

startOpts.NotificationMappings = notificationMappings;
startOpts.NotificationMappingsCount = ARRAYSIZE(notificationMapping);

// Start the instance and provide our notification mappings.
HRESULT hr;
PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
hr = PrjStartVirtualizing(rootName,
                          &callbackTable,
                          nullptr,
                          &startOpts,
                          &instanceHandle);
if (FAILED(hr))
{
    wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
    return;
}
```

## <a name="receiving-notifications"></a>Recebendo notificações

O ProjFS envia notificações de operações do sistema de arquivos chamando o retorno de PRJ_NOTIFICATION_CB **do** provedor.  Ele faz isso para cada operação para a que o provedor se registrou.  Se, como no exemplo acima, o provedor registrado para PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED um aplicativo criou um novo arquivo na raiz de notificação, o ProjFS chamaria o retorno de  chamada do PRJ_NOTIFICATION_CB com **o** nome do caminho do novo arquivo e o parâmetro de notificação definido como PRJ_NOTIFICATION_NEW_FILE_CREATED.

O ProjFS envia as notificações na lista a seguir antes que a operação do sistema de arquivos associada seja realizada.  Se o provedor retornar um código de falha do **PRJ_NOTIFICATION_CB** retorno de chamada, a operação do sistema de arquivos falhará e retornará o código de falha especificado pelo provedor.

* PRJ_NOTIFICATION_PRE_DELETE - o arquivo está prestes a ser excluído.
* PRJ_NOTIFICATION_PRE_RENAME - o arquivo está prestes a ser renomeado.
* PRJ_NOTIFICATION_PRE_SET_HARDLINK - um link rígido está prestes a ser criado para o arquivo.
* PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL - um arquivo está prestes a ser expandido de um espaço reservado para um arquivo completo, o que indica que seu conteúdo provavelmente será modificado.

O ProjFS envia as notificações na lista a seguir após a conclusão da operação do sistema de arquivos associada.

* PRJ_NOTIFICATION_FILE_OPENED - Um arquivo existente foi aberto.
  * Embora essa notificação seja enviada depois que o arquivo foi aberto, o provedor pode retornar um código de falha.  Em resposta, o ProjFS cancelará o aberto e retornará a falha ao chamador.
* PRJ_NOTIFICATION_NEW_FILE_CREATED - um novo arquivo foi criado.
* PRJ_NOTIFICATION_FILE_OVERWRITTEN - um arquivo existente foi substituído, por exemplo, chamando [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) com o sinalizador **CREATE_ALWAYS** _dwCreationDisposition._
* PRJ_NOTIFICATION_FILE_RENAMED - um arquivo foi renomeado.
* PRJ_NOTIFICATION_HARDLINK_CREATED - um [link rígido](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) foi criado para um arquivo.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION - um alça de arquivo foi fechado e o conteúdo do arquivo não foi modificado, nem o arquivo foi excluído.
* PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED - um alça de arquivo foi fechado e o conteúdo do arquivo foi modificado.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED - um alça de arquivo foi fechado e o arquivo foi excluído como parte do fechamento do alça.

Para obter mais detalhes sobre cada notificação, consulte a documentação **[do PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.

O **PRJ_NOTIFICATION_CB** _notificationParameters_ do retorno de chamada especifica parâmetros extras para determinadas notificações.  Se um provedor receber uma PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED ou PRJ_NOTIFICATION_FILE_OVERWRITTEN ou uma notificação PRJ_NOTIFICATION_FILE_RENAMED, o provedor poderá especificar um novo conjunto de notificações a ser recebido para o arquivo. Para obter mais detalhes, consulte a documentação **[do PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.

O exemplo a seguir mostra exemplos simples de como um provedor pode processar as notificações que ele registrou no snippet de código acima.

```C++
#include <windows.h>

HRESULT
MyNotificationCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ BOOLEAN isDirectory,
    _In_ PRJ_NOTIFICATION notification,
    _In_opt_z_ PCWSTR destinationFileName,
    _Inout_ PRJ_NOTIFICATION_PARAMETERS* operationParameters
    )
{
    HRESULT hr = S_OK;

    switch (notification)
    {
    case PRJ_NOTIFY_NEW_FILE_CREATED:

        wprintf(L"A new %ls was created at [%ls].\n",
                isDirectory ? L"directory" : L"file",
                callbackData->FilePathName);

        // Let's stop getting notifications inside newly-created directories.
        if (isDirectory)
        {
            operationParameters->PostCreate.NotificationMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;
        }
        break;

    case PRJ_NOTIFY_FILE_OPENED:

        wprintf(L"Handle opened to %ls [%ls].\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_PRE_DELETE:

        wprintf(L"Attempt to delete %ls [%ls]: ",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);

        // MyAllowDelete is a routine the provider might implement to decide
        // whether to allow a given file/directory to be deleted.
        if (!MyAllowDelete(callbackData->FilePathName, isDirectory))
        {
            wprintf(L"DENIED\n");
            hr = HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED);
        }
        else
        {
            wprintf(L"ALLOWED\n");
        }
        break;

    case PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED:

        wprintf(L"The %ls [%ls] was deleted.\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_FILE_RENAMED:

        if (wcslen(callbackData->FilePathName) == 0)
        {
            // If callbackData->FilePathName is an empty string, then the item
            // that was renamed was originally in a location not under the
            // virtualization root.
            wprintf(L"A %ls was renamed into the virtualization root,\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its new location is [%ls].\n",
                    destinationFileName);
        }
        else if (wcslen(destinationFileName) == 0)
        {
            // If destinationFileName is an empty string, then the item that was
            // renamed is now in a location not under the virtualization root.
            wprintf(L"A %ls was renamed out of the virtualization root.\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its original location was [%ls].\n",
                    callbackData->FilePathName);
        }
        else
        {
            // If both names are specified, both the new and old names are under
            // the virtualization root (it is never the case that nether name is
            // specified).
            wprintf(L"A %ls [%ls] was renamed.\n",
                    isDirectory ? L"directory": L"file",
                    callbackData->FilePathName);
            wprintf(L"Its new name is [%ls].\n", destinationFileName);
        }
        break;

    default:
        wprintf(L"Unrecognized notification: 0x%08x");
    }

    // Note that this may be a failure code from MyAllowDelete().
    return hr;
}
```
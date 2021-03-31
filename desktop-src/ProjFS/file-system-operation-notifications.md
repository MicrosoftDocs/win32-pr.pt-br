---
title: Notificações de operação do sistema de arquivos
description: Descreve como um provedor pode receber notificações de operações do sistema de arquivos.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/04/2018
ms.topic: article
ms.openlocfilehash: 9eae9bde6d56592f371dcd48c24fef96a9eecbdf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641226"
---
# <a name="file-system-operation-notifications"></a><span data-ttu-id="e323a-103">Notificações de operação do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="e323a-103">File System Operation Notifications</span></span>

<span data-ttu-id="e323a-104">Além dos retornos de chamada necessários para manipular a enumeração, retornar os metadados do arquivo e o conteúdo do arquivo, um provedor pode, opcionalmente, registrar um retorno de chamada **[PRJ_NOTIFICATION_CB]()** em sua chamada para **[PrjStartVirtualizing]()**.</span><span class="sxs-lookup"><span data-stu-id="e323a-104">In addition to required callbacks for handling enumeration, returning file metadata, and file contents, a provider may optionally register a **[PRJ_NOTIFICATION_CB]()** callback in its call to **[PrjStartVirtualizing]()**.</span></span>  <span data-ttu-id="e323a-105">Esse retorno de chamada recebe notificações de operações do sistema de arquivos executadas em arquivos e diretórios abaixo da raiz de virtualização da instância.</span><span class="sxs-lookup"><span data-stu-id="e323a-105">This callback receives notifications of file system operations performed on files and directories beneath the instance's virtualization root.</span></span>  <span data-ttu-id="e323a-106">Algumas das notificações são notificações de "pós-operação", que dizem ao provedor que uma operação acabou de ser concluída.</span><span class="sxs-lookup"><span data-stu-id="e323a-106">Some of the notifications are "post-operation" notifications, which tell the provider that an operation has just completed.</span></span>  <span data-ttu-id="e323a-107">As outras notificações são notificações de "pré-operação", o que significa que o provedor é notificado antes que a operação ocorra.</span><span class="sxs-lookup"><span data-stu-id="e323a-107">The other notifications are "pre-operation" notifications, meaning that the provider is notified before the operation happens.</span></span>  <span data-ttu-id="e323a-108">Em uma notificação de pré-operação, o provedor pode vetar a operação retornando um código de erro do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e323a-108">In a pre-operation notification the provider can veto the operation by returning an error code from the callback.</span></span>  <span data-ttu-id="e323a-109">Isso faz com que a operação falhe com o código de erro retornado.</span><span class="sxs-lookup"><span data-stu-id="e323a-109">This causes the operation to fail with the returned error code.</span></span>

## <a name="how-to-specify-notifications-to-receive"></a><span data-ttu-id="e323a-110">Como especificar notificações a serem recebidas</span><span class="sxs-lookup"><span data-stu-id="e323a-110">How to Specify Notifications to Receive</span></span>

<span data-ttu-id="e323a-111">Se o provedor fornecer uma implementação de **PRJ_NOTIFICATION_CB** quando ele iniciar uma instância de virtualização, ele também deverá especificar quais notificações deseja receber.</span><span class="sxs-lookup"><span data-stu-id="e323a-111">If the provider supplies an implementation of **PRJ_NOTIFICATION_CB** when it starts a virtualization instance, it should also specify which notifications it wishes to receive.</span></span>  <span data-ttu-id="e323a-112">As notificações para as quais o provedor pode registrar são definidas no [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) enum.</span><span class="sxs-lookup"><span data-stu-id="e323a-112">The notifications for which the provider can register are defined in the [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) enum.</span></span>

<span data-ttu-id="e323a-113">Quando o provedor especifica as notificações que deseja receber, ele faz isso usando uma matriz de uma ou mais estruturas de [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) .</span><span class="sxs-lookup"><span data-stu-id="e323a-113">When the provider specifies the notifications it wishes to receive, it does so using an array of one or more [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) structures.</span></span>  <span data-ttu-id="e323a-114">Eles definem "mapeamentos de notificação".</span><span class="sxs-lookup"><span data-stu-id="e323a-114">These define "notification mappings".</span></span>  <span data-ttu-id="e323a-115">Um mapeamento de notificação é um emparelhamento entre um diretório, chamado de "raiz de notificação", e um conjunto de notificações, expresso como uma máscara de bits, que ProjFS deve enviar para esse diretório e seus descendentes.</span><span class="sxs-lookup"><span data-stu-id="e323a-115">A notification mapping is a pairing between a directory, referred to as a "notification root", and a set of notifications, expressed as a bit mask, which ProjFS should send for that directory and its descendants.</span></span>  <span data-ttu-id="e323a-116">Um mapeamento de notificação também pode ser estabelecido para um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="e323a-116">A notification mapping can also be established for a single file.</span></span>  <span data-ttu-id="e323a-117">Um arquivo ou diretório especificado em um mapeamento de notificação não precisa existir no momento em que o provedor chama **PrjStartVirtualizing**, o provedor pode especificar qualquer caminho e o mapeamento será aplicado a ele se ele já estiver criado.</span><span class="sxs-lookup"><span data-stu-id="e323a-117">A file or directory specified in a notification mapping does not have to exist already at the time the provider calls **PrjStartVirtualizing**, the provider can specify any path and the mapping will apply to it if it is ever created.</span></span>

<span data-ttu-id="e323a-118">Se o provedor especificar vários mapeamentos de notificação e alguns forem descendentes de outros, os mapeamentos deverão ser especificados em profundidade decrescente.</span><span class="sxs-lookup"><span data-stu-id="e323a-118">If the provider specifies multiple notification mappings, and some are descendants of others, the mappings must be specified in descending depth.</span></span>  <span data-ttu-id="e323a-119">Os mapeamentos de notificação em níveis mais detalhados substituem os de nível superior por seus descendentes.</span><span class="sxs-lookup"><span data-stu-id="e323a-119">Notification mappings at deeper levels override higher-level ones for their descendants.</span></span>

<span data-ttu-id="e323a-120">Se o provedor não especificar um conjunto de mapeamentos de notificação, o padrão ProjFS será enviá-lo PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED e PRJ_NOTIFY_FILE_OVERWRITTEN para todos os arquivos e diretórios abaixo da raiz de virtualização.</span><span class="sxs-lookup"><span data-stu-id="e323a-120">If the provider does not specify a set of notification mappings, ProjFS will default to sending it PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED, and PRJ_NOTIFY_FILE_OVERWRITTEN for all files and directories beneath the virtualization root.</span></span>

<span data-ttu-id="e323a-121">O trecho de código a seguir ilustra como registrar um conjunto de notificações ao iniciar uma instância de virtualização.</span><span class="sxs-lookup"><span data-stu-id="e323a-121">The following code snippet illustrates how to register a set of notifications when starting a virtualization instance.</span></span>

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

## <a name="receiving-notifications"></a><span data-ttu-id="e323a-122">Recebendo notificações</span><span class="sxs-lookup"><span data-stu-id="e323a-122">Receiving Notifications</span></span>

<span data-ttu-id="e323a-123">O ProjFS envia notificações de operações do sistema de arquivos chamando o retorno de chamada do **PRJ_NOTIFICATION_CB** do provedor.</span><span class="sxs-lookup"><span data-stu-id="e323a-123">ProjFS sends notifications of file system operations by calling the provider's **PRJ_NOTIFICATION_CB** callback.</span></span>  <span data-ttu-id="e323a-124">Ele faz isso para cada operação para a qual o provedor se registrou.</span><span class="sxs-lookup"><span data-stu-id="e323a-124">It does this for each operation the provider has registered for.</span></span>  <span data-ttu-id="e323a-125">Se, como no exemplo acima, o provedor registrado para PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED, e um aplicativo criou um novo arquivo na raiz de notificação, ProjFS chamaria o retorno de chamada **PRJ_NOTIFICATION_CB** com o nome do caminho do novo arquivo e o parâmetro de _notificação_ definido como PRJ_NOTIFICATION_NEW_FILE_CREATED.</span><span class="sxs-lookup"><span data-stu-id="e323a-125">If, as in the above example, the provider registered for PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED, and an application created a new file in the notification root, ProjFS would call the **PRJ_NOTIFICATION_CB** callback with the new file's path name and the _notification_ parameter set to PRJ_NOTIFICATION_NEW_FILE_CREATED.</span></span>

<span data-ttu-id="e323a-126">O ProjFS envia as notificações na lista a seguir antes que a operação do sistema de arquivos associada ocorra.</span><span class="sxs-lookup"><span data-stu-id="e323a-126">ProjFS sends the notifications in the following list before the associated file system operation takes place.</span></span>  <span data-ttu-id="e323a-127">Se o provedor retornar um código de falha do **PRJ_NOTIFICATION_CB** retorno de chamada, a operação do sistema de arquivos falhará e retornará o código de falha especificado pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="e323a-127">If the provider returns a failure code from the **PRJ_NOTIFICATION_CB** callback, the file system operation will fail and return the failure code the provider specified.</span></span>

* <span data-ttu-id="e323a-128">PRJ_NOTIFICATION_PRE_DELETE-o arquivo está prestes a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="e323a-128">PRJ_NOTIFICATION_PRE_DELETE - The file is about to be deleted.</span></span>
* <span data-ttu-id="e323a-129">PRJ_NOTIFICATION_PRE_RENAME-o arquivo está prestes a ser renomeado.</span><span class="sxs-lookup"><span data-stu-id="e323a-129">PRJ_NOTIFICATION_PRE_RENAME - The file is about to be renamed.</span></span>
* <span data-ttu-id="e323a-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK-um link físico está prestes a ser criado para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="e323a-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK - A hard link is about to be created for the file.</span></span>
* <span data-ttu-id="e323a-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL-um arquivo está prestes a ser expandido de um espaço reservado para um arquivo completo, o que indica que seu conteúdo provavelmente será modificado.</span><span class="sxs-lookup"><span data-stu-id="e323a-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL - A file is about to be expanded from a placeholder to a full file, which indicates its contents are likely to be modified.</span></span>

<span data-ttu-id="e323a-132">O ProjFS envia as notificações na lista a seguir após a conclusão da operação do sistema de arquivos associada.</span><span class="sxs-lookup"><span data-stu-id="e323a-132">ProjFS sends the notifications in the following list after the associated file system operation has completed.</span></span>

* <span data-ttu-id="e323a-133">PRJ_NOTIFICATION_FILE_OPENED-um arquivo existente foi aberto.</span><span class="sxs-lookup"><span data-stu-id="e323a-133">PRJ_NOTIFICATION_FILE_OPENED - An existing file has been opened.</span></span>
  * <span data-ttu-id="e323a-134">Embora essa notificação seja enviada depois que o arquivo tiver sido aberto, o provedor pode retornar um código de falha.</span><span class="sxs-lookup"><span data-stu-id="e323a-134">Even though this notification is sent after the file has been opened, the provider can return a failure code.</span></span>  <span data-ttu-id="e323a-135">Em resposta, o ProjFS cancelará a abertura e retornará a falha para o chamador.</span><span class="sxs-lookup"><span data-stu-id="e323a-135">In response, ProjFS will cancel the open and return the failure to the caller.</span></span>
* <span data-ttu-id="e323a-136">PRJ_NOTIFICATION_NEW_FILE_CREATED-um novo arquivo foi criado.</span><span class="sxs-lookup"><span data-stu-id="e323a-136">PRJ_NOTIFICATION_NEW_FILE_CREATED - A new file has been created.</span></span>
* <span data-ttu-id="e323a-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN-um arquivo existente foi substituído, por exemplo, chamando [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) com o sinalizador **CREATE_ALWAYS** _dwCreationDisposition_ .</span><span class="sxs-lookup"><span data-stu-id="e323a-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN - An existing file has been overwritten, for example by calling [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) with the **CREATE_ALWAYS** _dwCreationDisposition_ flag.</span></span>
* <span data-ttu-id="e323a-138">PRJ_NOTIFICATION_FILE_RENAMED-um arquivo foi renomeado.</span><span class="sxs-lookup"><span data-stu-id="e323a-138">PRJ_NOTIFICATION_FILE_RENAMED - A file has been renamed.</span></span>
* <span data-ttu-id="e323a-139">PRJ_NOTIFICATION_HARDLINK_CREATED-um [link físico](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) foi criado para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e323a-139">PRJ_NOTIFICATION_HARDLINK_CREATED - A [hard link](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) has been created for a file.</span></span>
* <span data-ttu-id="e323a-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION-um identificador de arquivo foi fechado, e o conteúdo do arquivo não foi modificado, nem o arquivo foi excluído.</span><span class="sxs-lookup"><span data-stu-id="e323a-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION - A file handle has been closed, and the file's content was not modified, nor was the file deleted.</span></span>
* <span data-ttu-id="e323a-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED-um identificador de arquivo foi fechado e o conteúdo do arquivo foi modificado.</span><span class="sxs-lookup"><span data-stu-id="e323a-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED - A file handle has been closed, and the file's content has been modified.</span></span>
* <span data-ttu-id="e323a-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED-um identificador de arquivo foi fechado e o arquivo foi excluído como parte do fechamento do identificador.</span><span class="sxs-lookup"><span data-stu-id="e323a-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED - A file handle has been closed, and the file was deleted as part of closing the handle.</span></span>

<span data-ttu-id="e323a-143">Para obter mais detalhes sobre cada notificação, consulte a documentação do **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span><span class="sxs-lookup"><span data-stu-id="e323a-143">For more details on each notification refer to the documentation for **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span></span>

<span data-ttu-id="e323a-144">O parâmetro _notificationparameters_ do **PRJ_NOTIFICATION_CB** callback especifica parâmetros extras para determinadas notificações.</span><span class="sxs-lookup"><span data-stu-id="e323a-144">The **PRJ_NOTIFICATION_CB** callback's _notificationParameters_ parameter specifies extra parameters for certain notifications.</span></span>  <span data-ttu-id="e323a-145">Se um provedor receber uma notificação PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED ou PRJ_NOTIFICATION_FILE_OVERWRITTEN ou PRJ_NOTIFICATION_FILE_RENAMED, o provedor poderá especificar um novo conjunto de notificações a receber para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="e323a-145">If a provider receives a PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED, or PRJ_NOTIFICATION_FILE_OVERWRITTEN, or PRJ_NOTIFICATION_FILE_RENAMED notification, the provider can specify a new set of notifications to receive for the file.</span></span> <span data-ttu-id="e323a-146">Para obter mais detalhes, consulte a documentação do **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span><span class="sxs-lookup"><span data-stu-id="e323a-146">For further details, refer to the documentation for **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span></span>

<span data-ttu-id="e323a-147">O exemplo a seguir mostra exemplos simples de como um provedor pode processar as notificações registradas no trecho de código acima.</span><span class="sxs-lookup"><span data-stu-id="e323a-147">The following sample shows simple examples of how a provider might process the notifications it registered for in the code snippet above.</span></span>

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
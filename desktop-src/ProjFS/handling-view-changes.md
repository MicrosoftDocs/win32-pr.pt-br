---
title: Manipulando alterações de exibição
description: Descreve como atualizar a exibição de cliente do armazenamento de backup de um provedor.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 1d5a709752f92b7449d2ccc38f67c4417edf8d62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007667"
---
# <a name="handling-view-changes"></a><span data-ttu-id="e69ed-103">Manipulando alterações de exibição</span><span class="sxs-lookup"><span data-stu-id="e69ed-103">Handling View Changes</span></span>

<span data-ttu-id="e69ed-104">Como os arquivos e diretórios na raiz de virtualização são abertos, o provedor cria espaços reservados no disco e, à medida que os arquivos são lidos, os espaços reservados são alimentados com o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e69ed-104">As files and directories under the virtualization root are opened, the provider creates placeholders on disk, and as files are read the placeholders are hydrated with contents.</span></span>  <span data-ttu-id="e69ed-105">Esses espaços reservados representam o estado do repositório de backup no momento em que foram criados.</span><span class="sxs-lookup"><span data-stu-id="e69ed-105">These placeholders represent the state of the backing store at the time they were created.</span></span>  <span data-ttu-id="e69ed-106">Esses itens armazenados em cache, combinados com os itens projetados pelo provedor em enumerações, constituem a "exibição" do cliente do repositório de backup.</span><span class="sxs-lookup"><span data-stu-id="e69ed-106">These cached items, combined with the items projected by the provider in enumerations, constitute the client's "view" of the backing store.</span></span>  <span data-ttu-id="e69ed-107">De tempos em tempos, o provedor pode desejar atualizar a exibição do cliente, independentemente de alterações no repositório de backup ou devido à ação explícita tomada pelo usuário para alterar sua exibição.</span><span class="sxs-lookup"><span data-stu-id="e69ed-107">From time to time the provider may wish to update the client's view, whether because of changes in the backing store, or because of explicit action taken by the user to change their view.</span></span>

> <span data-ttu-id="e69ed-108">Se o provedor atualizar a exibição proativamente, à medida que o armazenamento de backup for alterado, é recomendável que as alterações de exibição sejam relativamente infrequentes.</span><span class="sxs-lookup"><span data-stu-id="e69ed-108">If the provider updates the view proactively, as the backing store changes, it is recommended that view changes be relatively infrequent.</span></span>  <span data-ttu-id="e69ed-109">Isso ocorre porque uma exibição é alterada para um item que foi aberto e, portanto, tinha um espaço reservado criado no disco, requer que o item em disco seja atualizado ou excluído para refletir a alteração da exibição.</span><span class="sxs-lookup"><span data-stu-id="e69ed-109">This is because a view change to an item that has been opened, and therefore had a placeholder created on disk, requires that the on-disk item be either updated or deleted to reflect the view change.</span></span>  <span data-ttu-id="e69ed-110">Atualizações frequentes podem resultar em atividade de disco extra que pode afetar negativamente o desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="e69ed-110">Frequent updates may result in extra disk activity that can negatively impact system performance.</span></span>

## <a name="item-versioning"></a><span data-ttu-id="e69ed-111">Controle de versão do item</span><span class="sxs-lookup"><span data-stu-id="e69ed-111">Item Versioning</span></span>

<span data-ttu-id="e69ed-112">Para dar suporte à manutenção de vários modos de exibição, o ProjFS fornece o **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.</span><span class="sxs-lookup"><span data-stu-id="e69ed-112">To support maintaining multiple views, ProjFS provides the **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.</span></span>  <span data-ttu-id="e69ed-113">Um provedor usa essa struct autônomo em chamadas para **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** e é inserido nas estruturas **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** e **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** .</span><span class="sxs-lookup"><span data-stu-id="e69ed-113">A provider uses this struct standalone in calls to **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)**, and it is embedded in the **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** and **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** structs.</span></span>  <span data-ttu-id="e69ed-114">O **PRJ_PLACEHOLDER_VERSION_INFO**. O campo ContentId é onde o provedor armazena até 128 bytes de informações de versão para um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="e69ed-114">The **PRJ_PLACEHOLDER_VERSION_INFO**.ContentID field is where the provider stores up to 128 bytes of version information for a file or directory.</span></span>  <span data-ttu-id="e69ed-115">O provedor pode, então, associar internamente esse valor a algum valor que identifique uma determinada exibição.</span><span class="sxs-lookup"><span data-stu-id="e69ed-115">The provider may then internally associate this value to some value that identifies a particular view.</span></span>

<span data-ttu-id="e69ed-116">Por exemplo, um provedor que virtualiza um repositório de controle do código-fonte pode optar por usar um hash do conteúdo de um arquivo para servir como ContentId e pode usar carimbos de data/hora para identificar exibições do repositório em vários pontos no tempo.</span><span class="sxs-lookup"><span data-stu-id="e69ed-116">For example, a provider that virtualizes a source control repository might choose to use a hash of a file's contents to serve as the ContentID, and it might use timestamps to identify views of the repository at various points in time.</span></span>  <span data-ttu-id="e69ed-117">Os carimbos de data/hora podem ser os horários em que as confirmações do repositório foram executadas.</span><span class="sxs-lookup"><span data-stu-id="e69ed-117">The timestamps might be the times that commits to the repository were performed.</span></span>

<span data-ttu-id="e69ed-118">Usando o exemplo de um repositório indexado por carimbo de data/hora, um fluxo típico para usar ContentId de um item pode ser:</span><span class="sxs-lookup"><span data-stu-id="e69ed-118">Using the example of a timestamp-indexed repository, a typical flow for using an item's ContentID might be:</span></span>

1. <span data-ttu-id="e69ed-119">O cliente estabelece uma exibição especificando o carimbo de data/hora no qual apresentar o conteúdo do repositório.</span><span class="sxs-lookup"><span data-stu-id="e69ed-119">The client establishes a view by specifying the timestamp at which to present the repository contents.</span></span>  <span data-ttu-id="e69ed-120">Isso seria feito por meio de alguma interface implementada pelo provedor, não por meio de uma API ProjFS.</span><span class="sxs-lookup"><span data-stu-id="e69ed-120">This would be done through some interface implemented by the provider, not via a ProjFS API.</span></span>  <span data-ttu-id="e69ed-121">Por exemplo, o provedor pode ter uma ferramenta de linha de comando que poderia ser usada para informar ao provedor que exibe o desejo do usuário.</span><span class="sxs-lookup"><span data-stu-id="e69ed-121">For example, the provider may have a command-line tool that could be used to tell the provider which view the user desires.</span></span>
1. <span data-ttu-id="e69ed-122">Quando o cliente cria um identificador para um arquivo ou diretório virtualizado, o provedor cria um espaço reservado para ele, usando metadados do sistema de arquivos do repositório de backup.</span><span class="sxs-lookup"><span data-stu-id="e69ed-122">When the client creates a handle to a virtualized file or directory, the provider creates a placeholder for it, using file system metadata from the backing store.</span></span>  <span data-ttu-id="e69ed-123">O conjunto específico de metadados que ele usa é identificado pelo valor ContentId associado ao carimbo de data/hora da exibição desejada.</span><span class="sxs-lookup"><span data-stu-id="e69ed-123">The particular set of metadata it uses is identified by the ContentID value associated with the timestamp of the desired view.</span></span>  <span data-ttu-id="e69ed-124">Quando o provedor chama **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** para gravar as informações de espaço reservado, ele fornece o ContentId no membro VERSIONINFO do argumento _placeholderInfo_ .</span><span class="sxs-lookup"><span data-stu-id="e69ed-124">When the provider calls **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** to write the placeholder information, it supplies the ContentID in the VersionInfo member of the _placeholderInfo_ argument.</span></span>  <span data-ttu-id="e69ed-125">Em seguida, o provedor deve registrar que um espaço reservado para esse arquivo ou diretório foi criado nessa exibição.</span><span class="sxs-lookup"><span data-stu-id="e69ed-125">The provider should then record that a placeholder for that file or directory was created in this view.</span></span>
1. <span data-ttu-id="e69ed-126">Quando o cliente lê de um espaço reservado, o **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** retorno de chamada do provedor é invocado.</span><span class="sxs-lookup"><span data-stu-id="e69ed-126">When the client reads from a placeholder, the provider's **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** callback is invoked.</span></span>  <span data-ttu-id="e69ed-127">O membro VersionInfo do parâmetro _callbackdata_ contém ContentId o provedor especificado em **PrjWritePlaceholderInfo** quando ele criou o espaço reservado do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e69ed-127">The _callbackData_ parameter's VersionInfo member contains the ContentID the provider specified in **PrjWritePlaceholderInfo** when it created the file placeholder.</span></span>  <span data-ttu-id="e69ed-128">O provedor usa esse ContentId para recuperar o conteúdo correto do arquivo de seu armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="e69ed-128">The provider uses that ContentID to retrieve the correct contents of the file from its backing store.</span></span>
1. <span data-ttu-id="e69ed-129">O cliente solicita uma alteração de exibição especificando um novo carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="e69ed-129">The client requests a view change by specifying a new timestamp.</span></span>  <span data-ttu-id="e69ed-130">Para cada espaço reservado que o provedor criou na exibição anterior, se uma versão diferente desse arquivo existir na nova exibição, o provedor poderá substituir o espaço reservado no disco por um atualizado cujo ContentId esteja associado ao novo carimbo de data/hora chamando **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.</span><span class="sxs-lookup"><span data-stu-id="e69ed-130">For each placeholder the provider created in the previous view, if a different version of that file exists in the new view the provider may replace the placeholder on disk with an updated one whose ContentID is associated with the new timestamp by calling **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.</span></span>  <span data-ttu-id="e69ed-131">Como alternativa, o provedor pode excluir o espaço reservado chamando **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** para que a nova exibição do arquivo seja projetada em enumerações.</span><span class="sxs-lookup"><span data-stu-id="e69ed-131">Alternatively, the provider may delete the placeholder by calling **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** so that the new view of the file will be projected in enumerations.</span></span>  <span data-ttu-id="e69ed-132">Se o arquivo não existir no novo modo de exibição, o provedor deverá excluí-lo chamando **PrjDeleteFile**.</span><span class="sxs-lookup"><span data-stu-id="e69ed-132">If the file does not exist in the new view, the provider must delete it by calling **PrjDeleteFile**.</span></span>

<span data-ttu-id="e69ed-133">Observe que o provedor deve garantir que, quando o cliente enumera um diretório, o provedor fornecerá o conteúdo que corresponde à exibição do cliente.</span><span class="sxs-lookup"><span data-stu-id="e69ed-133">Note that the provider must ensure that when the client enumerates a directory, the provider will supply the contents that correspond to the client's view.</span></span>  <span data-ttu-id="e69ed-134">Por exemplo, o provedor poderia usar o membro VersionInfo do parâmetro _callbackdata_ do **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** e **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** retornos de chamada para recuperar o conteúdo do diretório em tempo real.</span><span class="sxs-lookup"><span data-stu-id="e69ed-134">For example, the provider could use the VersionInfo member of the _callbackData_ parameter of the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** and **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** callbacks to retrieve directory contents on the fly.</span></span>  <span data-ttu-id="e69ed-135">Como alternativa, ele poderia criar uma estrutura de diretório para essa exibição em seu armazenamento de backup como parte do estabelecimento da exibição e, em seguida, simplesmente enumerar essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="e69ed-135">Alternatively it could build a directory structure for that view in its backing store as part of establishing the view, and then simply enumerate that structure.</span></span>

> <span data-ttu-id="e69ed-136">Sempre que um retorno de chamada do provedor é invocado para um espaço reservado ou arquivo parcial, as informações de versão que o provedor especificou ao criar o item são fornecidas no membro VersionInfo do parâmetro _callbackdata_ do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e69ed-136">Whenever a provider callback is invoked for a placeholder or partial file, the version information the provider specified when creating the item is provided in the VersionInfo member of the callback's _callbackData_ parameter.</span></span>

## <a name="updating-the-view"></a><span data-ttu-id="e69ed-137">Atualizando a exibição</span><span class="sxs-lookup"><span data-stu-id="e69ed-137">Updating the View</span></span>

<span data-ttu-id="e69ed-138">Abaixo está uma função de exemplo que ilustra como um provedor pode atualizar a exibição local quando o usuário especifica um novo carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="e69ed-138">Below is a sample function illustrating how a provider might update the local view when the user specifies a new timestamp.</span></span>  <span data-ttu-id="e69ed-139">A função recupera uma lista dos espaços reservados que o provedor criou para a exibição do qual o usuário acabou de alterar e atualiza o estado do cache local com base no estado de cada espaço reservado na nova exibição.</span><span class="sxs-lookup"><span data-stu-id="e69ed-139">The function retrieves a list of the placeholders the provider created for the view the user has just changed from, and updates the local cache state based on each placeholder's state in the new view.</span></span>  <span data-ttu-id="e69ed-140">Para maior clareza, essa rotina omite determinadas complexidades de lidar com o sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e69ed-140">For clarity, this routine omits certain complexities of dealing with the file system.</span></span>  <span data-ttu-id="e69ed-141">Por exemplo, na exibição antiga, um determinado diretório pode ter existido com alguns arquivos ou diretórios, mas na nova exibição que o diretório (e seu conteúdo) pode não existir mais.</span><span class="sxs-lookup"><span data-stu-id="e69ed-141">For example, in the old view a given directory may have existed with some files or directories in it, but in the new view that directory (and its contents) may no longer exist.</span></span>  <span data-ttu-id="e69ed-142">Para evitar erros em tal situação, o provedor deve atualizar o estado do arquivo e dos diretórios sob a raiz de virtualização de uma maneira de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e69ed-142">To avoid encountering errors in such a situation the provider should update the state of the file and directories beneath the virtualization root in a depth-first fashion.</span></span>

```C++
typedef struct MY_ON_DISK_PLACEHOLDER MY_ON_DISK_PLACEHOLDER;

typedef struct MY_ON_DISK_PLACEHOLDER {
    MY_ON_DISK_PLACEHOLDER* Next;
    PWSTR RelativePath;
} MY_ON_DISK_PLACEHOLDER;

HRESULT
MyViewUpdater(
    _In_ PRJ_CALLBACK_DATA callbackData,
    _In_ time_t newViewTime
    )
{
    HRESULT hr = S_OK;

    // MyGetOnDiskPlaceholders is a routine the provider might implement to produce
    // a pointer to a list of the placeholders the provider has created in the view.
    MY_ON_DISK_PLACEHOLDER* placeholder = MyGetOnDiskPlaceholders();
    while (placeholder != NULL)
    {
        // MyGetProjectedFileInfo is a routine the provider might implement to
        // determine whether a given file exists in its backing store at a
        // particular timestamp.  If it does, the routine returns a pointer to
        // a PRJ_PLACEHOLDER_INFO struct populated with information about the
        // file.
        PRJ_PLACEHOLDER_INFO* newViewPlaceholderInfo = NULL;
        UINT32 newViewPlaceholderInfoSize = 0;

        newViewPlaceholderInfo = MyGetProjectedFileInfo(placeholder->RelativePath,
                                                 newViewTime,
                                                 &newViewPlaceholderInfoSize);
        if (newViewPlaceholderInfo == NULL)
        {
            // The file no longer exists in the new view.  We want to remove its
            // placeholder from the local cache.
            PRJ_UPDATE_FAILURE_CAUSES deleteFailureReason;
            hr = PrjDeleteFile(callbackData->NamespaceVirtualizationContext,
                               placeholder->RelativePath,
                               PRJ_UPDATE_ALLOW_DIRTY_METADATA
                               | PRJ_UPDATE_ALLOW_DIRTY_DATA
                               | PRJ_UPDATE_ALLOW_TOMBSTONE,
                               &deleteFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not delete [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", deleteFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error deleting [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyRemovePlaceholderData is a routine the provider might implement
            // to remove an item from its list of placeholders it has created in
            // the view.
            MyRemovePlaceholderData(placeholder);
        }
        else
        {
            // The file exists in the new view.  Its local cache state may need
            // to be updated, for example if its content is different in this view.
            // As an optimization, the provider may compare the file's ContentID
            // in the new view (stored in newViewPlaceholderInfo->ContentId) with
            // the ContentID it had in the old view.  If they are the same, calling
            // PrjUpdateFileIfNeeded would not be needed.
            PRJ_UPDATE_FAILURE_CAUSES updateFailureReason;
            hr = PrjUpdateFileIfNeeded(callbackData->NamespaceVirtualizationContext,
                                       placeholder->RelativePath,
                                       newViewPlaceholderInfo,
                                       newViewPlaceholderInfoSize,
                                       PRJ_UPDATE_ALLOW_DIRTY_METADATA
                                       | PRJ_UPDATE_ALLOW_DIRTY_DATA
                                       | PRJ_UPDATE_ALLOW_TOMBSTONE,
                                       &updateFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not update [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", updateFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error updating [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyUpdatePlaceholderData is a routine the provider might implement
            // to update information about a placeholder it has created in the view.
            MyUpdatePlaceholderData(placeholder, newViewPlaceholderInfo);
        }

        placeholder = placeholder->Next;
    }

    return hr;
}
```
---
title: Fornecer dados de arquivo
description: Descreve como um provedor fornece informações de espaço reservado e dados de arquivo.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/01/2018
ms.topic: article
ms.openlocfilehash: 341a0f1c477b605b2a437edf311c380910744ac0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366385"
---
# <a name="providing-file-data"></a><span data-ttu-id="94889-103">Fornecer dados de arquivo</span><span class="sxs-lookup"><span data-stu-id="94889-103">Providing File Data</span></span>

<span data-ttu-id="94889-104">Quando um provedor cria pela primeira vez uma raiz de virtualização, ele está vazio no sistema local.</span><span class="sxs-lookup"><span data-stu-id="94889-104">When a provider first creates a virtualization root it is empty on the local system.</span></span> <span data-ttu-id="94889-105">Ou seja, nenhum dos itens no armazenamento de dados de backup ainda foi armazenado em cache no disco.</span><span class="sxs-lookup"><span data-stu-id="94889-105">That is, none of the items in the backing data store have yet been cached to disk.</span></span> <span data-ttu-id="94889-106">À medida que os itens são abertos, o ProjFS solicita informações do provedor para permitir que os espaços reservados para esses itens sejam criados no sistema de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="94889-106">As items are opened, ProjFS requests information from the provider to allow placeholders for those items to be created in the local file system.</span></span>  <span data-ttu-id="94889-107">À medida que o conteúdo do item é acessado, o ProjFS solicita o conteúdo do provedor.</span><span class="sxs-lookup"><span data-stu-id="94889-107">As item contents are accessed, ProjFS requests those contents from the provider.</span></span>  <span data-ttu-id="94889-108">O resultado é que, da perspectiva do usuário, os arquivos virtualizados e os diretórios são semelhantes aos arquivos normais e aos diretórios que já residem no sistema de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="94889-108">The result is that from the user's perspective, virtualized files and directories appear similar to normal files and directories that already reside on the local file system.</span></span>

## <a name="placeholder-creation"></a><span data-ttu-id="94889-109">Criação de espaço reservado</span><span class="sxs-lookup"><span data-stu-id="94889-109">Placeholder Creation</span></span>

<span data-ttu-id="94889-110">Quando um aplicativo tenta abrir um identificador para um arquivo virtualizado, ProjFS chama o retorno de chamada **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** para cada item do caminho que ainda não existe no disco.</span><span class="sxs-lookup"><span data-stu-id="94889-110">When an application attempts to open a handle to a virtualized file, ProjFS calls the **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** callback for each item of the path that does not yet exist on disk.</span></span>  <span data-ttu-id="94889-111">Por exemplo, se um aplicativo tentar abrir `C:\virtRoot\dir1\dir2\file.txt` , mas apenas o caminho `C:\virtRoot\dir1` existir no disco, o provedor receberá um retorno de chamada para `C:\virtRoot\dir1\dir2` `C:\virtRoot\dir1\dir2\file.txt` .</span><span class="sxs-lookup"><span data-stu-id="94889-111">For example, if an application tries to open `C:\virtRoot\dir1\dir2\file.txt`, but only the path `C:\virtRoot\dir1` exists on disk, then the provider will receive a callback for `C:\virtRoot\dir1\dir2`, then for `C:\virtRoot\dir1\dir2\file.txt`.</span></span>

<span data-ttu-id="94889-112">Quando ProjFS chama o retorno de chamada de **PRJ_GET_PLACEHOLDER_INFO_CB** do provedor, o provedor executa as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="94889-112">When ProjFS calls the provider's **PRJ_GET_PLACEHOLDER_INFO_CB** callback, the provider performs the following actions:</span></span>

1. <span data-ttu-id="94889-113">O provedor determina se o nome solicitado existe em seu armazenamento de backup.</span><span class="sxs-lookup"><span data-stu-id="94889-113">The provider determines whether the requested name exists in its backing store.</span></span>  <span data-ttu-id="94889-114">O provedor deve usar **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** como a rotina de comparação ao pesquisar seu repositório de backup para determinar se o nome solicitado existe no repositório de backup.</span><span class="sxs-lookup"><span data-stu-id="94889-114">The provider should use **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** as the comparison routine when searching its backing store to determine whether the requested name exists in the backing store.</span></span>  <span data-ttu-id="94889-115">Caso contrário, o provedor retornará HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND) do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="94889-115">If it does not, the provider returns HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) from the callback.</span></span>

1. <span data-ttu-id="94889-116">Se o nome solicitado existir no repositório de backup, o provedor populará uma estrutura de [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) com os metadados do sistema de arquivos do item e chamará **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** para enviar os dados para ProjFS.</span><span class="sxs-lookup"><span data-stu-id="94889-116">If the requested name does exist in the backing store, the provider populates a [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) structure with the item's file system metadata and calls **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** to send the data to ProjFS.</span></span>  <span data-ttu-id="94889-117">O ProjFS usará essas informações para criar um espaço reservado no sistema de arquivos local para o item.</span><span class="sxs-lookup"><span data-stu-id="94889-117">ProjFS will use that information to create a placeholder in the local file system for the item.</span></span>

    > <span data-ttu-id="94889-118">ProjFS usará qualquer FILE_ATTRIBUTE sinalizar os conjuntos de provedores no membro **FileBasicInfo. FileAttributes** de PRJ_PLACEHOLDER_INFO, exceto para FILE_ATTRIBUTE_DIRECTORY; ele definirá o valor correto para FILE_ATTRIBUTE_DIRECTORY no membro **FileBasicInfo. FileAttributes** de acordo com o valor fornecido do membro **FileBasicInfo. IsDirectory** .</span><span class="sxs-lookup"><span data-stu-id="94889-118">ProjFS will use whatever FILE_ATTRIBUTE flags the provider sets in the **FileBasicInfo.FileAttributes** member of PRJ_PLACEHOLDER_INFO except for FILE_ATTRIBUTE_DIRECTORY; it will set the correct value for FILE_ATTRIBUTE_DIRECTORY in the **FileBasicInfo.FileAttributes** member according to the supplied value of the **FileBasicInfo.IsDirectory** member.</span></span>

    > <span data-ttu-id="94889-119">Se o armazenamento de backup der suporte a links simbólicos, o provedor deverá usar **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** para enviar os dados de espaço reservado para ProjFS.</span><span class="sxs-lookup"><span data-stu-id="94889-119">If the backing store supports symbolic links, the provider must use **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** to send the placeholder data to ProjFS.</span></span>  <span data-ttu-id="94889-120">O **PrjWritePlaceholderInfo2** dá suporte a uma entrada de buffer extra que permite que o provedor especifique que o espaço reservado é um link simbólico e qual é seu destino.</span><span class="sxs-lookup"><span data-stu-id="94889-120">**PrjWritePlaceholderInfo2** supports an extra buffer input that allows the provider to specify that the placeholder is a symbolic link and what its target is.</span></span>  <span data-ttu-id="94889-121">Caso contrário, ele se comporta conforme descrito acima para **PrjWritePlaceholderInfo**.</span><span class="sxs-lookup"><span data-stu-id="94889-121">It otherwise behaves as described above for **PrjWritePlaceholderInfo**.</span></span>  <span data-ttu-id="94889-122">O exemplo a seguir ilustra como usar o **PrjWritePlaceholderInfo2** para fornecer suporte para links simbólicos.</span><span class="sxs-lookup"><span data-stu-id="94889-122">The following sample illustrates how to use **PrjWritePlaceholderInfo2** to provide support for symbolic links.</span></span>
    >
    > <span data-ttu-id="94889-123">Observe que o **PrjWritePlaceholderInfo2** tem suporte a partir do Windows 10, versão 2004.</span><span class="sxs-lookup"><span data-stu-id="94889-123">Note that **PrjWritePlaceholderInfo2** is supported as of Windows 10, version 2004.</span></span>  <span data-ttu-id="94889-124">Um provedor deve investigar a existência de **PrjWritePlaceholderInfo2**, por exemplo, usando **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span><span class="sxs-lookup"><span data-stu-id="94889-124">A provider should probe for the existence of **PrjWritePlaceholderInfo2**, for instance by using **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span></span>

```C++
HRESULT
MyGetPlaceholderInfoCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
    )
{
    // MyGetItemInfo is a routine the provider might implement to get
    // information from its backing store for a given file path.  The first
    // parameter is an _In_ parameter that supplies the name to look for.
    // If the item exists the routine provides the file information in the
    // remaining parameters, all of which are annotated _Out_:
    // * 2nd parameter: the name as it appears in the backing store
    // * 3rd-9th parameters: basic file info
    // * 10th parameter: if the item is a symbolic link, a pointer to a 
    //   NULL-terminated string identifying the link's target
    //
    // Note that the routine returns the name that is in the backing
    // store.  This is because the input file path may not be in the same
    // case as what is in the backing store.  The provider should create
    // the placeholder with the name it has in the backing store.
    //
    // Note also that this example does not provide anything beyond basic
    // file information and a possible symbolic link target.
    HRESULT hr;
    WCHAR* backingStoreName = NULL;
    WCHAR* symlinkTarget = NULL;
    PRJ_PLACEHOLDER_INFO placeholderInfo = {};
    hr = MyGetItemInfo(callbackData->FilePathName,
                       &backingStoreName,
                       &placeholderInfo.FileBasicInfo.IsDirectory,
                       &placeholderInfo.FileBasicInfo.FileSize,
                       &placeholderInfo.FileBasicInfo.CreationTime,
                       &placeholderInfo.FileBasicInfo.LastAccessTime,
                       &placeholderInfo.FileBasicInfo.LastWriteTime,
                       &placeholderInfo.FileBasicInfo.ChangeTime,
                       &placeholderInfo.FileBasicInfo.FileAttributes,
                       &symlinkTarget);

    if (FAILED(hr))
    {
        // If callbackData->FilePathName doesn't exist in our backing store then
        // MyGetItemInfo should HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND).
        // If this is some other error, e.g. E_OUTOFMEMORY because MyGetItemInfo
        // couldn't allocate space for backingStoreName, we return that.
        return hr;
    }

    // If the file path is for a symbolic link, pass that in with the placeholder info.
    if (symlinkTarget != NULL)
    {
        PRJ_EXTENDED_INFO extraInfo = {};

        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
        extraInfo.Symlink.TargetName = symlinkTarget;

        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo2(callbackData->NamespaceVirtualizationContext,
                                      backingStoreName,
                                      &placeholderInfo,
                                      sizeof(placeholderInfo),
                                      &extraInfo);
    }
    else
    {
        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo(callbackData->NamespaceVirtualizationContext,
                                     backingStoreName,
                                     &placeholderInfo,
                                     sizeof(placeholderInfo));
    }

    free(backingStoreName);

    if (symlinkTarget != NULL)
    {
        free(symlinkTarget);
    }

    return hr;
}
```

## <a name="providing-file-contents"></a><span data-ttu-id="94889-125">Fornecendo conteúdo do arquivo</span><span class="sxs-lookup"><span data-stu-id="94889-125">Providing File Contents</span></span>

<span data-ttu-id="94889-126">Quando o ProjFS precisa garantir que um arquivo virtualizado contenha dados, como quando um aplicativo tenta ler a partir do arquivo, o ProjFS chama o retorno de chamada **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** para esse item para solicitar que o provedor forneça o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="94889-126">When ProjFS needs to ensure that a virtualized file contains data, such as when an application attempts to read from the file, ProjFS calls the **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** callback for that item to request that the provider supply the file's contents.</span></span>  <span data-ttu-id="94889-127">O provedor recupera os dados do arquivo de seu armazenamento de backup e usa **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** para enviar os dados para o sistema de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="94889-127">The provider retrieves the file's data from its backing store and uses **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** to send the data to the local file system.</span></span>

> <span data-ttu-id="94889-128">Quando o ProjFS chama esse retorno de chamada, o membro **FilePathName** do parâmetro _callbackdata_ fornece o nome que o arquivo tinha quando seu espaço reservado foi criado.</span><span class="sxs-lookup"><span data-stu-id="94889-128">When ProjFS calls this callback, the **FilePathName** member of the _callbackData_ parameter supplies the name the file had when its placeholder was created.</span></span>  <span data-ttu-id="94889-129">Ou seja, se o arquivo foi renomeado desde que seu espaço reservado foi criado, o retorno de chamada fornece o nome original (pré-renomear), não o nome atual (após o renomeação).</span><span class="sxs-lookup"><span data-stu-id="94889-129">That is, if the file has been renamed since its placeholder was created, the callback supplies the original (pre-rename) name, not the current (post-rename) name.</span></span>  <span data-ttu-id="94889-130">Se necessário, o provedor pode usar o membro **VERSIONINFO** do parâmetro _callbackdata_ para determinar quais dados do arquivo estão sendo solicitados.</span><span class="sxs-lookup"><span data-stu-id="94889-130">If necessary, the provider can use the **VersionInfo** member of the _callbackData_ parameter to determine which file's data is being requested.</span></span>
>
> <span data-ttu-id="94889-131">Para obter mais informações sobre como o membro **VERSIONINFO** de PRJ_CALLBACK_DATA pode ser usado, consulte a documentação do [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) e o tópico [manipulando alterações de exibição](handling-view-changes.md) .</span><span class="sxs-lookup"><span data-stu-id="94889-131">For more information on how the **VersionInfo** member of PRJ_CALLBACK_DATA may be used, see the documentation for [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) and the [Handling View Changes](handling-view-changes.md) topic.</span></span>

<span data-ttu-id="94889-132">O provedor tem permissão para dividir o intervalo de dados solicitados no retorno de chamada **PRJ_GET_FILE_DATA_CB** em várias chamadas para **PrjWriteFileData**, cada um fornecendo uma parte do intervalo solicitado.</span><span class="sxs-lookup"><span data-stu-id="94889-132">The provider is allowed to split the range of data requested in the **PRJ_GET_FILE_DATA_CB** callback into multiple calls to **PrjWriteFileData**, each supplying a portion of the requested range.</span></span>  <span data-ttu-id="94889-133">No entanto, o provedor deve fornecer todo o intervalo solicitado antes de concluir o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="94889-133">However, the provider must supply the entire requested range before completing the callback.</span></span>  <span data-ttu-id="94889-134">Por exemplo, se o retorno de chamada solicitar 10 MB de dados de _byteOffset_ 0 para o _comprimento_ 10.485.760, o provedor poderá optar por fornecer os dados em 10 chamadas para **PrjWriteFileData**, cada um enviando 1 MB.</span><span class="sxs-lookup"><span data-stu-id="94889-134">For example, if the callback requests 10 MB of data from _byteOffset_ 0 for _length_ 10,485,760, the provider may choose to supply the data in 10 calls to **PrjWriteFileData**, each sending 1 MB.</span></span>

<span data-ttu-id="94889-135">O provedor também é gratuito para fornecer mais do que o intervalo solicitado, até o comprimento do arquivo.</span><span class="sxs-lookup"><span data-stu-id="94889-135">The provider is also free to supply more than the requested range, up to the length of the file.</span></span>  <span data-ttu-id="94889-136">O intervalo que o provedor fornece deve abranger o intervalo solicitado.</span><span class="sxs-lookup"><span data-stu-id="94889-136">The range the provider supplies must cover the requested range.</span></span>  <span data-ttu-id="94889-137">Por exemplo, se o retorno de chamada solicitar 1 MB de dados de _byteOffset_ 4096 para _comprimento_ 1.052.672 e o arquivo tiver um tamanho total de 10 MB, o provedor poderá optar por retornar 2 MB de dados começando no deslocamento 0.</span><span class="sxs-lookup"><span data-stu-id="94889-137">For example, if the callback requests 1 MB of data from _byteOffset_ 4096 for _length_ 1,052,672, and the file has a total size of 10 MB, the provider could choose to return 2 MB of data starting at offset 0.</span></span>

### <a name="buffer-alignment-considerations"></a><span data-ttu-id="94889-138">Considerações sobre alinhamento de buffer</span><span class="sxs-lookup"><span data-stu-id="94889-138">Buffer Alignment Considerations</span></span>

<span data-ttu-id="94889-139">O ProjFS usa o [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) do chamador que exige que os dados gravem os dados no sistema de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="94889-139">ProjFS uses the [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) from the caller who requires the data to write the data to the local file system.</span></span>  <span data-ttu-id="94889-140">No entanto, ProjFS não pode controlar se esse FILE_OBJECT foi aberto para e/s em buffer ou sem buffer.</span><span class="sxs-lookup"><span data-stu-id="94889-140">However ProjFS cannot control whether that FILE_OBJECT was opened for buffered or unbuffered I/O.</span></span>  <span data-ttu-id="94889-141">Se o FILE_OBJECT foi aberto para e/s não armazenada em buffer, leituras e gravações no arquivo devem aderir a determinados requisitos de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="94889-141">If the FILE_OBJECT was opened for unbuffered I/O, reads and writes to the file must adhere to certain alignment requirements.</span></span>  <span data-ttu-id="94889-142">O provedor pode atender a esses requisitos de alinhamento fazendo duas coisas:</span><span class="sxs-lookup"><span data-stu-id="94889-142">The provider can meet those alignment requirements by doing two things:</span></span>

1. <span data-ttu-id="94889-143">Use **[PrjAllocateAlignedBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** para alocar o buffer para passar o parâmetro de _buffer_ de **PrjWriteFileData**.</span><span class="sxs-lookup"><span data-stu-id="94889-143">Use **[PrjAllocateAlignedBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** to allocate the buffer to pass in **PrjWriteFileData**'s _buffer_ parameter.</span></span>
1. <span data-ttu-id="94889-144">Verifique se os parâmetros _byteOffset_ e _Length_ de **PrjWriteFileData** são múltiplos inteiros do requisito de alinhamento do dispositivo de armazenamento (Observe que o parâmetro _Length_ não precisa atender a esse requisito se _byteOffset_  +  _Length_ for igual ao final do arquivo).</span><span class="sxs-lookup"><span data-stu-id="94889-144">Ensure that the _byteOffset_ and _length_ parameters of **PrjWriteFileData** are integer multiples of the storage device's alignment requirement (note that the _length_ parameter does not have to meet this requirement if _byteOffset_ + _length_ is equal to the end of the file).</span></span>  <span data-ttu-id="94889-145">O provedor pode usar **[PrjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** para recuperar o requisito de alinhamento do dispositivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="94889-145">The provider can use **[PrjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** to retrieve the storage device's alignment requirement.</span></span>

<span data-ttu-id="94889-146">ProjFS deixa-o para o provedor para calcular o alinhamento adequado.</span><span class="sxs-lookup"><span data-stu-id="94889-146">ProjFS leaves it up to the provider to calculate proper alignment.</span></span>  <span data-ttu-id="94889-147">Isso ocorre porque, ao processar um **PRJ_GET_FILE_DATA_CB** callback, o provedor pode optar por retornar os dados solicitados entre várias chamadas **PrjWriteFileData** , cada uma retornando parte do total de dados solicitados, antes de concluir o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="94889-147">This is because when processing a **PRJ_GET_FILE_DATA_CB** callback the provider may opt to return the requested data across multiple **PrjWriteFileData** calls, each returning part of the total requested data, before completing the callback.</span></span>

> <span data-ttu-id="94889-148">Se o provedor usar uma única chamada para **PrjWriteFileData** para gravar todo o arquivo, ou seja, de _byteOffset_ = 0 até _comprimento_ = tamanho do arquivo, ou para retornar o intervalo exato solicitado no retorno de chamada **PRJ_GET_FILE_DATA_CB** , o provedor não precisará fazer nenhum cálculo de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="94889-148">If the provider is going to use a single call to **PrjWriteFileData** to either write the entire file, i.e. from _byteOffset_ = 0 to _length_ = size of the file, or to return the exact range requested in the **PRJ_GET_FILE_DATA_CB** callback, the provider does not have to do any alignment calculations.</span></span>  <span data-ttu-id="94889-149">No entanto, ele ainda deve usar **PrjAllocateAlignedBuffer** para garantir que o _buffer_ atenda aos requisitos de alinhamento do dispositivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="94889-149">However, it must still use **PrjAllocateAlignedBuffer** to ensure that _buffer_ meets the storage device’s alignment requirements.</span></span>

<span data-ttu-id="94889-150">Consulte o tópico [buffer de arquivo](/windows/desktop/FileIO/file-buffering) para obter mais informações sobre e/s em buffer versus sem buffer.</span><span class="sxs-lookup"><span data-stu-id="94889-150">See the topic [File Buffering](/windows/desktop/FileIO/file-buffering) for more information on buffered vs. unbuffered I/O.</span></span>

```C++
//  BlockAlignTruncate(): Aligns P on the previous V boundary (V must be != 0).
#define BlockAlignTruncate(P,V) ((P) & (0-((UINT64)(V))))

// This sample illustrates both returning the entire requested range in a
// single call to PrjWriteFileData(), and splitting it up into smaller 
// units.  Note that the provider must return all the requested data before
// completing the PRJ_GET_FILE_DATA_CB callback with S_OK.
HRESULT
MyGetFileDataCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ UINT64 byteOffset,
    _In_ UINT32 length
    )
{
    HRESULT hr;

    // For the purposes of this sample our provider has a 1 MB limit to how
    // much data it can return at once (perhaps its backing store imposes such
    // a limit).
    UINT64 writeStartOffset;
    UINT32 writeLength;
    if (length <= 1024*1024)
    {
        // The range requested in the callback is less than 1MB, so we can return
        // the data in a single call, without doing any alignment calculations.
        writeStartOffset = byteOffset;
        writeLength = length;
    }
    else
    {
        // The range requested is more than 1MB.  Retrieve the device alignment
        // and calculate a transfer size that conforms to the device alignment and
        // is <= 1MB.
        PRJ_VIRTUALIZATION_INSTANCE_INFO instanceInfo;
        UINT32 infoSize = sizeof(instanceInfo);
        hr = PrjGetVirtualizationInstanceInfo(callbackData->NamespaceVirtualizationContext,
                                              &infoSize,
                                              &instanceInfo);

        if (FAILED(hr))
        {
            return hr;
        }

        // The first transfer will start at the beginning of the requested range,
        // which is guaranteed to have the correct alignment.
        writeStartOffset = byteOffset;

        // Ensure our transfer size is aligned to the device alignment, and is
        // no larger than 1 MB (note this assumes the device alignment is less
        // than 1 MB).
        UINT64 writeEndOffset = BlockAlignTruncate(writeStartOffset + 1024*1024,
                                                   instanceInfo->WriteAlignment);
        assert(writeEndOffset > 0);
        assert(writeEndOffset > writeStartOffset);

        writeLength = writeEndOffset - writeStartOffset;
    }

    // Allocate a buffer that adheres to the needed memory alignment.
    void* writeBuffer = NULL;
    writeBuffer = PrjAllocateAlignedBuffer(callbackData->NamespaceVirtualizationContext,
                                           writeLength);

    if (writeBuffer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    do
    {
        // MyGetFileDataFromStore is a routine the provider might implement to copy
        // data for the specified file from the provider's backing store to a
        // buffer.  The routine finds the file located at callbackData->FilePathName
        // and copies writeLength bytes of its data, starting at writeStartOffset,
        // to the buffer pointed to by writeBuffer.
        hr = MyGetFileDataFromStore(callbackData->FilePathName,
                                    writeStartOffset,
                                    writeLength,
                                    writeBuffer);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // Write the data to the file in the local file system.
        hr = PrjWriteFileData(callbackData->NamespaceVirtualizationContext,
                              callbackData->DataStreamId,
                              writeBuffer,
                              writeStartOffset,
                              writeLength);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // The length parameter to the callback is guaranteed to be either
        // correctly aligned or to result in a write to the end of the file.
        length -= writeLength;
        if (length < writeLength)
        {
            writeLength = length;
        }
    }
    while (writeLength > 0);

    PrjFreeAlignedBuffer(writeBuffer);
    return hr;
}
```
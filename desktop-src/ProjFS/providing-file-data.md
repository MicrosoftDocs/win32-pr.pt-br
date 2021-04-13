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
# <a name="providing-file-data"></a>Fornecer dados de arquivo

Quando um provedor cria pela primeira vez uma raiz de virtualização, ele está vazio no sistema local. Ou seja, nenhum dos itens no armazenamento de dados de backup ainda foi armazenado em cache no disco. À medida que os itens são abertos, o ProjFS solicita informações do provedor para permitir que os espaços reservados para esses itens sejam criados no sistema de arquivos local.  À medida que o conteúdo do item é acessado, o ProjFS solicita o conteúdo do provedor.  O resultado é que, da perspectiva do usuário, os arquivos virtualizados e os diretórios são semelhantes aos arquivos normais e aos diretórios que já residem no sistema de arquivos local.

## <a name="placeholder-creation"></a>Criação de espaço reservado

Quando um aplicativo tenta abrir um identificador para um arquivo virtualizado, ProjFS chama o retorno de chamada **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** para cada item do caminho que ainda não existe no disco.  Por exemplo, se um aplicativo tentar abrir `C:\virtRoot\dir1\dir2\file.txt` , mas apenas o caminho `C:\virtRoot\dir1` existir no disco, o provedor receberá um retorno de chamada para `C:\virtRoot\dir1\dir2` `C:\virtRoot\dir1\dir2\file.txt` .

Quando ProjFS chama o retorno de chamada de **PRJ_GET_PLACEHOLDER_INFO_CB** do provedor, o provedor executa as seguintes ações:

1. O provedor determina se o nome solicitado existe em seu armazenamento de backup.  O provedor deve usar **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** como a rotina de comparação ao pesquisar seu repositório de backup para determinar se o nome solicitado existe no repositório de backup.  Caso contrário, o provedor retornará HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND) do retorno de chamada.

1. Se o nome solicitado existir no repositório de backup, o provedor populará uma estrutura de [PRJ_PLACEHOLDER_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) com os metadados do sistema de arquivos do item e chamará **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** para enviar os dados para ProjFS.  O ProjFS usará essas informações para criar um espaço reservado no sistema de arquivos local para o item.

    > ProjFS usará qualquer FILE_ATTRIBUTE sinalizar os conjuntos de provedores no membro **FileBasicInfo. FileAttributes** de PRJ_PLACEHOLDER_INFO, exceto para FILE_ATTRIBUTE_DIRECTORY; ele definirá o valor correto para FILE_ATTRIBUTE_DIRECTORY no membro **FileBasicInfo. FileAttributes** de acordo com o valor fornecido do membro **FileBasicInfo. IsDirectory** .

    > Se o armazenamento de backup der suporte a links simbólicos, o provedor deverá usar **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** para enviar os dados de espaço reservado para ProjFS.  O **PrjWritePlaceholderInfo2** dá suporte a uma entrada de buffer extra que permite que o provedor especifique que o espaço reservado é um link simbólico e qual é seu destino.  Caso contrário, ele se comporta conforme descrito acima para **PrjWritePlaceholderInfo**.  O exemplo a seguir ilustra como usar o **PrjWritePlaceholderInfo2** para fornecer suporte para links simbólicos.
    >
    > Observe que o **PrjWritePlaceholderInfo2** tem suporte a partir do Windows 10, versão 2004.  Um provedor deve investigar a existência de **PrjWritePlaceholderInfo2**, por exemplo, usando **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

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

## <a name="providing-file-contents"></a>Fornecendo conteúdo do arquivo

Quando o ProjFS precisa garantir que um arquivo virtualizado contenha dados, como quando um aplicativo tenta ler a partir do arquivo, o ProjFS chama o retorno de chamada **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** para esse item para solicitar que o provedor forneça o conteúdo do arquivo.  O provedor recupera os dados do arquivo de seu armazenamento de backup e usa **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** para enviar os dados para o sistema de arquivos local.

> Quando o ProjFS chama esse retorno de chamada, o membro **FilePathName** do parâmetro _callbackdata_ fornece o nome que o arquivo tinha quando seu espaço reservado foi criado.  Ou seja, se o arquivo foi renomeado desde que seu espaço reservado foi criado, o retorno de chamada fornece o nome original (pré-renomear), não o nome atual (após o renomeação).  Se necessário, o provedor pode usar o membro **VERSIONINFO** do parâmetro _callbackdata_ para determinar quais dados do arquivo estão sendo solicitados.
>
> Para obter mais informações sobre como o membro **VERSIONINFO** de PRJ_CALLBACK_DATA pode ser usado, consulte a documentação do [PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) e o tópico [manipulando alterações de exibição](handling-view-changes.md) .

O provedor tem permissão para dividir o intervalo de dados solicitados no retorno de chamada **PRJ_GET_FILE_DATA_CB** em várias chamadas para **PrjWriteFileData**, cada um fornecendo uma parte do intervalo solicitado.  No entanto, o provedor deve fornecer todo o intervalo solicitado antes de concluir o retorno de chamada.  Por exemplo, se o retorno de chamada solicitar 10 MB de dados de _byteOffset_ 0 para o _comprimento_ 10.485.760, o provedor poderá optar por fornecer os dados em 10 chamadas para **PrjWriteFileData**, cada um enviando 1 MB.

O provedor também é gratuito para fornecer mais do que o intervalo solicitado, até o comprimento do arquivo.  O intervalo que o provedor fornece deve abranger o intervalo solicitado.  Por exemplo, se o retorno de chamada solicitar 1 MB de dados de _byteOffset_ 4096 para _comprimento_ 1.052.672 e o arquivo tiver um tamanho total de 10 MB, o provedor poderá optar por retornar 2 MB de dados começando no deslocamento 0.

### <a name="buffer-alignment-considerations"></a>Considerações sobre alinhamento de buffer

O ProjFS usa o [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) do chamador que exige que os dados gravem os dados no sistema de arquivos local.  No entanto, ProjFS não pode controlar se esse FILE_OBJECT foi aberto para e/s em buffer ou sem buffer.  Se o FILE_OBJECT foi aberto para e/s não armazenada em buffer, leituras e gravações no arquivo devem aderir a determinados requisitos de alinhamento.  O provedor pode atender a esses requisitos de alinhamento fazendo duas coisas:

1. Use **[PrjAllocateAlignedBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** para alocar o buffer para passar o parâmetro de _buffer_ de **PrjWriteFileData**.
1. Verifique se os parâmetros _byteOffset_ e _Length_ de **PrjWriteFileData** são múltiplos inteiros do requisito de alinhamento do dispositivo de armazenamento (Observe que o parâmetro _Length_ não precisa atender a esse requisito se _byteOffset_  +  _Length_ for igual ao final do arquivo).  O provedor pode usar **[PrjGetVirtualizationInstanceInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** para recuperar o requisito de alinhamento do dispositivo de armazenamento.

ProjFS deixa-o para o provedor para calcular o alinhamento adequado.  Isso ocorre porque, ao processar um **PRJ_GET_FILE_DATA_CB** callback, o provedor pode optar por retornar os dados solicitados entre várias chamadas **PrjWriteFileData** , cada uma retornando parte do total de dados solicitados, antes de concluir o retorno de chamada.

> Se o provedor usar uma única chamada para **PrjWriteFileData** para gravar todo o arquivo, ou seja, de _byteOffset_ = 0 até _comprimento_ = tamanho do arquivo, ou para retornar o intervalo exato solicitado no retorno de chamada **PRJ_GET_FILE_DATA_CB** , o provedor não precisará fazer nenhum cálculo de alinhamento.  No entanto, ele ainda deve usar **PrjAllocateAlignedBuffer** para garantir que o _buffer_ atenda aos requisitos de alinhamento do dispositivo de armazenamento.

Consulte o tópico [buffer de arquivo](/windows/desktop/FileIO/file-buffering) para obter mais informações sobre e/s em buffer versus sem buffer.

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
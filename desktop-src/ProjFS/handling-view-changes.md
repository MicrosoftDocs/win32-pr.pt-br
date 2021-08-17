---
title: Manipulando alterações de exibição
description: Descreve como atualizar a exibição do cliente do armazenamento de back-back de um provedor.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 99ace7849b8967748f26210d9d6b770e424c349359aa39e828c8ad9af36a65af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792643"
---
# <a name="handling-view-changes"></a>Manipulando alterações de exibição

À medida que arquivos e diretórios na raiz de virtualização são abertos, o provedor cria espaço reservados no disco e, à medida que os arquivos são lidos, os espaço reservados são alimentados com conteúdo.  Esses espaço reservados representam o estado do armazenamento de back-back no momento em que foram criados.  Esses itens armazenados em cache, combinados com os itens projetados pelo provedor em enumerações, constituem a "exibição" do cliente do armazenamento de back-back.  De tempos em tempos, o provedor pode querer atualizar a exibição do cliente, seja devido a alterações no armazenamento de back-back ou devido à ação explícita tomada pelo usuário para alterar sua exibição.

> Se o provedor atualizar a exibição proativamente, à medida que o armazenamento de suporte mudar, é recomendável que as alterações de exibição sejam relativamente pouco frequentes.  Isso ocorre porque uma alteração de exibição para um item que foi aberto e, portanto, tinha um espaço reservado criado no disco, exige que o item em disco seja atualizado ou excluído para refletir a alteração da exibição.  Atualizações frequentes podem resultar em atividade de disco extra que pode afetar negativamente o desempenho do sistema.

## <a name="item-versioning"></a>Versão do item

Para dar suporte à manutenção de várias exibições, o ProjFS **[fornece PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.  Um provedor usa esse struct autônomo em chamadas para **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** e é inserido nos structs **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** e **[PRJ_CALLBACK_DATA.](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)**  O **PRJ_PLACEHOLDER_VERSION_INFO**. O campo ContentID é onde o provedor armazena até 128 bytes de informações de versão para um arquivo ou diretório.  O provedor pode associar internamente esse valor a algum valor que identifique uma exibição específica.

Por exemplo, um provedor que virtualiza um repositório de controle do código-fonte pode optar por usar um hash do conteúdo de um arquivo para servir como ContentID e pode usar osstamps de data/hora para identificar exibições do repositório em vários pontos no tempo.  Os timestamps podem ser os horários em que as confirmações no repositório foram executadas.

Usando o exemplo de um repositório indexado por timestamp, um fluxo típico para usar ContentID de um item pode ser:

1. O cliente estabelece uma exibição especificando o timestamp no qual apresentar o conteúdo do repositório.  Isso seria feito por meio de alguma interface implementada pelo provedor, não por meio de uma API projFS.  Por exemplo, o provedor pode ter uma ferramenta de linha de comando que pode ser usada para dizer ao provedor qual exibir o desejo do usuário.
1. Quando o cliente cria um handle para um arquivo ou diretório virtualizado, o provedor cria um espaço reservado para ele, usando metadados do sistema de arquivos do armazenamento de backing.  O conjunto específico de metadados que ele usa é identificado pelo valor ContentID associado ao timestamp da exibição desejada.  Quando o provedor chama **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** para gravar as informações de espaço reservado, ele fornece o ContentID no membro VersionInfo do _argumento placeholderInfo._  Em seguida, o provedor deve registrar que um espaço reservado para esse arquivo ou diretório foi criado nessa exibição.
1. Quando o cliente lê de um espaço **[](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** reservado, o retorno de PRJ_GET_FILE_DATA_CB do provedor é invocado.  O membro VersionInfo do parâmetro _callbackData_ contém o ContentID especificado em **PrjWritePlaceholderInfo** quando ele criou o espaço reservado do arquivo.  O provedor usa essa ContentID para recuperar o conteúdo correto do arquivo de seu armazenamento de apoio.
1. O cliente solicita uma alteração de exibição especificando um novo timestamp.  Para cada espaço reservado criado pelo provedor na exibição anterior, se houver uma versão diferente desse arquivo na nova exibição, o provedor poderá substituir o espaço reservado no disco por um atualizado cujo ContentID está associado ao novo timestamp chamando **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.  Como alternativa, o provedor pode excluir o espaço reservado chamando **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** para que a nova exibição do arquivo seja projetada em enumerações.  Se o arquivo não existir na nova exibição, o provedor deverá excluí-lo chamando **PrjDeleteFile**.

Observe que o provedor deve garantir que, quando o cliente enumerar um diretório, o provedor fornecerá o conteúdo que corresponde à exibição do cliente.  Por exemplo, o provedor pode usar o membro VersionInfo do parâmetro **[](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** _callbackData_ dos retornos de chamada **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** e PRJ_GET_DIRECTORY_ENUMERATION_CB para recuperar o conteúdo do diretório em tempo real.  Como alternativa, ele pode criar uma estrutura de diretório para essa exibição em seu armazenamento de apoio como parte do estabelecimento da exibição e, em seguida, simplesmente enumerar essa estrutura.

> Sempre que um retorno de chamada do provedor é invocado para um espaço reservado ou arquivo parcial, as informações de versão especificadas pelo provedor ao criar o item são fornecidas no membro VersionInfo do parâmetro _callbackData_ do retorno de chamada.

## <a name="updating-the-view"></a>Atualizando a exibição

Veja abaixo uma função de exemplo que ilustra como um provedor pode atualizar a exibição local quando o usuário especifica um novo timestamp.  A função recupera uma lista dos espaço reservados que o provedor criou para a exibição que o usuário acabou de mudar e atualiza o estado do cache local com base no estado de cada espaço reservado na nova exibição.  Para maior clareza, essa rotina omite determinadas complexidades de lidar com o sistema de arquivos.  Por exemplo, na exibição antiga, um determinado diretório pode ter existido com alguns arquivos ou diretórios nele, mas na nova exibição esse diretório (e seu conteúdo) pode não existir mais.  Para evitar encontrar erros nessa situação, o provedor deve atualizar o estado do arquivo e dos diretórios abaixo da raiz de virtualização de maneira aprofundada.

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
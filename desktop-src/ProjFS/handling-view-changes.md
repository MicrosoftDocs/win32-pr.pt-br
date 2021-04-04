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
# <a name="handling-view-changes"></a>Manipulando alterações de exibição

Como os arquivos e diretórios na raiz de virtualização são abertos, o provedor cria espaços reservados no disco e, à medida que os arquivos são lidos, os espaços reservados são alimentados com o conteúdo.  Esses espaços reservados representam o estado do repositório de backup no momento em que foram criados.  Esses itens armazenados em cache, combinados com os itens projetados pelo provedor em enumerações, constituem a "exibição" do cliente do repositório de backup.  De tempos em tempos, o provedor pode desejar atualizar a exibição do cliente, independentemente de alterações no repositório de backup ou devido à ação explícita tomada pelo usuário para alterar sua exibição.

> Se o provedor atualizar a exibição proativamente, à medida que o armazenamento de backup for alterado, é recomendável que as alterações de exibição sejam relativamente infrequentes.  Isso ocorre porque uma exibição é alterada para um item que foi aberto e, portanto, tinha um espaço reservado criado no disco, requer que o item em disco seja atualizado ou excluído para refletir a alteração da exibição.  Atualizações frequentes podem resultar em atividade de disco extra que pode afetar negativamente o desempenho do sistema.

## <a name="item-versioning"></a>Controle de versão do item

Para dar suporte à manutenção de vários modos de exibição, o ProjFS fornece o **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.  Um provedor usa essa struct autônomo em chamadas para **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** e é inserido nas estruturas **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** e **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** .  O **PRJ_PLACEHOLDER_VERSION_INFO**. O campo ContentId é onde o provedor armazena até 128 bytes de informações de versão para um arquivo ou diretório.  O provedor pode, então, associar internamente esse valor a algum valor que identifique uma determinada exibição.

Por exemplo, um provedor que virtualiza um repositório de controle do código-fonte pode optar por usar um hash do conteúdo de um arquivo para servir como ContentId e pode usar carimbos de data/hora para identificar exibições do repositório em vários pontos no tempo.  Os carimbos de data/hora podem ser os horários em que as confirmações do repositório foram executadas.

Usando o exemplo de um repositório indexado por carimbo de data/hora, um fluxo típico para usar ContentId de um item pode ser:

1. O cliente estabelece uma exibição especificando o carimbo de data/hora no qual apresentar o conteúdo do repositório.  Isso seria feito por meio de alguma interface implementada pelo provedor, não por meio de uma API ProjFS.  Por exemplo, o provedor pode ter uma ferramenta de linha de comando que poderia ser usada para informar ao provedor que exibe o desejo do usuário.
1. Quando o cliente cria um identificador para um arquivo ou diretório virtualizado, o provedor cria um espaço reservado para ele, usando metadados do sistema de arquivos do repositório de backup.  O conjunto específico de metadados que ele usa é identificado pelo valor ContentId associado ao carimbo de data/hora da exibição desejada.  Quando o provedor chama **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** para gravar as informações de espaço reservado, ele fornece o ContentId no membro VERSIONINFO do argumento _placeholderInfo_ .  Em seguida, o provedor deve registrar que um espaço reservado para esse arquivo ou diretório foi criado nessa exibição.
1. Quando o cliente lê de um espaço reservado, o **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** retorno de chamada do provedor é invocado.  O membro VersionInfo do parâmetro _callbackdata_ contém ContentId o provedor especificado em **PrjWritePlaceholderInfo** quando ele criou o espaço reservado do arquivo.  O provedor usa esse ContentId para recuperar o conteúdo correto do arquivo de seu armazenamento de backup.
1. O cliente solicita uma alteração de exibição especificando um novo carimbo de data/hora.  Para cada espaço reservado que o provedor criou na exibição anterior, se uma versão diferente desse arquivo existir na nova exibição, o provedor poderá substituir o espaço reservado no disco por um atualizado cujo ContentId esteja associado ao novo carimbo de data/hora chamando **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.  Como alternativa, o provedor pode excluir o espaço reservado chamando **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** para que a nova exibição do arquivo seja projetada em enumerações.  Se o arquivo não existir no novo modo de exibição, o provedor deverá excluí-lo chamando **PrjDeleteFile**.

Observe que o provedor deve garantir que, quando o cliente enumera um diretório, o provedor fornecerá o conteúdo que corresponde à exibição do cliente.  Por exemplo, o provedor poderia usar o membro VersionInfo do parâmetro _callbackdata_ do **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** e **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** retornos de chamada para recuperar o conteúdo do diretório em tempo real.  Como alternativa, ele poderia criar uma estrutura de diretório para essa exibição em seu armazenamento de backup como parte do estabelecimento da exibição e, em seguida, simplesmente enumerar essa estrutura.

> Sempre que um retorno de chamada do provedor é invocado para um espaço reservado ou arquivo parcial, as informações de versão que o provedor especificou ao criar o item são fornecidas no membro VersionInfo do parâmetro _callbackdata_ do retorno de chamada.

## <a name="updating-the-view"></a>Atualizando a exibição

Abaixo está uma função de exemplo que ilustra como um provedor pode atualizar a exibição local quando o usuário especifica um novo carimbo de data/hora.  A função recupera uma lista dos espaços reservados que o provedor criou para a exibição do qual o usuário acabou de alterar e atualiza o estado do cache local com base no estado de cada espaço reservado na nova exibição.  Para maior clareza, essa rotina omite determinadas complexidades de lidar com o sistema de arquivos.  Por exemplo, na exibição antiga, um determinado diretório pode ter existido com alguns arquivos ou diretórios, mas na nova exibição que o diretório (e seu conteúdo) pode não existir mais.  Para evitar erros em tal situação, o provedor deve atualizar o estado do arquivo e dos diretórios sob a raiz de virtualização de uma maneira de profundidade.

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
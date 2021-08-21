---
title: Requisitos para que players de áudio portáteis apareçam no Windows Explorer
description: Requisitos para que players de áudio portáteis apareçam no Windows Explorer
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Mídia Gerenciador de Dispositivos, players de áudio portáteis
- Gerenciador de Dispositivos, players de áudio portáteis
- guia de programação, players de áudio portáteis
- provedores de serviços, players de áudio portáteis
- criando provedores de serviços, players de áudio portáteis
- player de áudio portátil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d91e844f564ead03ddb78cf57c13c81a56bc8934bbfbde51c105b5c7e1e2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055574"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a>Requisitos para que players de áudio portáteis apareçam no Windows Explorer

A extensão de namespace do shell do player de áudio portátil fornece Windows usuários com uma maneira consistente de gerenciar dispositivos de áudio gerenciados pelo Windows Media Gerenciador de Dispositivos. Se você for autor de seu provedor de serviços e componentes de driver de acordo com as diretrizes a seguir, seu dispositivo será aparecer no namespace do shell. Os usuários poderão interagir com o conteúdo do dispositivo de maneira consistente no Windows Explorer para executar operações básicas, como copiar, excluir e renomear.

Os requisitos de shell a seguir para o provedor de serviços e os componentes do driver destinam-se a complementar as diretrizes gerais Windows mídia Gerenciador de Dispositivos mídia.

Funcionalidades do dispositivo

Windows Os provedores Gerenciador de Dispositivos serviços de mídia devem ser explícitos em seus recursos com suporte. Se não há suporte para uma chamada, um código de erro deve ser retornado. Os campos apropriados devem ser definidos para a presença ou ausência de recursos no retorno das seguintes funções:

-   [**IMDSPStorageGlobals::GetCapabilities**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [**IMDSPStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

Os provedores de serviços devem dar suporte aos seguintes recursos para serem compatíveis com o shell:

-   Copiar para o dispositivo (com suporte para retornos de chamada de cancelamento e progresso)
-   Excluir arquivo do dispositivo (com suporte para retornos de chamada de cancelamento e progresso)
-   Renomear o arquivo no dispositivo
-   Relatório de espaço (espaço total, espaço livre, espaço inutilizável)
-   Plug and Play (consulte [Habilitando o PnP para dispositivos](enabling-pnp-for-devices.md))
-   Formato (preferencialmente com suporte para retornos de chamada de cancelamento e progresso)

Se há suporte para metadados, os campos a seguir devem ter suporte para arquivos individuais. Se nenhum dado estiver disponível, o campo deverá ser inicializado como uma cadeia de caracteres vazia:



| Campo        | Constante (definida em WMDM.idl) | Marca de metadados    |
|--------------|--------------------------------|-----------------|
| Título da música   | g \_ wszWMDMTitle                | WMDM/Título      |
| Número da faixa | g \_ wszWMDMTrack                | WMDM/Track      |
| Artista       | g \_ wszWMDMAuthor               | WMDM/Autor     |
| Álbum        | g \_ wszWMDMAlbumTitle           | WMDM/AlbumTitle |
| Year         | g \_ wszWMDMYear                 | WMDM/Ano       |
| Gênero        | g \_ wszWMDMGenre                | WMDM/Gênero      |



 

Simultaneidade

Os drivers de modo kernel Windows mídia Gerenciador de Dispositivos precisam ser robustos para lidar com o acesso simultâneo. Por exemplo, um usuário pode acessar simultaneamente o dispositivo por meio do shell e do player de mídia ou simplesmente por meio de várias janelas no shell. Como parte do tratamento da simultância, os drivers não devem assumir, apenas porque o provedor de serviços está carregado, que o dispositivo está em uso. Em vez disso, eles devem implementar um mecanismo de bloqueio para serializar o acesso ao dispositivo conforme necessário para operações individuais.

Interface do usuário

Provedores de serviços para Windows mídia Gerenciador de Dispositivos não devem mostrar nenhuma interface do usuário. Todos os erros devem ser retornados de chamadas de método como Windows mídia Gerenciador de Dispositivos códigos de erro sempre que possível.

Habilitando no Shell

Se o pacote atender a todos os requisitos de shell, você poderá permitir que seu dispositivo seja mostrado no shell definindo o valor *ShowInShell* como 1 nos parâmetros do dispositivo. Para obter mais informações, consulte [Parâmetros de dispositivo](device-parameters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um provedor de serviços**](creating-a-service-provider.md)
</dt> </dl>

 

 





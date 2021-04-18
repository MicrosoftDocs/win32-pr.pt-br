---
title: Requisitos para players de áudio portáteis aparecerem no Windows Explorer
description: Requisitos para players de áudio portáteis aparecerem no Windows Explorer
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Media Gerenciador de Dispositivos, players de áudio portáteis
- Gerenciador de Dispositivos, players de áudio portáteis
- Guia de programação, players de áudio portáteis
- provedores de serviços, players de áudio portáteis
- criando provedores de serviços, players de áudio portáteis
- players de áudio portáteis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a163bf04f4185bc1325aa12ea6acddd43191529
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105784929"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a>Requisitos para players de áudio portáteis aparecerem no Windows Explorer

A extensão de namespace do Shell player de áudio portátil fornece aos usuários do Windows uma maneira consistente de gerenciar dispositivos de áudio gerenciados pelo Windows Media Gerenciador de Dispositivos. Se você criar seu provedor de serviços e componentes de driver de acordo com as diretrizes a seguir, seu dispositivo será exibido no namespace do Shell. Os usuários poderão interagir com o conteúdo do seu dispositivo de maneira consistente no Windows Explorer para executar operações básicas, como copiar, excluir e renomear.

Os seguintes requisitos de Shell para o provedor de serviços e componentes de driver destinam-se a complementar as diretrizes gerais de Gerenciador de Dispositivos de mídia do Windows.

Funcionalidades do dispositivo

Os provedores de serviços do Windows Media Gerenciador de Dispositivos devem ser explícitos em seus recursos com suporte. Se não houver suporte para uma chamada, um código de erro deverá ser retornado. Os campos apropriados devem ser definidos para a presença ou ausência de recursos no retorno das seguintes funções:

-   [**IMDSPStorageGlobals:: GetCapabilities**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [**IMDSPStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

Os provedores de serviços devem dar suporte aos seguintes recursos para serem compatíveis com o Shell:

-   Copiar para o dispositivo (com suporte para retornos de chamada de cancelamento e progresso)
-   Excluir arquivo do dispositivo (com suporte para retornos de chamada de cancelamento e progresso)
-   Renomear arquivo no dispositivo
-   Relatório de espaço (espaço total, espaço livre, espaço inutilizável)
-   Plug and Play (consulte [habilitando PNP para dispositivos](enabling-pnp-for-devices.md))
-   Formato (preferencialmente com suporte para retornos de chamada de cancelamento e progresso)

Se houver suporte para metadados, os campos a seguir deverão ter suporte para arquivos individuais. Se nenhum dado estiver disponível, o campo deverá ser inicializado como uma cadeia de caracteres vazia:



| Campo        | Constante (definida em WMDM. idl) | Marca de metadados    |
|--------------|--------------------------------|-----------------|
| Título da música   | g \_ wszWMDMTitle                | WMDM/título      |
| Número da faixa | g \_ wszWMDMTrack                | WMDM/faixa      |
| Autor       | g \_ wszWMDMAuthor               | WMDM/autor     |
| Álbuns        | g \_ wszWMDMAlbumTitle           | WMDM/campos AlbumTitle |
| Year         | g \_ wszWMDMYear                 | WMDM/ano       |
| Gênero        | g \_ wszWMDMGenre                | WMDM/gênero      |



 

Simultaneidade

Os drivers de modo kernel para Windows Media Gerenciador de Dispositivos precisam ser robustos para lidar com o acesso simultâneo. Por exemplo, um usuário pode acessar simultaneamente o dispositivo por meio do Shell e do Media Player ou simplesmente por meio de várias janelas no Shell. Como parte do tratamento de simultaneidade, os drivers não devem assumir, apenas porque o provedor de serviços está carregado, se o dispositivo está em uso. Em vez disso, eles devem implementar um mecanismo de bloqueio para serializar o acesso ao dispositivo, conforme necessário, para operações individuais.

Interface do usuário

Os provedores de serviço para Windows Media Gerenciador de Dispositivos não devem mostrar nenhuma interface do usuário. Todos os erros devem ser retornados de chamadas de método como códigos de erro específicos do Windows Media Gerenciador de Dispositivos sempre que possível.

Habilitando no Shell

Se o pacote atender a todos os requisitos de Shell, você poderá habilitar seu dispositivo para ser mostrado no Shell definindo o valor *ShowInShell* como 1 nos parâmetros do dispositivo. Para obter mais informações, consulte [parâmetros do dispositivo](device-parameters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um provedor de serviços**](creating-a-service-provider.md)
</dt> </dl>

 

 





---
title: Interfaces para provedores de serviços
description: Interfaces para provedores de serviços
ms.assetid: bd61c5fa-047c-4d93-bae1-f3433696b95b
keywords:
- Windows Gerenciador de Dispositivos de mídia, interfaces de provedor de serviço
- Gerenciador de Dispositivos, interfaces de provedor de serviço
- provedores de serviços, interfaces
- referência de programação, interfaces de provedor de serviço
- referência para Windows de mídia Gerenciador de Dispositivos, interfaces de provedor de serviços
- interfaces de provedor de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a7b178ec0f3ab70f0a133a2286a97e294d449264061681fec540ae9b434c94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766697"
---
# <a name="interfaces-for-service-providers"></a>Interfaces para provedores de serviços

esta seção descreve as interfaces implementadas por Windows provedores de serviços de Gerenciador de Dispositivos de mídia. os provedores de serviço executam a maior parte do trabalho real de comunicação com um dispositivo, pois eles implementam a maioria dos métodos do SDK de Gerenciador de Dispositivos de mídia Windows chamados pelo aplicativo.

Os provedores de serviços não precisam implementar todas as interfaces listadas nesta seção. Por exemplo, um dispositivo de mídia que não tem o armazenamento integrado não implementa as interfaces que são usadas para controlar ou expor conteúdo. Se um método ou interface é necessário é indicado na página de referência apropriada.



| Interface ou classe                                     | Descrição                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CSecureChannelServer](csecurechannelserver-class.md) | Uma classe auxiliar que permite que um provedor de serviços ou provedor de conteúdo seguro autentique um aplicativo e crie assinaturas MAC para parâmetros seguros.                                                                                                                                                         |
| [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)       | fornece ao cliente (geralmente Windows Gerenciador de Dispositivos de mídia) com um enumerador de dispositivo para os dispositivos aos quais esse provedor de serviços dá suporte.                                                                                                                                                                          |
| [**IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)     | Estende o **IMDServiceProvider** fornecendo um método para criar o dispositivo usando o caminho do dispositivo.                                                                                                                                                                                                            |
| [**IMDServiceProvider3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider3)     | Estende o **IMDServiceProvider2** fornecendo um método para definir as preferências de enumeração de dispositivo.                                                                                                                                                                                                             |
| [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)                     | Fornece uma associação baseada em instância com um dispositivo de mídia. Usando essa interface, o cliente pode enumerar os enumeradores de mídia de armazenamento para o dispositivo, obter informações sobre o dispositivo e enviar comandos opacos (passagem) para o dispositivo.                                                                 |
| [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2)                   | Estende o **IMDSPDevice** fornecendo métodos para obter formatos de vídeo estendidos, obter plug and Play (PnP) nomes de dispositivos, habilitar o uso de páginas de propriedades e tornar possível obter um ponteiro para um meio de armazenamento a partir de seu nome. Essa interface é opcional para o provedor de serviços, mas é recomendada. |
| [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)                   | Estende o **IMDSPDevice2** fornecendo a capacidade de consultar Propriedades e recursos do dispositivo em relação a um formato de objeto.                                                                                                                                                                                 |
| [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)       | Fornece métodos para controlar dispositivos.                                                                                                                                                                                                                                                                         |
| [**IMDSPDirectTransfer**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdirecttransfer)     | habilita Windows mídia Gerenciador de Dispositivos para delegar a transferência de conteúdo para o provedor de serviços. nesse caso Windows mídia Gerenciador de Dispositivos não realiza nenhum processamento do conteúdo antes de enviá-lo para o provedor de serviços. O provedor de serviços obtém controle total da origem.                                   |
| [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)             | Enumera os dispositivos de mídia com suporte por este provedor de serviços.                                                                                                                                                                                                                                                  |
| [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)           | Enumera a mídia de armazenamento em um dispositivo e o conteúdo em um meio de armazenamento.                                                                                                                                                                                                                                    |
| [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject)                     | Contém métodos para operações de transferência de dados em um objeto de armazenamento.                                                                                                                                                                                                                                                |
| [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)                   | Estende o **IMDSPObject** fornecendo uma transmissão mais eficiente de dados habilitados para DRM.                                                                                                                                                                                                                             |
| [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)             | Define ou Obtém o comprimento da reprodução, a posição da reprodução, o deslocamento da reprodução ou o comprimento total dos objetos reproduzidos em um meio de armazenamento.                                                                                                                                                                                                    |
| [**IMDSPRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-imdsprevoked)                   | Recupera a URL da qual os componentes atualizados podem ser baixados.                                                                                                                                                                                                                                                |
| [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)                   | Fornece uma associação baseada em instância com um meio de armazenamento em um dispositivo. Essa interface cria objetos de armazenamento, recupera informações sobre eles e fornece acesso à interface **IMDSPEnumStorage** para enumerar subpastas aninhadas no armazenamento atual.                                      |
| [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2)                 | Estende o **IMDSPStorage** obtendo e Configurando atributos estendidos e tornando possível obter um ponteiro para o armazenamento a partir de seu nome.                                                                                                                                                                             |
| [**IMDSPStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3)                 | Estende o **IMDSPStorage2** ao dar suporte a metadados.                                                                                                                                                                                                                                                                 |
| [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)                 | Estende **IMDSPStorage3** ao dar suporte a objetos playlist.                                                                                                                                                                                                                                                         |
| [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals)     | Recupera informações globais sobre um meio de armazenamento, como a quantidade de espaço livre e o número total de arquivos.                                                                                                                                                                                              |



 

O diagrama a seguir mostra como obter as várias interfaces implementadas por um provedor de serviços. Neste diagrama, as interfaces derivadas são exibidas na mesma marca para compactação, portanto, IMDServiceProvider/2/3 representaria três interfaces: **IMDServiceProvider**, **IMDServiceProvider2** e **IMDServiceProvider3**. Os métodos mostrados são estendidos por apenas uma dessas interfaces. Interfaces derivadas são obtidas chamando **QueryInterface** na interface base do objeto criado.

![diagrama mostrando como o Windows Media Device Manager espera adquirir interfaces de um provedor de serviços.](images/wmdm-sp-interfaces.gif)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> <dt>

[**Windows Interfaces de DRM-Implemented de mídia**](windows-media-drm-implemented-interfaces.md)
</dt> </dl>

 

 





---
description: Muitas novas APIs de aquisição de imagem do Windows (WIA) estão incluídas na aquisição de imagens do Windows (WIA) 2,0.
ms.assetid: d8e85c34-d8ce-4512-af71-102a21393fdf
title: O que há de novo na aquisição de imagens do Windows (WIA) 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f9d225185b8f1ff2d6441a7ddf0e8fd919ac98
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105770616"
---
# <a name="whats-new-in-windows-image-acquisition-wia-20"></a>O que há de novo na aquisição de imagens do Windows (WIA) 2,0

Muitas novas APIs de aquisição de imagem do Windows (WIA) estão incluídas na aquisição de imagens do Windows (WIA) 2,0. Além disso, há algumas incompatibilidades posteriores e regressivas entre o WIA (Windows Image Acquisition) 1,0 e o serviço WIA 2,0 fornecido com o Windows Vista. Algumas interfaces, estruturas, propriedades e valores de Propriedade do WIA 1,0 não são suportados pelo, e os aplicativos que os utilizam não serão executados no, no Windows Vista e posterior. Da mesma forma, os aplicativos que usam as novas interfaces, estruturas, propriedades e valores de propriedade introduzidos com a WIA 2,0 (veja abaixo) não serão executados em versões do sistema operacional anteriores ao Windows Vista.

## <a name="new-api-for-wia-20"></a>Nova API para WIA 2,0

### <a name="constants-lists-updated-for-wia-20"></a>Constantes: listas atualizadas para o WIA 2,0

-   [**Constantes de propriedade de item WIA comuns**](-wia-wiaitempropcommonitem.md)
-   [**Constantes da propriedade de informações do dispositivo**](-wia-wiadeviceinfoprop.md)
-   [**Constantes de propriedade de dispositivo do scanner**](-wia-wiaitempropscannerdevice.md)
-   [**Constantes da propriedade item do scanner WIA**](-wia-wiaitempropscanneritem.md)
-   [**GUIDs de categoria de item WIA 2,0**](-wia-wia2-itemcategoryguids.md)
-   [**Constantes de tamanho de página WIA 2,0**](-wia-wia2-pagesizeconstants.md)
-   [**Sinalizadores de tipo de item WIA**](-wia-wia-item-type-flags.md)

### <a name="new-structures-in-wia-20"></a>Novas estruturas no WIA 2,0



| Tópico                                               | Sumário                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) | Define os dados necessários para chamar uma caixa de diálogo de dispositivo.<br/>                                                                                                                                                                                                       |
| [**\_cabeçalho bruto \_ WIA**](-wia-wia-raw-header.md)     | A estrutura de [**\_ \_ cabeçalho bruto do WIA**](-wia-wia-raw-header.md) define uma imagem no formato de dados brutos de um dispositivo e permite que os aplicativos usem o formato bruto em transferências WIA.<br/>                                                                         |
| [**WiaTransferParams**](-wia-wiatransferparams.md) | O [**WiaTransferParams**](-wia-wiatransferparams.md) é transmitido para um aplicativo durante uma transferência de dados pelo sistema de tempo de execução WIA para o método [**IWiaTransferCallback:: TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) .<br/> |



 

### <a name="new-interfaces-in-wia-20"></a>Novas interfaces no WIA 2,0



| Tópico                                                         | Sumário                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)                   | Usado por aplicativos para enumerar objetos [**IWiaItem2**](-wia-iwiaitem2.md) na pasta atual da árvore de itens.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfile**](-wia-iscanprofile.md)                     | A interface [**IScanProfile**](-wia-iscanprofile.md) representa um único perfil de verificação e permite que os aplicativos definam e obtenham as propriedades do perfil. <br/>                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfileMgr**](-wia-iscanprofilemgr.md)               | A interface [**IScanProfileMgr**](-wia-iscanprofilemgr.md) fornece métodos para criar, abrir, excluir e gerenciar perfis de verificação. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IScanProfileUI**](-wia-iscanprofileui.md)                 | A interface [**IScanProfileUI**](-wia-iscanprofileui.md) permite que os aplicativos exibam uma caixa de diálogo para que os usuários possam criar, modificar e excluir perfis de verificação.<br/>                                                                                                                                                                                                                                                                                                                               |
| [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md)       | A interface [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md) permite que os aplicativos exibam janelas de erro (durante transferências de dados) da qual o usuário pode escolher se deseja continuar, cancelar ou anular a transferência.<br/>                                                                                                                                                                                                                                                                     |
| [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)                       | A interface [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) é usada para criar e gerenciar dispositivos de aquisição de imagem e para se registrar para receber eventos de dispositivo.<br/>                                                                                                                                                                                                                                                                                                                                             |
| [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)             | A interface [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md) fornece métodos para lidar com erros que podem ocorrer quando um aplicativo solicita dados de imagem, seja para os bits de visualização ou final. <br/>                                                                                                                                                                                                                                                                                                      |
| [**IWiaImageFilter**](-wia-iwiaimagefilter.md)               | A interface [**IWiaImageFilter**](-wia-iwiaimagefilter.md) é uma interface de extensão implementada por desenvolvedores de filtro de processamento de imagens e chamada pelo WIA 2,0. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**IWiaItem2**](-wia-iwiaitem2.md)                           | A interface [**IWiaItem2**](-wia-iwiaitem2.md) fornece aplicativos com a mesma funcionalidade que a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (a capacidade de consultar dispositivos para descobrir seus recursos, acessar interfaces de transferência de dados e propriedades de item e controlar o dispositivo). Ele também fornece ao aplicativo a capacidade de criar e usar dinamicamente filtros de processamento de imagens que podem vir como extensões dos drivers de dispositivo WIA 2,0 fornecidos no Windows Vista.<br/> |
| [**IWiaPreview**](-wia-iwiapreview.md)                       | A interface [**IWiaPreview**](-wia-iwiapreview.md) armazena em cache as imagens não filtradas internamente e as passa por filtros de processamento de imagem. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) | A interface [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) detecta as subregiãos de um fluxo de imagem e torna itens [**IWiaItem2**](-wia-iwiaitem2.md) separados para cada um. <br/>                                                                                                                                                                                                                                                                                                         |
| [**IWiaTransfer**](-wia-iwiatransfer.md)                     | A interface [**IWiaTransfer**](-wia-iwiatransfer.md) fornece transferência de dados baseada em fluxo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)     | A interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) recebe retornos de chamada durante uma transferência de dados. <br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**IWiaUIExtension2**](-wia-iwiauiextension2.md)             | A interface IWiaUIExtension2 fornece métodos que substituem a interface do usuário padrão fornecida pelo sistema por uma interface do usuário personalizada e que fornecem um ícone de dispositivo personalizado. Os fornecedores de dispositivos podem implementar essa interface para fornecer interfaces de usuário personalizadas para seus dispositivos.<br/>                                                                                                                                                                                                                     |



 

### <a name="new-and-changed-overviews-for-wia-20"></a>Visões gerais novas e alteradas para o WIA 2,0



| Tópico                                                                          | Sumário |
|--------------------------------------------------------------------------------|----------|
| [Constantes](-wia-constants.md)                                                |          |
| [Funções](-wia-functions.md)                                                |          |
| [Interfaces](-wia-interfaces.md)                                              |          |
| [Esquema do perfil de verificação](-wia-scan-profile-schema.md)                            |          |
| [Estruturas](-wia-structures.md)                                              |          |
| [Transferindo dados de imagem no WIA 2,0](-wia-transferring-image-data-in-wia2.md) |          |
| [Especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md)              |          |
| [Constantes da propriedade WIA](-wia-wia-property-constants.md)                      |          |



 

## <a name="leave-feedback"></a>Deixar comentários

Email **sdkfdbk@microsoft.com** para fazer solicitações de recursos e relatórios de erros diretamente para a Microsoft.

 

 





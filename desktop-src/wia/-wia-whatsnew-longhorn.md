---
description: Muitas novas Windows API wia (aquisição de imagem) estão incluídas no WIA (Aquisição de Imagem) 2.0 do Windows.
ms.assetid: d8e85c34-d8ce-4512-af71-102a21393fdf
title: Novidades na wia (aquisição Windows imagem) 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fef5fdc2f70c7b0a7c25e3e9df68b82d05b7fd1a53eb7ec3613962f975e5c1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592946"
---
# <a name="whats-new-in-windows-image-acquisition-wia-20"></a>Novidades na wia (aquisição Windows imagem) 2.0

Muitas novas Windows API wia (aquisição de imagem) estão incluídas no WIA (Aquisição de Imagem) 2.0 do Windows. Além disso, há algumas incompatibilidades para frente e para trás entre o WIA (Aquisição de Imagem) 1.0 do Windows e o serviço WIA 2.0 que acompanha o Windows Vista. Algumas interfaces, estruturas, propriedades e valores de propriedade do WIA 1.0 não são suportados pelo e os aplicativos que os usam não serão executados no Windows Vista e posterior. Da mesma forma, os aplicativos que usam as novas interfaces, estruturas, propriedades e valores de propriedade introduzidos com o WIA 2.0 (veja abaixo) não serão executados em versões do sistema operacional anteriores ao Windows Vista.

## <a name="new-api-for-wia-20"></a>Nova API para WIA 2.0

### <a name="constants-lists-updated-for-wia-20"></a>Constantes: listas atualizadas para WIA 2.0

-   [**Constantes comuns de propriedade de item WIA**](-wia-wiaitempropcommonitem.md)
-   [**Constantes de propriedade de informações do dispositivo**](-wia-wiadeviceinfoprop.md)
-   [**Constantes de propriedade do dispositivo do scanner**](-wia-wiaitempropscannerdevice.md)
-   [**Constantes de propriedade de item WIA do scanner**](-wia-wiaitempropscanneritem.md)
-   [**GUIDs da categoria de item WIA 2.0**](-wia-wia2-itemcategoryguids.md)
-   [**Constantes de tamanho de página WIA 2.0**](-wia-wia2-pagesizeconstants.md)
-   [**Sinalizadores de tipo de item WIA**](-wia-wia-item-type-flags.md)

### <a name="new-structures-in-wia-20"></a>Novas estruturas no WIA 2.0



| Tópico                                               | Sumário                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) | Define os dados necessários para chamar uma caixa de diálogo do dispositivo.<br/>                                                                                                                                                                                                       |
| [**HEADER \_ RAW DO WIA \_**](-wia-wia-raw-header.md)     | A [**estrutura \_ DE \_ HEADER RAW**](-wia-wia-raw-header.md) do WIA define uma imagem no formato de dados RAW de um dispositivo e permite que os aplicativos usem o formato RAW em transferências WIA.<br/>                                                                         |
| [**WiaTransferParams**](-wia-wiatransferparams.md) | O [**WiaTransferParams**](-wia-wiatransferparams.md) é transmitido para um aplicativo durante uma transferência de dados pelo sistema de tempo de executar WIA para o [**método IWiaTransferCallback::TransferCallback.**](-wia-iwiatransfercallback-transfercallback.md)<br/> |



 

### <a name="new-interfaces-in-wia-20"></a>Novas interfaces no WIA 2.0



| Tópico                                                         | Sumário                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)                   | Usado por aplicativos para enumerar [**objetos IWiaItem2**](-wia-iwiaitem2.md) na pasta atual da árvore de itens.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfile**](-wia-iscanprofile.md)                     | A interface [**IScanProfile**](-wia-iscanprofile.md) representa um único perfil de verificação e permite que os aplicativos de definir e obter as propriedades do perfil. <br/>                                                                                                                                                                                                                                                                                                                                   |
| [**IScanProfileMgr**](-wia-iscanprofilemgr.md)               | A interface [**IScanProfileMgr**](-wia-iscanprofilemgr.md) fornece métodos para criar, abrir, excluir e gerenciar perfis de verificação. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IScanProfileUI**](-wia-iscanprofileui.md)                 | A interface [**IScanProfileUI**](-wia-iscanprofileui.md) permite que os aplicativos excluam uma caixa de diálogo para que os usuários possam criar, modificar e excluir perfis de verificação.<br/>                                                                                                                                                                                                                                                                                                                               |
| [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md)       | A interface [**IWiaAppErrorHandler**](-wia-iwiaapperrorhandler.md) permite que os aplicativos exibem janelas de erro (durante transferências de dados) das quais o usuário pode optar por continuar, cancelar ou anular a transferência.<br/>                                                                                                                                                                                                                                                                     |
| [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)                       | A interface [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) é usada para criar e gerenciar dispositivos de aquisição de imagem e para se registrar para receber eventos de dispositivo.<br/>                                                                                                                                                                                                                                                                                                                                             |
| [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)             | A interface [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md) fornece métodos para tratar erros que podem ocorrer quando um aplicativo solicita dados de imagem, seja para bits de versão prévia ou final. <br/>                                                                                                                                                                                                                                                                                                      |
| [**IWiaImageFilter**](-wia-iwiaimagefilter.md)               | A interface [**IWiaImageFilter**](-wia-iwiaimagefilter.md) é uma interface de extensão implementada pelos desenvolvedores de filtro de processamento de imagem e chamada pelo WIA 2.0. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**IWiaItem2**](-wia-iwiaitem2.md)                           | A interface [**IWiaItem2**](-wia-iwiaitem2.md) fornece aplicativos com a mesma funcionalidade que a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (a capacidade de consultar dispositivos para descobrir seus recursos, acessar interfaces de transferência de dados e propriedades de item e controlar o dispositivo). Ele também fornece ao aplicativo a capacidade de criar e usar dinamicamente filtros de processamento de imagem que podem vir como extensões dos drivers de dispositivo WIA 2.0 fornecidos no Windows Vista.<br/> |
| [**IWiaPreview**](-wia-iwiapreview.md)                       | A interface [**IWiaPreview**](-wia-iwiapreview.md) armazena em cache imagens não filtradas internamente e as passa por filtros de processamento de imagem. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) | A interface [**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md) detecta sub-regiões de um fluxo de imagem e faz itens [**IWiaItem2**](-wia-iwiaitem2.md) separados para cada um. <br/>                                                                                                                                                                                                                                                                                                         |
| [**IWiaTransfer**](-wia-iwiatransfer.md)                     | A interface [**IWiaTransfer**](-wia-iwiatransfer.md) fornece transferência de dados baseada em fluxo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)     | A interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) recebe retornos de chamada durante uma transferência de dados. <br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**IWiaUIExtension2**](-wia-iwiauiextension2.md)             | A interface IWiaUIExtension2 fornece métodos que substituem a interface do usuário padrão fornecida pelo sistema por uma interface do usuário personalizada e que fornecem um ícone de dispositivo personalizado. Os fornecedores de dispositivos podem implementar essa interface para fornecer interfaces de usuário personalizadas para seus dispositivos.<br/>                                                                                                                                                                                                                     |



 

### <a name="new-and-changed-overviews-for-wia-20"></a>Visão geral novas e alteradas do WIA 2.0



| Tópico                                                                          | Sumário |
|--------------------------------------------------------------------------------|----------|
| [Constantes](-wia-constants.md)                                                |          |
| [Funções](-wia-functions.md)                                                |          |
| [Interfaces](-wia-interfaces.md)                                              |          |
| [Esquema de perfil de verificação](-wia-scan-profile-schema.md)                            |          |
| [Estruturas](-wia-structures.md)                                              |          |
| [Transferindo dados de imagem no WIA 2.0](-wia-transferring-image-data-in-wia2.md) |          |
| [Especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md)              |          |
| [Constantes de propriedade WIA](-wia-wia-property-constants.md)                      |          |



 

## <a name="leave-feedback"></a>Deixe comentários

Email para fazer relatórios **sdkfdbk@microsoft.com** de erros e solicitações de recursos diretamente para a Microsoft.

 

 





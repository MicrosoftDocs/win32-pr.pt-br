---
title: Funções WIC
description: Esta seção contém informações sobre as funções Windows WIC (componente de imagens de dados).
ms.assetid: 6f948df6-5b70-4f1e-b01d-3841d7819acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f60660780e97831a77101c15646385d62048f005279b388a532ca687a200996
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056796"
---
# <a name="wic-functions"></a>Funções WIC

Esta seção contém informações sobre as funções Windows WIC (componente de imagens de dados).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                      | Descrição                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*ProgressNotificationCallback*](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)<br/>   | Função de retorno de chamada definida pelo aplicativo chamada quando o progresso do componente codec é feito.<br/>                                                                                                                        |
| [**WICConvertBitmapSource**](/windows/desktop/api/Wincodec/nf-wincodec-wicconvertbitmapsource)<br/>             | Obtém um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) no formato de pixel desejado de um **determinado IWICBitmapSource.**<br/>                                                                           |
| [**WICCreateBitmapFromSection**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsection)<br/>     | Retorna um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que é apoiado pelos pixels de um Windows Graphics Device Interface de seção (GDI).<br/>                                                |
| [**WICCreateBitmapFromSectionEx**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsectionex)<br/> | Retorna um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que é apoiado pelos pixels de um alça de seção GDI.<br/>                                                                                    |
| [**WICGetMetadataContentSize**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicgetmetadatacontentsize)<br/>       | Retorna o tamanho do conteúdo de metadados contido pelo [**IWICMetadataWriter especificado.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) O tamanho retornado conta para o header e o comprimento dos metadados.<br/> |
| [**WICMapGuidToShortName**](/windows/desktop/api/WinCodec/nf-wincodec-wicmapguidtoshortname)<br/>               | Obtém o nome curto associado a um determinado GUID.<br/>                                                                                                                                                       |
| [**WICMapSchemaToName**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapschematoname)<br/>                     | Obtém o nome associado a um determinado esquema.<br/>                                                                                                                                                           |
| [**WICMapShortNameToGuid**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapshortnametoguid)<br/>               | Obtém o GUID associado ao nome curto determinado.<br/>                                                                                                                                                     |
| [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)<br/>           | Obtém um GUID de formato de metadados para um formato de contêiner e fornecedor especificados que melhor corresponde ao conteúdo dentro de um determinado fluxo.<br/>                                                                            |
| [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent)<br/>   | Grava metadados em um determinado fluxo.<br/>                                                                                                                                                                       |
| [Funções de proxy WIC](wic-proxy-functions.md)<br/>                                  | Esta seção contém as funções de proxy WIC.<br/>                                                                                                                                                             |



 

 

 





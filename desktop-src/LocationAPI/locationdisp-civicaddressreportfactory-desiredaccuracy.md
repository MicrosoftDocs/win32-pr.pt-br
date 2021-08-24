---
description: Propriedade LocationDisp.CivicAddressReportFactory.DesiredAccuracy – o valor de precisão desejada atual.
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: Propriedade LocationDisp.CivicAddressReportFactory.DesiredAccuracy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca2d4f4a7be4afa800cfe81b5df7396be579197e7f997019f4ece3a39598c975
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693126"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a>Propriedade LocationDisp.CivicAddressReportFactory.DesiredAccuracy

\[O modelo de objeto da API de Localização está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de Geolocalização do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo da área de trabalho, use o [**Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

O valor de precisão desejada atual.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade é um ULONG de **leitura/gravação.**



| Valor                                                                        | Significado                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Padrão. O sensor deve usar a precisão para a qual ele pode otimizar o uso de energia e outras considerações de custo.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | O sensor deve fornecer o relatório mais preciso possível. Isso inclui usar serviços que podem cobrar dinheiro ou consumir níveis mais altos de energia da bateria ou largura de banda da conexão.<br/> |



 

## <a name="remarks"></a>Comentários

Esse valor é uma solicitação para o provedor de localização. O provedor de localização não é necessário para fornecer a precisão solicitada. Leia o valor dessa propriedade para descobrir a configuração de precisão verdadeira.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 


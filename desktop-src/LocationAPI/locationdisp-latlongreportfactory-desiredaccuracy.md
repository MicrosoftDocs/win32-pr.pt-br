---
description: Propriedade LocationDisp. LatLongReportFactory. DesiredAccuracy-o valor de precisão desejado atual.
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: Propriedade LocationDisp. LatLongReportFactory. DesiredAccuracy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3deccb2dcc71a62b64a508e55759e5cc9c00b5cb0a7a59fb3390046371d2fac4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129846"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a>Propriedade LocationDisp. LatLongReportFactory. DesiredAccuracy

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use o [**Windows. API de dispositivos. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

O valor de precisão desejado atual.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Valor da propriedade

Esta propriedade é um **ULONG** de leitura/gravação.



| Valor                                                                        | Significado                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Padrão. O sensor deve usar a precisão para a qual ele pode otimizar o uso de energia e outras considerações de custo.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | O sensor deve fornecer o relatório mais preciso possível. Isso inclui usar serviços que podem cobrar dinheiro ou consumir níveis mais altos de energia da bateria ou largura de banda da conexão.<br/> |



 

## <a name="remarks"></a>Comentários

Esse valor é uma solicitação para o provedor de localização. O provedor de localização não é necessário para fornecer relatórios no intervalo solicitado. Leia o valor dessa propriedade para descobrir a configuração real do intervalo de relatório.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 


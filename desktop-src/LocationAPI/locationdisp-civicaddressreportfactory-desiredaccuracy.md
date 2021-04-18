---
description: O valor de precisão desejado atual.
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: Propriedade LocationDisp. CivicAddressReportFactory. DesiredAccuracy
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
ms.openlocfilehash: eb05aeb6a69bfe978682d418cf1e71aed2184bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753461"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a>Propriedade LocationDisp. CivicAddressReportFactory. DesiredAccuracy

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

O valor de precisão desejado atual.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Valor da propriedade

Esta propriedade é um **ULONG** de leitura/gravação.



| Valor                                                                        | Significado                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Padrão. O sensor deve usar a precisão para a qual ele pode otimizar o uso de energia e outras considerações de custo.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | O sensor deve fornecer o relatório mais preciso possível. Isso inclui usar serviços que podem cobrar dinheiro ou consumir níveis mais altos de energia da bateria ou largura de banda da conexão.<br/> |



 

## <a name="remarks"></a>Comentários

Esse valor é uma solicitação para o provedor de localização. O provedor de localização não é necessário para fornecer a precisão solicitada. Leia o valor dessa propriedade para descobrir a configuração de precisão real.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 


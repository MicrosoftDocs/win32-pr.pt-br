---
description: Erro de altitude, em metros.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: Propriedade LocationDisp. DispLatLongReport. AltitudeError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.AltitudeError
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8d84c09a143808302a623ab7b098a105ef74ee4ad7aecfe3a4a172b765fcbdfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809522"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a>Propriedade LocationDisp. DispLatLongReport. AltitudeError

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use o [**Windows. API de dispositivos. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

Erro de altitude, em metros.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade é um **número** somente leitura (ponto flutuante de precisão dupla).

## <a name="remarks"></a>Comentários

Os sensores de localização não são necessários para fornecer essa propriedade. Você deve tratar exceções ao tentar acessar essa propriedade.

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar essa propriedade, consulte [um exemplo de relatório simples de LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 


---
description: Altitude atual, em metros. Altitude é relativa ao elipsoide de referência.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: Propriedade LocationDisp. DispLatLongReport. altitude
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2004c8df6c61fb890bf8f71fb3c2b5446d71d79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828569"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a>Propriedade LocationDisp. DispLatLongReport. altitude

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

Altitude atual, em metros. Altitude é relativa ao elipsoide de referência.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade é um **número** somente leitura (ponto flutuante de precisão dupla).

## <a name="remarks"></a>Comentários

Os sensores de localização não são necessários para fornecer essa propriedade. Você deve tratar exceções ao tentar acessar essa propriedade.

O método **altitude** recupera a altitude relativa ao elipsoide de referência que é definido pela revisão mais recente do sistema geodésico (WGS 84), em vez da altitude em relação ao nível do Sea.

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar essa propriedade, consulte [um exemplo de relatório simples de LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 


---
description: Propriedade LocationDisp. DispLatLongReport. Timestamp-a data e a hora em que o relatório foi gerado.
ms.assetid: 3b8036aa-499c-4baf-bcc4-5b6c3f54eb7b
title: Propriedade LocationDisp. DispLatLongReport. Timestamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: fd505f967bad31afa908609a72d108b17552fce8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105684"
---
# <a name="locationdispdisplatlongreporttimestamp-property"></a>Propriedade LocationDisp. DispLatLongReport. Timestamp

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

A data e a hora em que o relatório foi gerado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
Timestamp = LocationDisp.DispLatLongReport.Timestamp
```



## <a name="property-value"></a>Valor da propriedade

Esta propriedade é uma **Data** somente leitura. Os carimbos de data/hora são fornecidos como UTC (tempo Universal Coordenado).

## <a name="remarks"></a>Comentários

Observe que as linguagens de script, como o Microsoft JScript, podem exigir que você execute conversões para outros formatos de tempo ao exibir carimbos de data/hora como cadeias de caracteres.

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar essa propriedade, consulte [um exemplo de relatório simples de LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 


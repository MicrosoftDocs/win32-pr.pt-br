---
description: Propriedade LocationDisp. DispCivicAddressReport. Timestamp-a data e a hora em que o relatório foi gerado.
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: Propriedade LocationDisp. DispCivicAddressReport. Timestamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 12388706c0b8e9205f398ec259314ab05ff5fe1c062f4b8920d610b7d74b36f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129986"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a>Propriedade LocationDisp. DispCivicAddressReport. Timestamp

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use o [**Windows. API de dispositivos. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

A data e a hora em que o relatório foi gerado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a>Valor da propriedade

Esta propriedade é uma **Data** somente leitura. Os carimbos de data/hora são fornecidos como UTC (tempo Universal Coordenado).

## <a name="remarks"></a>Comentários

observe que as linguagens de script, como o Microsoft JScript, podem exigir que você execute conversões para outros formatos de tempo ao exibir carimbos de data/hora como cadeias de caracteres.

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar essa propriedade, consulte [um exemplo de relatório de endereço cívico simples](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 


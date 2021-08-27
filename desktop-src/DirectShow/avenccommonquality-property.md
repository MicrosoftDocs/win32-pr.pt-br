---
description: Especifica o nível de qualidade para codificação.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Propriedade AVEncCommonQuality (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99202391e919fa1da9028a15a57154834feddd3039160b9b0562a713fe59ddaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087666"
---
# <a name="avenccommonquality-property"></a>Propriedade AVEncCommonQuality

Especifica o nível de qualidade para codificação.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonQuality**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade tem o seguinte intervalo.



| Valor | Descrição                           |
|-------|---------------------------------------|
| 0     | Qualidade mínima, tamanho de saída menor. |
| 100   | Qualidade máxima, tamanho de saída maior.  |



 

## <a name="remarks"></a>Comentários

Essa propriedade controla o nível de qualidade quando o codificador não está usando uma taxa de bits restrita. A propriedade [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) determina se a taxa de bits está restrita.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 





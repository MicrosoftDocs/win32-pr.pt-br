---
description: Especifica o aumento de baixo nível quando o decodificador executa o controle de intervalo dinâmico em um fluxo de áudio Dolby AC-3.
ms.assetid: d723c825-f2f1-4ba0-a667-8285009764fd
title: Propriedade AVDecDDDynamicRangeScaleLow (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91773eb20f3d0714223877acba4f26b01503202fc87f9f7b97dcde60ab99512e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586736"
---
# <a name="avdecdddynamicrangescalelow-property"></a>Propriedade AVDecDDynamicRangeScaleLow

Especifica o aumento de baixo nível quando o decodificador executa o controle de intervalo dinâmico em um fluxo de áudio Dolby AC-3.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecDDDynamicRangeScaleLow**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade tem o intervalo a seguir.



| Valor | Descrição                                                    |
|-------|----------------------------------------------------------------|
| 0     | Nenhuma compactação de intervalo dinâmico. Preservar o intervalo dinâmico completo. |
| 100   | Aplicar compactação de intervalo dinâmico completa.                          |



 

## <a name="remarks"></a>Comentários

Essa propriedade se aplica somente quando o valor da propriedade [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) é eAVDecDDOperationalMode \_ LINE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 





---
description: Especifica o corte de alto nível quando o decodificador executa o controle de intervalo dinâmico em um fluxo de áudio Dolby AC-3.
ms.assetid: 8771a5f9-878b-43fd-8eaa-0bfc276194aa
title: Propriedade AVDecDDDynamicRangeScaleHigh (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521cd631d92db73f23c7018adeda9bd321d23c1a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456764"
---
# <a name="avdecdddynamicrangescalehigh-property"></a>Propriedade AVDecDDDynamicRangeScaleHigh

Especifica o corte de alto nível quando o decodificador executa o controle de intervalo dinâmico em um fluxo de áudio Dolby AC-3.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecDDDynamicRangeScaleHigh**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade tem o seguinte intervalo.



| Valor | Descrição                                                    |
|-------|----------------------------------------------------------------|
| 0     | Sem compactação de intervalo dinâmico. Preserve o intervalo dinâmico completo. |
| 100   | Aplicar compactação completa de intervalo dinâmico.                          |



 

## <a name="remarks"></a>Comentários

Essa propriedade aplica-se somente quando o valor da propriedade [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) é eAVDecDDOperationalMode \_ linha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 





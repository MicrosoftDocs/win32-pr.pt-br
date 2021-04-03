---
description: Especifica o aumento de nível baixo quando o decodificador executa o controle de intervalo dinâmico em um fluxo de áudio Dolby AC-3.
ms.assetid: d723c825-f2f1-4ba0-a667-8285009764fd
title: Propriedade AVDecDDDynamicRangeScaleLow (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b68b1d4376d9ba15859be943ded23458fe16d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010050"
---
# <a name="avdecdddynamicrangescalelow-property"></a>Propriedade AVDecDDDynamicRangeScaleLow

Especifica o aumento de nível baixo quando o decodificador executa o controle de intervalo dinâmico em um fluxo de áudio Dolby AC-3.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecDDDynamicRangeScaleLow**

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

 

 





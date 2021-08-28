---
description: Especifica o número máximo de quadros LTR (Referência de Longo Prazo) controlados pelo aplicativo.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: CODECAPI_AVEncVideoLTRBufferControl propriedade (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cca2e24e8295969609ba325a2abf24be76fb07c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481922"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>Propriedade CODECAPI \_ AVEncVideoLTRBufferControl

Especifica o número máximo de quadros LTR (Referência de Longo Prazo) controlados pelo aplicativo.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoLTRBufferControl**

## <a name="property-value"></a>Valor da propriedade

O valor desse controle inclui dois campos, em que cada campo tem 16 bits.




| Valor | Significado | 
|-------|---------|
| <span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl><dt><strong>O primeiro campo</strong></dt><dt>Bits[0..15]</dt></dl> | O número de quadros LTR controlados pelo aplicativo.<br /><strong>Codificadores H.264/AVC:</strong><br /> Supondo que o valor seja N e N seja um valor não zero, em cada quadro IDR, o codificador deverá marcar automaticamente os quadros após o quadro de IDR (e incluindo o quadro IDR) como quadros LTR, desde que todos os três dos seguintes valores se apliquem:<ul><li>O quadro ainda não está definido para ser marcado como um quadro de referência de longo prazo.</li><li>O quadro é um quadro de camada base. Por exemplo, o elemento de <strong>sintaxe temporal_id</strong> igual a 0.</li><li>O número de quadros atualmente marcados como LTR é menor que N.</li></ul><br /> | 
| <span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl><dt><strong>O segundo campo</strong></dt><dt>Bits[16..31]</dt></dl> | O modo de confiança do controle LTR.<br /><strong>Codificadores H.264/AVC:</strong><br /> 1 (Confiar até) significa que o codificador pode usar um quadro LTR, a menos que o aplicativo o invalide explicitamente por meio do <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> controle. <br /> Outros valores são inválidos e reservados para uso futuro.<br /> | 




 

## <a name="remarks"></a>Comentários

Essa é uma API estática.

O valor padrão deve ser 0

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Aplicativos UWP de aplicativos da área \[ de trabalho \| R2\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 





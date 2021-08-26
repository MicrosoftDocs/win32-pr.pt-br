---
description: Especifica que o quadro atual é codificado usando um ou vários quadros LTR.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: CODECAPI_AVEncVideoUseLTRFrame propriedade (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c438a4e6e2656c5e952062d9e3c1c0000899f2c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473152"
---
# <a name="codecapi_avencvideouseltrframe-property"></a>Propriedade CODECAPI \_ AVEncVideoUseLTRFrame

Especifica que o quadro atual é codificado usando um ou vários quadros LTR.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoUseLTRFrame**

## <a name="property-value"></a>Valor da propriedade

O valor desse controle inclui dois campos, em que cada campo tem 16 bits.




| Valor | Significado | 
|-------|---------|
| <span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl><dt><strong>O primeiro campo</strong></dt><dt>Bits[0..15]</dt></dl> | Indica quais quadros LTR são permitidos para codificar o quadro atual. <br /><strong>Codificadores H.264/AVC:</strong><br /> Este é um bitmap que indica quais quadros LTR podem ser usados como referência para esse quadro. O bit menos significativo corresponde ao índice LTR 0, o segundo bit menos significativo corresponde ao índice LTR 1 etc.<br /> Esse valor não deve ser 0.<br /> O índice mais alto especificado por esse valor não deve ser maior que o número máximo de quadros LTR especificado na propriedade <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> menos um.<br /> | 
| <span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl><dt><strong>O segundo campo</strong></dt><dt>Bits[16..31]</dt></dl> | Sinalizador que indica se são necessárias limitações adicionais para codificar quadros subsequentes. <br /><strong>Codificadores H.264/AVC:</strong><br /> 1 está no único valor válido para esse campo. Todos os outros valores são inválidos e reservados para uso futuro.<br /> Quando o sinalizador for 1, o codificador deverá codificar quadros subsequentes na ordem de codificação sujeitos às seguintes restrições:<br /><ul><li>Ele não deve usar quadros de referência de curto prazo na ordem de codificação mais antigas do que o quadro atual ou codificação futura na ordem de codificação.</li><li>Ele não deve usar quadros LTR não descritos pelo controle de CODECAPI_AVEncVideoUseLTRFrame mais recente.</li><li>Ele pode usar quadros LTR atualizados após o quadro atual.</li></ul> | 




 

## <a name="remarks"></a>Comentários

**Codificadores H.264/AVC:**

Essa propriedade não deverá ser chamada se uma chamada pendente para usar um quadro LTR tiver sido emitida usando a propriedade CODECAPI AVEncVideoUseLTRFrame e o codificador ainda não tiver gerado um quadro que tenha usado o \_ LTR. Em outras palavras, o codificador não deve enfileirar solicitações \_ CODECAPI AVEncVideoUseLTRFrame.

Se uma solicitação CODECAPI AVEncVideoUseLTRFrame for enviada enquanto outra solicitação \_ CODECAPI AVEncVideoUseLTRFrame ainda estiver pendente, a solicitação mais antiga deverá \_ ser retirada.

Chamar CODECAPI AVEncVideoUseLTRFrame em um quadro de camada não base é válido e deve se aplicar ao quadro de camada não base, sem atraso em um quadro de camada \_ base.

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

 

 





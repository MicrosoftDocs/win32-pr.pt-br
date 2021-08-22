---
description: Especifica que o quadro atual é codificado usando um ou vários quadros EPD.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: Propriedade CODECAPI_AVEncVideoUseLTRFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b4df79755ed03873f0393d93f7e21ab8046af6295309207dc976f87eb0ee99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743802"
---
# <a name="codecapi_avencvideouseltrframe-property"></a>\_Propriedade CODECAPI AVEncVideoUseLTRFrame

Especifica que o quadro atual é codificado usando um ou vários quadros EPD.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoUseLTRFrame**

## <a name="property-value"></a>Valor da propriedade

O valor desse controle inclui dois campos, onde cada campo tem 16 bits.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <dt><strong>O primeiro bits de campo</strong></dt> <dt>[0.. 15]</dt> </dl></td>
<td>Indica quais quadros EPD são permitidos para codificar o quadro atual. <br/> <strong>Codificadores H. 264/AVC:</strong><br/> Este é um bitmap que indica quais quadros EPD podem ser usados como uma referência para esse quadro. O bit menos significativo corresponde ao índice LTR 0, o segundo bit menos significativo corresponde ao índice EPD 1, etc.<br/> Esse valor não deve ser 0.<br/> O índice mais alto especificado por esse valor não deve ser maior que o número máximo de quadros EPD especificados na propriedade <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> menos um.<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>O segundo campo</strong></dt> <dt>bits [16.. 31]</dt> </dl></td>
<td>Sinalizador que indica se são necessárias limitações adicionais para a codificação de quadros subsequentes. <br/> <strong>Codificadores H. 264/AVC:</strong><br/> 1 está no único valor válido para este campo. Todos os outros valores são inválidos e reservados para uso futuro.<br/> Quando o sinalizador for 1, o codificador deverá codificar os quadros subsequentes na ordem de codificação, sujeito às seguintes restrições:<br/>
<ul>
<li>Ele não deve usar quadros de referência de curto prazo na ordem de codificação mais antiga do que o quadro atual ou a codificação futura na ordem de codificação.</li>
<li>Ele não deve usar quadros LTR não descritos pelo controle de CODECAPI_AVEncVideoUseLTRFrame mais recente.</li>
<li>Ele pode usar quadros LTR atualizados após o quadro atual.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

**Codificadores H. 264/AVC:**

Esta propriedade não deverá ser chamada se uma chamada pendente para usar um quadro EPD tiver sido emitida usando a \_ Propriedade CODECAPI AVEncVideoUseLTRFrame e o codificador ainda não tiver gerado um quadro que tenha usado o ltr. Em outras palavras, o codificador não deve enfileirar \_ as solicitações CODECAPI AVEncVideoUseLTRFrame.

Se uma \_ solicitação CODECAPI AVEncVideoUseLTRFrame for enviada enquanto outra \_ solicitação AVEncVideoUseLTRFrame CODECAPI ainda estiver pendente, a solicitação mais antiga deverá ser descartada.

Chamar CODECAPI \_ AVEncVideoUseLTRFrame em um quadro de camada não base é válido e deve ser aplicado ao quadro de camada não base, sem atraso em um quadro de camada de base.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Aplicativos de aplicativos UWP da área de trabalho R2 \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 





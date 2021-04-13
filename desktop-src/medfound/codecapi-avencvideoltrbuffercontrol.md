---
description: Especifica o número máximo de quadros de referência de longo prazo (LTR) controlados pelo aplicativo.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: Propriedade CODECAPI_AVEncVideoLTRBufferControl (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501195"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>\_Propriedade CODECAPI AVEncVideoLTRBufferControl

Especifica o número máximo de quadros de referência de longo prazo (LTR) controlados pelo aplicativo.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoLTRBufferControl**

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
<td>O número de quadros LTR controlados pelo aplicativo.<br/> <strong>Codificadores H. 264/AVC:</strong><br/> Supondo que o valor seja N e N seja um valor diferente de zero, em cada quadro de IDR, o codificador deve marcar automaticamente os quadros seguindo o quadro IDR (e incluindo o quadro IDR) como quadros EPD, contanto que todos os três dos seguintes se apliquem:
<ul>
<li>O quadro já não está definido para ser marcado como um quadro de referência de longo prazo.</li>
<li>O quadro é um quadro de camada base. Por exemplo, o elemento de sintaxe <strong>temporal_id</strong> igual a 0.</li>
<li>O número de quadros marcados atualmente como EPD é menor que N.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>O segundo campo</strong></dt> <dt>bits [16.. 31]</dt> </dl></td>
<td>O modo de confiança do controle EPD.<br/> <strong>Codificadores H. 264/AVC:</strong><br/> 1 (confiar até) significa que o codificador pode usar um quadro EPD, a menos que o aplicativo invalide-o explicitamente por meio do controle de <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> . <br/> Outros valores são inválidos e reservados para uso futuro.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Essa é uma API estática.

O valor padrão deve ser 0

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 





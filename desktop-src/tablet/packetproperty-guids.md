---
description: A tabela a seguir lista os GUIDs de propriedade de pacote usados pela estrutura de propriedade de pacote \_ .
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: GUIDs de pacote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb7db9f2d5e05000bdccd5a09b2b799f38aa1bb692fea110ea153a57912cfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449366"
---
# <a name="packetproperty-guids"></a>GUIDs de pacote

A tabela a seguir lista os GUIDs de propriedade de pacote usados pela estrutura de [**\_ propriedade de pacote**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GUID_ALTITUDE_ORIENTATION<br/></td>
<td>Ângulo entre o eixo da caneta e a superfície do Tablet. O valor é 0 quando a caneta é paralela à superfície e 90 quando a caneta é perpendicular à superfície. Os valores são negativos quando a caneta é invertida.<br/></td>
</tr>
<tr class="even">
<td>GUID_AZIMUTH_ORIENTATION<br/></td>
<td>Rotação horária do cursor ao longo do eixo z por meio de um intervalo circular completo.<br/></td>
</tr>
<tr class="odd">
<td>GUID_BOXNUMBER<br/></td>
<td>O GUID que é usado para recuperar o número da caixa para uma alternativa de reconhecimento de tinta quando o reconhecedor está operando no modo de caixa.<br/></td>
</tr>
<tr class="even">
<td>GUID_BUTTON_PRESSURE<br/></td>
<td>Pressão sobre um botão sensível à pressão.<br/></td>
</tr>
<tr class="odd">
<td>GUID_NORMAL_PRESSURE<br/></td>
<td>O GUID do objeto de Pacoteproperty que representa a pressão da dica de caneta perpendicular à superfície do Tablet. Quanto maior a pressão colocada na ponta da caneta, mais tinta será desenhada.<br/></td>
</tr>
<tr class="even">
<td>GUID_PACKET_STATUS<br/></td>
<td>Contém um ou mais dos seguintes valores de sinalizador:<br/>
<ul>
<li>O cursor está tocando na superfície de desenho (valor = 1).</li>
<li>O cursor é invertido. Por exemplo, a extremidade de borracha da caneta está apontando para a superfície (valor = 2).</li>
<li>Não usado (valor = 4).</li>
<li>O botão de cilindro é pressionado (valor = 8).</li>
</ul></td>
</tr>
<tr class="odd">
<td>GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br/></td>
<td>O identificador de contato do dispositivo para um pacote.<br/></td>
</tr>
<tr class="even">
<td>GUID_SERIAL_NUMBER<br/></td>
<td>Identifica o pacote. Esse é o mesmo valor que você usa para recuperar o pacote da fila de pacotes.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TANGENT_PRESSURE<br/></td>
<td>O GUID do objeto de Pacoteproperty que representa a pressão da ponta da caneta ao longo do plano da superfície do Tablet.<br/></td>
</tr>
<tr class="even">
<td>GUID_TIMER_TICK<br/></td>
<td>Hora em que o pacote foi gerado.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TWIST_ORIENTATION<br/></td>
<td>Rotação horária do cursor em volta de seu próprio eixo.<br/></td>
</tr>
<tr class="even">
<td>GUID_X<br/></td>
<td>A coordenada x no espaço de coordenadas do Tablet. Cada pacote contém essa propriedade por padrão. A origem (0, 0) do Tablet é o canto superior esquerdo.<br/></td>
</tr>
<tr class="odd">
<td>GUID_X_TILT_ORIENTATION<br/></td>
<td>Para um cursor de caneta, a orientação de inclinação x é o ângulo entre os planos y, z-Plane e eixo y. O valor é 0 quando a caneta é perpendicular à superfície de desenho e é positiva quando a caneta está à direita de perpendicular.<br/></td>
</tr>
<tr class="even">
<td>GUID_Y<br/></td>
<td>A coordenada y no espaço de coordenadas do Tablet. Cada pacote contém essa propriedade por padrão. A origem (0, 0) do Tablet é o canto superior esquerdo.<br/></td>
</tr>
<tr class="odd">
<td>GUID_Y_TILT_ORIENTATION<br/></td>
<td>Para um cursor de caneta, a orientação de inclinação y é o ângulo entre os planos x, z-Plane e eixo x e de caneta. O valor é 0 quando a caneta é perpendicular à superfície de desenho e é positiva quando a caneta está para cima ou para fora do usuário.<br/></td>
</tr>
<tr class="even">
<td>GUID_Z<br/></td>
<td>A coordenada z ou a distância da ponta da caneta da superfície do Tablet. O tipo de enumeração <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> determina a unidade de medida para essa propriedade. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> O campo TangentPressure representa pressão ao longo do plano da superfície do Tablet; o campo NormalPressure representa a pressão perpendicular ao plano da superfície do Tablet.

 

 

 





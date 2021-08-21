---
description: A tabela a seguir lista GUIDs de propriedade de pacote usados pela estrutura PACKET \_ PROPERTY.
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: PacketProperty GUIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb7db9f2d5e05000bdccd5a09b2b799f38aa1bb692fea110ea153a57912cfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449366"
---
# <a name="packetproperty-guids"></a>PacketProperty GUIDs

A tabela a seguir lista GUIDs de propriedade de pacote usados pela [**estrutura PACKET \_ PROPERTY.**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)



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
<td>Ângulo entre o eixo da caneta e a superfície do tablet. O valor é 0 quando a caneta é paralela à superfície e 90 quando a caneta é uma vez à superfície. Os valores são negativos quando a caneta é invertida.<br/></td>
</tr>
<tr class="even">
<td>GUID_AZIMUTH_ORIENTATION<br/></td>
<td>Rotação no sentido horário do cursor ao redor do eixo z por meio de um intervalo circular completo.<br/></td>
</tr>
<tr class="odd">
<td>GUID_BOXNUMBER<br/></td>
<td>O GUID usado para recuperar o número da caixa para uma alternativa de reconhecimento de tinta quando o reconhecedor está operando no modo de caixa.<br/></td>
</tr>
<tr class="even">
<td>GUID_BUTTON_PRESSURE<br/></td>
<td>Pressão em um botão sensível à pressão.<br/></td>
</tr>
<tr class="odd">
<td>GUID_NORMAL_PRESSURE<br/></td>
<td>O GUID do objeto PacketProperty que representa a pressão da dica de caneta para a superfície do tablet. Quanto maior a pressão colocada na ponta da caneta, mais tinta será desenhada.<br/></td>
</tr>
<tr class="even">
<td>GUID_PACKET_STATUS<br/></td>
<td>Contém um ou mais dos seguintes valores de sinalizador:<br/>
<ul>
<li>O cursor está tocando na superfície de desenho (Valor = 1).</li>
<li>O cursor é invertido. Por exemplo, o final da borracha da caneta está apontando para a superfície (Valor = 2).</li>
<li>Não usado (Valor = 4).</li>
<li>O botão de botão de ressução é pressionado (Valor = 8).</li>
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
<td>O GUID do objeto PacketProperty que representa a pressão da ponta da caneta ao longo do plano da superfície do tablet.<br/></td>
</tr>
<tr class="even">
<td>GUID_TIMER_TICK<br/></td>
<td>Hora em que o pacote foi gerado.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TWIST_ORIENTATION<br/></td>
<td>Rotação no sentido horário do cursor em torno de seu próprio eixo.<br/></td>
</tr>
<tr class="even">
<td>GUID_X<br/></td>
<td>A coordenada X no espaço de coordenadas do tablet. Cada pacote contém essa propriedade por padrão. A origem (0,0) do tablet é o canto superior esquerdo.<br/></td>
</tr>
<tr class="odd">
<td>GUID_X_TILT_ORIENTATION<br/></td>
<td>Para um cursor de caneta, a orientação de inclinação x é o ângulo entre o plano y, z e a caneta e o plano do eixo y. O valor é 0 quando a caneta é um ponto final para a superfície de desenho e é positivo quando a caneta está à direita de um ponto final.<br/></td>
</tr>
<tr class="even">
<td>GUID_Y<br/></td>
<td>A coordenada y no espaço de coordenadas do tablet. Cada pacote contém essa propriedade por padrão. A origem (0,0) do tablet é o canto superior esquerdo.<br/></td>
</tr>
<tr class="odd">
<td>GUID_Y_TILT_ORIENTATION<br/></td>
<td>Para um cursor de caneta, a orientação de inclinação y é o ângulo entre o plano x,z e a caneta e o plano do eixo x. O valor é 0 quando a caneta é uma caneta para a superfície de desenho e é positivo quando a caneta está para cima ou para fora do usuário.<br/></td>
</tr>
<tr class="even">
<td>GUID_Z<br/></td>
<td>A coordenada z ou a distância da dica de caneta da superfície do tablet. O <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> de enumeração determina a unidade de medida para essa propriedade. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> O campo TangentPressure representa a pressão ao longo do plano da superfície do tablet; o campo NormalPressure representa a pressão ao plano da superfície do tablet.

 

 

 





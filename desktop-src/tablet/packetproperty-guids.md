---
description: A tabela a seguir lista GUIDs de propriedade de pacote usados pela estrutura PACKET \_ PROPERTY.
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: PacketProperty GUIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c897e19aea30db6e5dfa026fbdcfec77de5afa4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481642"
---
# <a name="packetproperty-guids"></a>PacketProperty GUIDs

A tabela a seguir lista GUIDs de propriedade de pacote usados pela [**estrutura PACKET \_ PROPERTY.**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)




| GUID | Descrição | 
|------|-------------|
| GUID_ALTITUDE_ORIENTATION<br /> | Ângulo entre o eixo da caneta e a superfície do tablet. O valor é 0 quando a caneta é paralela à superfície e 90 quando a caneta é uma vez à superfície. Os valores são negativos quando a caneta é invertida.<br /> | 
| GUID_AZIMUTH_ORIENTATION<br /> | Rotação no sentido horário do cursor ao redor do eixo z por meio de um intervalo circular completo.<br /> | 
| GUID_BOXNUMBER<br /> | O GUID usado para recuperar o número da caixa para uma alternativa de reconhecimento de tinta quando o reconhecedor está operando no modo de caixa.<br /> | 
| GUID_BUTTON_PRESSURE<br /> | Pressão em um botão sensível à pressão.<br /> | 
| GUID_NORMAL_PRESSURE<br /> | O GUID do objeto PacketProperty que representa a pressão da dica de caneta para a superfície do tablet. Quanto maior a pressão colocada na ponta da caneta, mais tinta será desenhada.<br /> | 
| GUID_PACKET_STATUS<br /> | Contém um ou mais dos seguintes valores de sinalizador:<br /><ul><li>O cursor está tocando na superfície de desenho (Valor = 1).</li><li>O cursor é invertido. Por exemplo, o final da borracha da caneta está apontando para a superfície (Valor = 2).</li><li>Não usado (Valor = 4).</li><li>O botão de botão de ressução é pressionado (Valor = 8).</li></ul> | 
| GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br /> | O identificador de contato do dispositivo para um pacote.<br /> | 
| GUID_SERIAL_NUMBER<br /> | Identifica o pacote. Esse é o mesmo valor que você usa para recuperar o pacote da fila de pacotes.<br /> | 
| GUID_TANGENT_PRESSURE<br /> | O GUID do objeto PacketProperty que representa a pressão da ponta da caneta ao longo do plano da superfície do tablet.<br /> | 
| GUID_TIMER_TICK<br /> | Hora em que o pacote foi gerado.<br /> | 
| GUID_TWIST_ORIENTATION<br /> | Rotação no sentido horário do cursor em torno de seu próprio eixo.<br /> | 
| GUID_X<br /> | A coordenada X no espaço de coordenadas do tablet. Cada pacote contém essa propriedade por padrão. A origem (0,0) do tablet é o canto superior esquerdo.<br /> | 
| GUID_X_TILT_ORIENTATION<br /> | Para um cursor de caneta, a orientação de inclinação x é o ângulo entre o plano y, z e a caneta e o plano do eixo y. O valor é 0 quando a caneta é um ponto final para a superfície de desenho e é positivo quando a caneta está à direita de um ponto final.<br /> | 
| GUID_Y<br /> | A coordenada y no espaço de coordenadas do tablet. Cada pacote contém essa propriedade por padrão. A origem (0,0) do tablet é o canto superior esquerdo.<br /> | 
| GUID_Y_TILT_ORIENTATION<br /> | Para um cursor de caneta, a orientação de inclinação y é o ângulo entre o plano x,z e a caneta e o plano do eixo x. O valor é 0 quando a caneta é uma caneta para a superfície de desenho e é positivo quando a caneta está para cima ou para fora do usuário.<br /> | 
| GUID_Z<br /> | A coordenada z ou a distância da dica de caneta da superfície do tablet. O <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> de enumeração determina a unidade de medida para essa propriedade. <br /> | 




 

> [!Note]  
> O campo TangentPressure representa a pressão ao longo do plano da superfície do tablet; o campo NormalPressure representa a pressão ao plano da superfície do tablet.

 

 

 





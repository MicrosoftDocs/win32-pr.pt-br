---
description: Define os valores que especificam as propriedades do pacote.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Constantes PacketPropertyGuids (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9eb946b170b1004deea7eb1f2faafeee5bc5dba
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884510"
---
# <a name="packetpropertyguids-constants"></a>Constantes PacketPropertyGuids

Define os valores que especificam as propriedades do pacote. O Tablet PCAPI usa identificadores globais exclusivos (GUIDs) para identificar Propriedades de pacote, que em COM são cadeias de caracteres constantes.

em C++, você pode acessar essas constantes no arquivo de cabeçalho Msinkaut. h, que está localizado no &lt; diretório systemdrive &gt; : \\ Program files \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ Include se você instalou o SDK no local padrão. Em C++, essas constantes são WCHARs, não BSTRs. Converta-os em BSTRs antes de usar. Para obter mais informações sobre o tipo de dados BSTR, consulte [usando a biblioteca com](using-the-com-library.md).

A tabela a seguir lista os campos GUID (identificador global exclusivo) da propriedade de pacote disponível. Use esses GUIDs para especificar quais propriedades o pacote contém ao criar o contexto do Tablet. Para determinar o intervalo e a resolução de uma propriedade, chame o método [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) . As constantes na tabela abaixo começando com "STR \_ " são representações de cadeia de caracteres das constantes binárias correspondentes mostradas na mesma célula de tabela.




| Constante | Descrição | 
|----------|-------------|
| <span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl><dt><strong>STR_GUID_X ou GUID_PACKETPROPERTY_GUID_X</strong></dt></dl> | A coordenada x no espaço de coordenadas do Tablet. Cada pacote contém essa propriedade por padrão. A origem (0, 0) do Tablet é o canto superior esquerdo.<br /> | 
| <span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl><dt><strong>STR_GUID_Y ou GUID_PACKETPROPERTY_GUID_Y</strong></dt></dl> | A coordenada y no espaço de coordenadas do Tablet. Cada pacote contém essa propriedade por padrão. A origem (0, 0) do Tablet é o canto superior esquerdo.<br /> | 
| <span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl><dt><strong>STR_GUID_Y ou GUID_PACKETPROPERTY_GUID_Y</strong></dt></dl> | A coordenada y no espaço de coordenadas do Tablet. Cada pacote contém essa propriedade por padrão. A origem (0, 0) do Tablet é o canto superior esquerdo.<br /> | 
| <span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl><dt><strong>STR_GUID_Z ou GUID_PACKETPROPERTY_GUID_Z</strong></dt></dl> | A coordenada z ou a distância da ponta da caneta da superfície do Tablet. O tipo de enumeração <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> determina a unidade de medida para essa propriedade.<br /> | 
| <span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl><dt><strong>STR_GUID_PAKETSTATUS ou GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt></dl> | Contém um ou mais dos seguintes valores de sinalizador:<br /><ul><li>O cursor está tocando na superfície de desenho (valor = 1).</li><li>O cursor é invertido. Por exemplo, a extremidade de borracha da caneta está apontando para a superfície (valor = 2).</li><li>Não usado (valor = 4).</li><li>O botão de cilindro é pressionado (valor = 8).</li></ul> | 
| <span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl><dt><strong>STR_GUID_TIMERTICK ou GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt></dl> | A hora em que o pacote foi gerado.<br /> | 
| <span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl><dt><strong>STR_GUID_TIMERTICK ou GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt></dl> | A hora em que o pacote foi gerado.<br /> | 
| <span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl><dt><strong>STR_GUID_SERIALNUMBER ou GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt></dl> | A propriedade de pacote para identificar o pacote.<br /> Esse é o mesmo valor que você usa para recuperar o pacote da fila de pacotes.<br /> | 
| <span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl><dt><strong>STR_GUID_NORMALPRESSURE ou GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt></dl> | A pressão da dica de caneta perpendicular à superfície do Tablet.<br /> Quanto maior a pressão na dica de caneta, mais tinta é desenhada.<br /> | 
| <span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl><dt><strong>STR_GUID_TANGENTPRESSURE ou GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt></dl> | A pressão da ponta da caneta ao longo do plano da superfície do Tablet.<br /> | 
| <span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl><dt><strong>STR_GUID_BUTTONPRESSURE ou GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt></dl> | A pressão sobre um botão sensível à pressão.<br /> | 
| <span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl><dt><strong>STR_GUID_XTILTORIENTATION ou GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt></dl> | O ângulo entre os planos y, z-Plane e eixo y.<br /> Aplica-se a um cursor de caneta.<br /> O valor é 0 quando a caneta é perpendicular à superfície de desenho e é positiva quando a caneta está à direita de perpendicular.<br /> | 
| <span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl><dt><strong>STR_GUID_YTILTORIENTATION ou GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt></dl> | O ângulo entre o plano x, o plano z e o eixo x e a caneta.<br /> Aplica-se a um cursor de caneta.<br /> O valor é 0 quando a caneta é perpendicular à superfície de desenho e é positiva quando a caneta está para cima ou para fora do usuário.<br /> | 
| <span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl><dt><strong>STR_GUID_AZIMUTHORIENTATION ou GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt></dl> | A rotação horária do cursor sobre o eixo z por meio de um intervalo circular completo.<br /> | 
| <span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl><dt><strong>STR_GUID_ALTITUDEORIENTATION ou GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt></dl> | O ângulo entre o eixo da caneta e a superfície do Tablet.<br /> O valor é 0 quando a caneta é paralela à superfície e 90 quando a caneta é perpendicular à superfície.<br /> Os valores são negativos quando a caneta é invertida.<br /> | 
| <span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl><dt><strong>STR_GUID_TWISTORIENTATION ou GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt></dl> | A rotação horária do cursor sobre seu próprio eixo.<br /> | 
| <span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl><dt><strong>STR_GUID_PITCHROTATION ou GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt></dl> | A propriedade de pacote que indica se a dica está acima ou abaixo de uma linha horizontal que é perpendicular à superfície de escrita.<br /><blockquote>[!Note]<br />Isso requer um digitalizador 3D.</blockquote><br /> O valor será positivo se a dica estiver acima da linha e negativa se estiver abaixo da linha. Por exemplo, se você mantiver a caneta na frente e escrever em uma parede imaginária, a inclinação será positiva se a dica estiver acima de uma linha que se estende de você para a parede.<br /> | 
| <span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl><dt><strong>STR_GUID_ROLLROTATION ou GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt></dl> | A rotação horária da caneta ao seu próprio eixo. <br /><blockquote>[!Note]<br />Isso requer um digitalizador 3D.</blockquote><br /> | 
| <span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl><dt><strong>STR_GUID_YAWROTATION ou GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt></dl> | O ângulo da caneta à esquerda ou à direita ao lado do centro de seu eixo horizontal quando a caneta é horizontal.<br /><blockquote>[!Note]<br />Isso requer um digitalizador 3D.</blockquote><br /> Se você mantiver a caneta na frente e escrever em uma parede imaginária, nenhuma guinada indica que a caneta é perpendicular à parede. O valor será negativo se a dica estiver à esquerda de perpendicular e positiva se a dica estiver à direita de perpendicular.<br /> | 
| <span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl><dt><strong>STR_GUID_YAWROTATION ou GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt></dl> | O ângulo da caneta à esquerda ou à direita ao lado do centro de seu eixo horizontal quando a caneta é horizontal.<br /><blockquote>[!Note]<br />Isso requer um digitalizador 3D.</blockquote><br /> Se você mantiver a caneta na frente e escrever em uma parede imaginária, nenhuma guinada indica que a caneta é perpendicular à parede. O valor será negativo se a dica estiver à esquerda de perpendicular e positiva se a dica estiver à direita de perpendicular.<br /> | 
| <span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl><dt><strong>STR_GUID_WIDTH ou GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt></dl> | A largura da área de contato em um digitalizador de toque.<br /> | 
| <span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl><dt><strong>STR_GUID_HEIGHT ou GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt></dl> | A altura da área de contato em um digitalizador de toque.<br /> | 
| <span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE ou GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt></dl> | O nível de confiança de que houve um contato Finger em um digitalizador de toque.<br /> | 
| <span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl><dt><strong>STR_GUID_DEVICE_CONTACT_ID ou GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt></dl> | O identificador de contato do dispositivo para um pacote.<br /> | 




## <a name="remarks"></a>Comentários

> [!Note]  
> Todos os valores de pacote provenientes do hardware do Tablet são inteiros de tamanho de 32 bits.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método IsPacketPropertySupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[**Método GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[**IInkTablet Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 





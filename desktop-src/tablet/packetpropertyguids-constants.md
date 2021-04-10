---
description: Define os valores que especificam as propriedades do pacote.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Constantes PacketPropertyGuids (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadb664cb3783932dc2e7063d7cfab07133ad9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171847"
---
# <a name="packetpropertyguids-constants"></a><span data-ttu-id="106b2-103">Constantes PacketPropertyGuids</span><span class="sxs-lookup"><span data-stu-id="106b2-103">PacketPropertyGuids Constants</span></span>

<span data-ttu-id="106b2-104">Define os valores que especificam as propriedades do pacote.</span><span class="sxs-lookup"><span data-stu-id="106b2-104">Defines values that specify the packet properties.</span></span> <span data-ttu-id="106b2-105">O Tablet PCAPI usa identificadores globais exclusivos (GUIDs) para identificar Propriedades de pacote, que em COM são cadeias de caracteres constantes.</span><span class="sxs-lookup"><span data-stu-id="106b2-105">The Tablet PCAPI uses globally unique identifiers (GUIDs) to identify packet properties, which in COM are constant strings.</span></span>

<span data-ttu-id="106b2-106">Em C++, você pode acessar essas constantes no arquivo de cabeçalho Msinkaut. h, que está localizado no <systemdrive> diretório: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ include se você instalou o SDK no local padrão.</span><span class="sxs-lookup"><span data-stu-id="106b2-106">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span> <span data-ttu-id="106b2-107">Em C++, essas constantes são WCHARs, não BSTRs.</span><span class="sxs-lookup"><span data-stu-id="106b2-107">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="106b2-108">Converta-os em BSTRs antes de usar.</span><span class="sxs-lookup"><span data-stu-id="106b2-108">Convert them into BSTRs before use.</span></span> <span data-ttu-id="106b2-109">Para obter mais informações sobre o tipo de dados BSTR, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="106b2-109">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

<span data-ttu-id="106b2-110">A tabela a seguir lista os campos GUID (identificador global exclusivo) da propriedade de pacote disponível.</span><span class="sxs-lookup"><span data-stu-id="106b2-110">The following table lists the available packet property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="106b2-111">Use esses GUIDs para especificar quais propriedades o pacote contém ao criar o contexto do Tablet.</span><span class="sxs-lookup"><span data-stu-id="106b2-111">Use these GUIDs to specify which properties the packet contains when you create the tablet context.</span></span> <span data-ttu-id="106b2-112">Para determinar o intervalo e a resolução de uma propriedade, chame o método [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) .</span><span class="sxs-lookup"><span data-stu-id="106b2-112">To determine the range and resolution of a property, call the [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) method.</span></span> <span data-ttu-id="106b2-113">As constantes na tabela abaixo começando com "STR \_ " são representações de cadeia de caracteres das constantes binárias correspondentes mostradas na mesma célula de tabela.</span><span class="sxs-lookup"><span data-stu-id="106b2-113">The constants in the table below beginning with "STR\_" are string representations of the corresponding binary constants shown in the same table cell.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="106b2-114">Constante</span><span class="sxs-lookup"><span data-stu-id="106b2-114">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="106b2-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="106b2-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl> <span data-ttu-id="106b2-116"><dt><strong>STR_GUID_X ou GUID_PACKETPROPERTY_GUID_X</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-116"><dt><strong>STR_GUID_X or GUID_PACKETPROPERTY_GUID_X</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-117">A coordenada x no espaço de coordenadas do Tablet.</span><span class="sxs-lookup"><span data-stu-id="106b2-117">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="106b2-118">Cada pacote contém essa propriedade por padrão.</span><span class="sxs-lookup"><span data-stu-id="106b2-118">Each packet contains this property by default.</span></span> <span data-ttu-id="106b2-119">A origem (0, 0) do Tablet é o canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="106b2-119">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="106b2-120"><dt><strong>STR_GUID_Y ou GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-120"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-121">A coordenada y no espaço de coordenadas do Tablet.</span><span class="sxs-lookup"><span data-stu-id="106b2-121">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="106b2-122">Cada pacote contém essa propriedade por padrão.</span><span class="sxs-lookup"><span data-stu-id="106b2-122">Each packet contains this property by default.</span></span> <span data-ttu-id="106b2-123">A origem (0, 0) do Tablet é o canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="106b2-123">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="106b2-124"><dt><strong>STR_GUID_Y ou GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-124"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-125">A coordenada y no espaço de coordenadas do Tablet.</span><span class="sxs-lookup"><span data-stu-id="106b2-125">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="106b2-126">Cada pacote contém essa propriedade por padrão.</span><span class="sxs-lookup"><span data-stu-id="106b2-126">Each packet contains this property by default.</span></span> <span data-ttu-id="106b2-127">A origem (0, 0) do Tablet é o canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="106b2-127">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl> <span data-ttu-id="106b2-128"><dt><strong>STR_GUID_Z ou GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-128"><dt><strong>STR_GUID_Z or GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-129">A coordenada z ou a distância da ponta da caneta da superfície do Tablet.</span><span class="sxs-lookup"><span data-stu-id="106b2-129">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="106b2-130">O tipo de enumeração <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> determina a unidade de medida para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="106b2-130">The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> enumeration type determines the unit of measurement for this property.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl> <span data-ttu-id="106b2-131"><dt><strong>STR_GUID_PAKETSTATUS ou GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-131"><dt><strong>STR_GUID_PAKETSTATUS or GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-132">Contém um ou mais dos seguintes valores de sinalizador:</span><span class="sxs-lookup"><span data-stu-id="106b2-132">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="106b2-133">O cursor está tocando na superfície de desenho (valor = 1).</span><span class="sxs-lookup"><span data-stu-id="106b2-133">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="106b2-134">O cursor é invertido.</span><span class="sxs-lookup"><span data-stu-id="106b2-134">The cursor is inverted.</span></span> <span data-ttu-id="106b2-135">Por exemplo, a extremidade de borracha da caneta está apontando para a superfície (valor = 2).</span><span class="sxs-lookup"><span data-stu-id="106b2-135">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="106b2-136">Não usado (valor = 4).</span><span class="sxs-lookup"><span data-stu-id="106b2-136">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="106b2-137">O botão de cilindro é pressionado (valor = 8).</span><span class="sxs-lookup"><span data-stu-id="106b2-137">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="106b2-138"><dt><strong>STR_GUID_TIMERTICK ou GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-138"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-139">A hora em que o pacote foi gerado.</span><span class="sxs-lookup"><span data-stu-id="106b2-139">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="106b2-140"><dt><strong>STR_GUID_TIMERTICK ou GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-140"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-141">A hora em que o pacote foi gerado.</span><span class="sxs-lookup"><span data-stu-id="106b2-141">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl> <span data-ttu-id="106b2-142"><dt><strong>STR_GUID_SERIALNUMBER ou GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-142"><dt><strong>STR_GUID_SERIALNUMBER or GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-143">A propriedade de pacote para identificar o pacote.</span><span class="sxs-lookup"><span data-stu-id="106b2-143">The packet property for identifying the packet.</span></span><br/> <span data-ttu-id="106b2-144">Esse é o mesmo valor que você usa para recuperar o pacote da fila de pacotes.</span><span class="sxs-lookup"><span data-stu-id="106b2-144">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl> <span data-ttu-id="106b2-145"><dt><strong>STR_GUID_NORMALPRESSURE ou GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-145"><dt><strong>STR_GUID_NORMALPRESSURE or GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-146">A pressão da dica de caneta perpendicular à superfície do Tablet.</span><span class="sxs-lookup"><span data-stu-id="106b2-146">The pressure of the pen tip perpendicular to the tablet surface.</span></span><br/> <span data-ttu-id="106b2-147">Quanto maior a pressão na dica de caneta, mais tinta é desenhada.</span><span class="sxs-lookup"><span data-stu-id="106b2-147">The greater the pressure on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl> <span data-ttu-id="106b2-148"><dt><strong>STR_GUID_TANGENTPRESSURE ou GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-148"><dt><strong>STR_GUID_TANGENTPRESSURE or GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-149">A pressão da ponta da caneta ao longo do plano da superfície do Tablet.</span><span class="sxs-lookup"><span data-stu-id="106b2-149">The pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl> <span data-ttu-id="106b2-150"><dt><strong>STR_GUID_BUTTONPRESSURE ou GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-150"><dt><strong>STR_GUID_BUTTONPRESSURE or GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-151">A pressão sobre um botão sensível à pressão.</span><span class="sxs-lookup"><span data-stu-id="106b2-151">The pressure on a pressure sensitive button.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl> <span data-ttu-id="106b2-152"><dt><strong>STR_GUID_XTILTORIENTATION ou GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-152"><dt><strong>STR_GUID_XTILTORIENTATION or GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-153">O ângulo entre os planos y, z-Plane e eixo y.</span><span class="sxs-lookup"><span data-stu-id="106b2-153">The angle between the y,z-plane and the pen and y-axis plane.</span></span><br/> <span data-ttu-id="106b2-154">Aplica-se a um cursor de caneta.</span><span class="sxs-lookup"><span data-stu-id="106b2-154">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="106b2-155">O valor é 0 quando a caneta é perpendicular à superfície de desenho e é positiva quando a caneta está à direita de perpendicular.</span><span class="sxs-lookup"><span data-stu-id="106b2-155">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl> <span data-ttu-id="106b2-156"><dt><strong>STR_GUID_YTILTORIENTATION ou GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-156"><dt><strong>STR_GUID_YTILTORIENTATION or GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-157">O ângulo entre o plano x, o plano z e o eixo x e a caneta.</span><span class="sxs-lookup"><span data-stu-id="106b2-157">The angle between the x,z-plane and the pen and x-axis plane.</span></span><br/> <span data-ttu-id="106b2-158">Aplica-se a um cursor de caneta.</span><span class="sxs-lookup"><span data-stu-id="106b2-158">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="106b2-159">O valor é 0 quando a caneta é perpendicular à superfície de desenho e é positiva quando a caneta está para cima ou para fora do usuário.</span><span class="sxs-lookup"><span data-stu-id="106b2-159">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl> <span data-ttu-id="106b2-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION ou GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION or GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-161">A rotação horária do cursor sobre o eixo z por meio de um intervalo circular completo.</span><span class="sxs-lookup"><span data-stu-id="106b2-161">The clockwise rotation of the cursor about the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl> <span data-ttu-id="106b2-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION ou GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION or GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-163">O ângulo entre o eixo da caneta e a superfície do Tablet.</span><span class="sxs-lookup"><span data-stu-id="106b2-163">The angle between the axis of the pen and the surface of the tablet.</span></span><br/> <span data-ttu-id="106b2-164">O valor é 0 quando a caneta é paralela à superfície e 90 quando a caneta é perpendicular à superfície.</span><span class="sxs-lookup"><span data-stu-id="106b2-164">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span><br/> <span data-ttu-id="106b2-165">Os valores são negativos quando a caneta é invertida.</span><span class="sxs-lookup"><span data-stu-id="106b2-165">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl> <span data-ttu-id="106b2-166"><dt><strong>STR_GUID_TWISTORIENTATION ou GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-166"><dt><strong>STR_GUID_TWISTORIENTATION or GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-167">A rotação horária do cursor sobre seu próprio eixo.</span><span class="sxs-lookup"><span data-stu-id="106b2-167">The clockwise rotation of the cursor about its own axis.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl> <span data-ttu-id="106b2-168"><dt><strong>STR_GUID_PITCHROTATION ou GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-168"><dt><strong>STR_GUID_PITCHROTATION or GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-169">A propriedade de pacote que indica se a dica está acima ou abaixo de uma linha horizontal que é perpendicular à superfície de escrita.</span><span class="sxs-lookup"><span data-stu-id="106b2-169">The packet property that indicates whether the tip is above or below a horizontal line that is perpendicular to the writing surface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="106b2-170">Isso requer um digitalizador 3D.</span><span class="sxs-lookup"><span data-stu-id="106b2-170">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="106b2-171">O valor será positivo se a dica estiver acima da linha e negativa se estiver abaixo da linha.</span><span class="sxs-lookup"><span data-stu-id="106b2-171">The value is positive if the tip is above the line and negative if it is below the line.</span></span> <span data-ttu-id="106b2-172">Por exemplo, se você mantiver a caneta na frente e escrever em uma parede imaginária, a inclinação será positiva se a dica estiver acima de uma linha que se estende de você para a parede.</span><span class="sxs-lookup"><span data-stu-id="106b2-172">For example, if you hold the pen in front of you and write on an imaginary wall, the pitch is positive if the tip is above a line extending from you to the wall.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl> <span data-ttu-id="106b2-173"><dt><strong>STR_GUID_ROLLROTATION ou GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-173"><dt><strong>STR_GUID_ROLLROTATION or GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-174">A rotação horária da caneta ao seu próprio eixo.</span><span class="sxs-lookup"><span data-stu-id="106b2-174">The clockwise rotation of the pen around its own axis.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="106b2-175">Isso requer um digitalizador 3D.</span><span class="sxs-lookup"><span data-stu-id="106b2-175">This requires a 3D digitizer.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="106b2-176"><dt><strong>STR_GUID_YAWROTATION ou GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-176"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-177">O ângulo da caneta à esquerda ou à direita ao lado do centro de seu eixo horizontal quando a caneta é horizontal.</span><span class="sxs-lookup"><span data-stu-id="106b2-177">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="106b2-178">Isso requer um digitalizador 3D.</span><span class="sxs-lookup"><span data-stu-id="106b2-178">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="106b2-179">Se você mantiver a caneta na frente e escrever em uma parede imaginária, nenhuma guinada indica que a caneta é perpendicular à parede.</span><span class="sxs-lookup"><span data-stu-id="106b2-179">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="106b2-180">O valor será negativo se a dica estiver à esquerda de perpendicular e positiva se a dica estiver à direita de perpendicular.</span><span class="sxs-lookup"><span data-stu-id="106b2-180">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="106b2-181"><dt><strong>STR_GUID_YAWROTATION ou GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-181"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-182">O ângulo da caneta à esquerda ou à direita ao lado do centro de seu eixo horizontal quando a caneta é horizontal.</span><span class="sxs-lookup"><span data-stu-id="106b2-182">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="106b2-183">Isso requer um digitalizador 3D.</span><span class="sxs-lookup"><span data-stu-id="106b2-183">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="106b2-184">Se você mantiver a caneta na frente e escrever em uma parede imaginária, nenhuma guinada indica que a caneta é perpendicular à parede.</span><span class="sxs-lookup"><span data-stu-id="106b2-184">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="106b2-185">O valor será negativo se a dica estiver à esquerda de perpendicular e positiva se a dica estiver à direita de perpendicular.</span><span class="sxs-lookup"><span data-stu-id="106b2-185">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl> <span data-ttu-id="106b2-186"><dt><strong>STR_GUID_WIDTH ou GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-186"><dt><strong>STR_GUID_WIDTH or GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-187">A largura da área de contato em um digitalizador de toque.</span><span class="sxs-lookup"><span data-stu-id="106b2-187">The width of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl> <span data-ttu-id="106b2-188"><dt><strong>STR_GUID_HEIGHT ou GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-188"><dt><strong>STR_GUID_HEIGHT or GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-189">A altura da área de contato em um digitalizador de toque.</span><span class="sxs-lookup"><span data-stu-id="106b2-189">The height of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl> <span data-ttu-id="106b2-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE ou GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE or GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-191">O nível de confiança de que houve um contato Finger em um digitalizador de toque.</span><span class="sxs-lookup"><span data-stu-id="106b2-191">The level of confidence that there was finger contact on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl> <span data-ttu-id="106b2-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID ou GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="106b2-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID or GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="106b2-193">O identificador de contato do dispositivo para um pacote.</span><span class="sxs-lookup"><span data-stu-id="106b2-193">The device contact identifier for a packet.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="106b2-194">Comentários</span><span class="sxs-lookup"><span data-stu-id="106b2-194">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="106b2-195">Todos os valores de pacote provenientes do hardware do Tablet são inteiros de tamanho de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="106b2-195">All packet values coming from the tablet hardware are 32-bit size integers.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="106b2-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="106b2-196">Requirements</span></span>



| <span data-ttu-id="106b2-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="106b2-197">Requirement</span></span> | <span data-ttu-id="106b2-198">Valor</span><span class="sxs-lookup"><span data-stu-id="106b2-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="106b2-199">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="106b2-199">Minimum supported client</span></span><br/> | <span data-ttu-id="106b2-200">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="106b2-200">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="106b2-201">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="106b2-201">Minimum supported server</span></span><br/> | <span data-ttu-id="106b2-202">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="106b2-202">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="106b2-203">parâmetro</span><span class="sxs-lookup"><span data-stu-id="106b2-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="106b2-204"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="106b2-204"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="106b2-205">Confira também</span><span class="sxs-lookup"><span data-stu-id="106b2-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="106b2-206">**Método IsPacketPropertySupported**</span><span class="sxs-lookup"><span data-stu-id="106b2-206">**IsPacketPropertySupported Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[<span data-ttu-id="106b2-207">**Método GetPropertyMetrics**</span><span class="sxs-lookup"><span data-stu-id="106b2-207">**GetPropertyMetrics Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[<span data-ttu-id="106b2-208">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="106b2-208">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 





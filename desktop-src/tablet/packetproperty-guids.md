---
description: A tabela a seguir lista os GUIDs de propriedade de pacote usados pela estrutura de propriedade de pacote \_ .
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: GUIDs de pacote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94591ccda5cd1f40b79c5cbb4fe80ca3ef99d2e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837344"
---
# <a name="packetproperty-guids"></a><span data-ttu-id="bdf1e-103">GUIDs de pacote</span><span class="sxs-lookup"><span data-stu-id="bdf1e-103">PacketProperty GUIDs</span></span>

<span data-ttu-id="bdf1e-104">A tabela a seguir lista os GUIDs de propriedade de pacote usados pela estrutura de [**\_ propriedade de pacote**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) .</span><span class="sxs-lookup"><span data-stu-id="bdf1e-104">The following table lists packet property GUIDs used by the [**PACKET\_PROPERTY**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bdf1e-105">GUID</span><span class="sxs-lookup"><span data-stu-id="bdf1e-105">GUID</span></span></th>
<th><span data-ttu-id="bdf1e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="bdf1e-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bdf1e-107">GUID_ALTITUDE_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="bdf1e-107">GUID_ALTITUDE_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="bdf1e-108">Ângulo entre o eixo da caneta e a superfície do Tablet.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-108">Angle between the axis of the pen and the surface of the tablet.</span></span> <span data-ttu-id="bdf1e-109">O valor é 0 quando a caneta é paralela à superfície e 90 quando a caneta é perpendicular à superfície.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-109">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span> <span data-ttu-id="bdf1e-110">Os valores são negativos quando a caneta é invertida.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-110">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bdf1e-111">GUID_AZIMUTH_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="bdf1e-111">GUID_AZIMUTH_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="bdf1e-112">Rotação horária do cursor ao longo do eixo z por meio de um intervalo circular completo.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-112">Clockwise rotation of the cursor around the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bdf1e-113">GUID_BOXNUMBER</span><span class="sxs-lookup"><span data-stu-id="bdf1e-113">GUID_BOXNUMBER</span></span><br/></td>
<td><span data-ttu-id="bdf1e-114">O GUID que é usado para recuperar o número da caixa para uma alternativa de reconhecimento de tinta quando o reconhecedor está operando no modo de caixa.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-114">The GUID that is used to retrieve the box number for an ink recognition alternate when the recognizer is operating in box mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bdf1e-115">GUID_BUTTON_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="bdf1e-115">GUID_BUTTON_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="bdf1e-116">Pressão sobre um botão sensível à pressão.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-116">Pressure on a pressure-sensitive button.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bdf1e-117">GUID_NORMAL_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="bdf1e-117">GUID_NORMAL_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="bdf1e-118">O GUID do objeto de Pacoteproperty que representa a pressão da dica de caneta perpendicular à superfície do Tablet.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-118">The GUID for the PacketProperty object that represents pressure of the pen tip perpendicular to the tablet surface.</span></span> <span data-ttu-id="bdf1e-119">Quanto maior a pressão colocada na ponta da caneta, mais tinta será desenhada.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-119">The greater the pressure put on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bdf1e-120">GUID_PACKET_STATUS</span><span class="sxs-lookup"><span data-stu-id="bdf1e-120">GUID_PACKET_STATUS</span></span><br/></td>
<td><span data-ttu-id="bdf1e-121">Contém um ou mais dos seguintes valores de sinalizador:</span><span class="sxs-lookup"><span data-stu-id="bdf1e-121">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="bdf1e-122">O cursor está tocando na superfície de desenho (valor = 1).</span><span class="sxs-lookup"><span data-stu-id="bdf1e-122">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="bdf1e-123">O cursor é invertido.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-123">The cursor is inverted.</span></span> <span data-ttu-id="bdf1e-124">Por exemplo, a extremidade de borracha da caneta está apontando para a superfície (valor = 2).</span><span class="sxs-lookup"><span data-stu-id="bdf1e-124">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="bdf1e-125">Não usado (valor = 4).</span><span class="sxs-lookup"><span data-stu-id="bdf1e-125">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="bdf1e-126">O botão de cilindro é pressionado (valor = 8).</span><span class="sxs-lookup"><span data-stu-id="bdf1e-126">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bdf1e-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span><span class="sxs-lookup"><span data-stu-id="bdf1e-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span></span><br/></td>
<td><span data-ttu-id="bdf1e-128">O identificador de contato do dispositivo para um pacote.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-128">The device contact identifier for a packet.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bdf1e-129">GUID_SERIAL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="bdf1e-129">GUID_SERIAL_NUMBER</span></span><br/></td>
<td><span data-ttu-id="bdf1e-130">Identifica o pacote.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-130">Identifies the packet.</span></span> <span data-ttu-id="bdf1e-131">Esse é o mesmo valor que você usa para recuperar o pacote da fila de pacotes.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-131">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bdf1e-132">GUID_TANGENT_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="bdf1e-132">GUID_TANGENT_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="bdf1e-133">O GUID do objeto de Pacoteproperty que representa a pressão da ponta da caneta ao longo do plano da superfície do Tablet.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-133">The GUID for the PacketProperty object that represents pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bdf1e-134">GUID_TIMER_TICK</span><span class="sxs-lookup"><span data-stu-id="bdf1e-134">GUID_TIMER_TICK</span></span><br/></td>
<td><span data-ttu-id="bdf1e-135">Hora em que o pacote foi gerado.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-135">Time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bdf1e-136">GUID_TWIST_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="bdf1e-136">GUID_TWIST_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="bdf1e-137">Rotação horária do cursor em volta de seu próprio eixo.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-137">Clockwise rotation of the cursor around its own axis.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bdf1e-138">GUID_X</span><span class="sxs-lookup"><span data-stu-id="bdf1e-138">GUID_X</span></span><br/></td>
<td><span data-ttu-id="bdf1e-139">A coordenada x no espaço de coordenadas do Tablet.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-139">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="bdf1e-140">Cada pacote contém essa propriedade por padrão.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-140">Each packet contains this property by default.</span></span> <span data-ttu-id="bdf1e-141">A origem (0, 0) do Tablet é o canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-141">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bdf1e-142">GUID_X_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="bdf1e-142">GUID_X_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="bdf1e-143">Para um cursor de caneta, a orientação de inclinação x é o ângulo entre os planos y, z-Plane e eixo y.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-143">For a pen cursor, the x-tilt orientation is the angle between the y,z-plane and the pen and y-axis plane.</span></span> <span data-ttu-id="bdf1e-144">O valor é 0 quando a caneta é perpendicular à superfície de desenho e é positiva quando a caneta está à direita de perpendicular.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-144">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bdf1e-145">GUID_Y</span><span class="sxs-lookup"><span data-stu-id="bdf1e-145">GUID_Y</span></span><br/></td>
<td><span data-ttu-id="bdf1e-146">A coordenada y no espaço de coordenadas do Tablet.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-146">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="bdf1e-147">Cada pacote contém essa propriedade por padrão.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-147">Each packet contains this property by default.</span></span> <span data-ttu-id="bdf1e-148">A origem (0, 0) do Tablet é o canto superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-148">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bdf1e-149">GUID_Y_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="bdf1e-149">GUID_Y_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="bdf1e-150">Para um cursor de caneta, a orientação de inclinação y é o ângulo entre os planos x, z-Plane e eixo x e de caneta.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-150">For a pen cursor, the y-tilt orientation is the angle between the x,z-plane and the pen and x-axis plane.</span></span> <span data-ttu-id="bdf1e-151">O valor é 0 quando a caneta é perpendicular à superfície de desenho e é positiva quando a caneta está para cima ou para fora do usuário.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-151">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward, or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bdf1e-152">GUID_Z</span><span class="sxs-lookup"><span data-stu-id="bdf1e-152">GUID_Z</span></span><br/></td>
<td><span data-ttu-id="bdf1e-153">A coordenada z ou a distância da ponta da caneta da superfície do Tablet.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-153">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="bdf1e-154">O tipo de enumeração <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> determina a unidade de medida para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-154">The <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> enumeration type determines the unit of measurement for this property.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="bdf1e-155">O campo TangentPressure representa pressão ao longo do plano da superfície do Tablet; o campo NormalPressure representa a pressão perpendicular ao plano da superfície do Tablet.</span><span class="sxs-lookup"><span data-stu-id="bdf1e-155">The TangentPressure field represents pressure along the plane of the tablet surface; the NormalPressure field represents pressure perpendicular to the plane of the tablet surface.</span></span>

 

 

 





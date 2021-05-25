---
description: Consulte uma lista de sinalizadores de capacidade de driver. Inclui as definições, os valores e as descrições com links para APIs.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f209e840450b834c3a69593d1297f2cba9ee43c0
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343371"
---
# <a name="d3dcaps2"></a><span data-ttu-id="85b16-104">D3DCAPS2</span><span class="sxs-lookup"><span data-stu-id="85b16-104">D3DCAPS2</span></span>

<span data-ttu-id="85b16-105">Sinalizadores de capacidade do driver.</span><span class="sxs-lookup"><span data-stu-id="85b16-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85b16-106">#definir</span><span class="sxs-lookup"><span data-stu-id="85b16-106">#define</span></span></td>
<td><span data-ttu-id="85b16-107">Valor</span><span class="sxs-lookup"><span data-stu-id="85b16-107">Value</span></span></td>
<td><span data-ttu-id="85b16-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="85b16-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b16-109">D3DCAPS2_CANAUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="85b16-109">D3DCAPS2_CANAUTOGENMIPMAP</span></span></td>
<td><span data-ttu-id="85b16-110">0x40000000L</span><span class="sxs-lookup"><span data-stu-id="85b16-110">0x40000000L</span></span></td>
<td><span data-ttu-id="85b16-111">O driver é capaz de gerar automaticamente mipmaps.</span><span class="sxs-lookup"><span data-stu-id="85b16-111">The driver is capable of automatically generating mipmaps.</span></span> <span data-ttu-id="85b16-112">Para obter mais informações, consulte <a href="automatic-generation-of-mipmaps.md">geração automática de mipmaps (Direct3D 9)</a>.</span><span class="sxs-lookup"><span data-stu-id="85b16-112">For more information, see <a href="automatic-generation-of-mipmaps.md">Automatic Generation of Mipmaps (Direct3D 9)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b16-113">D3DCAPS2_CANCALIBRATEGAMMA</span><span class="sxs-lookup"><span data-stu-id="85b16-113">D3DCAPS2_CANCALIBRATEGAMMA</span></span></td>
<td><span data-ttu-id="85b16-114">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="85b16-114">0x00100000L</span></span></td>
<td><span data-ttu-id="85b16-115">O sistema tem um calibrador instalado que pode ajustar automaticamente a rampa de gama para que o resultado seja idêntico em todos os sistemas que têm um calibrador.</span><span class="sxs-lookup"><span data-stu-id="85b16-115">The system has a calibrator installed that can automatically adjust the gamma ramp so that the result is identical on all systems that have a calibrator.</span></span> <span data-ttu-id="85b16-116">Para invocar o calibrador ao definir novos níveis de gama, use o sinalizador D3DSGR_CALIBRATE ao chamar <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="85b16-116">To invoke the calibrator when setting new gamma levels, use the D3DSGR_CALIBRATE flag when calling <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span></span> <span data-ttu-id="85b16-117">A calibragem de rampas de gama gera uma sobrecarga de processamento e não deve ser usada com frequência.</span><span class="sxs-lookup"><span data-stu-id="85b16-117">Calibrating gamma ramps incurs some processing overhead and should not be used frequently.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b16-118">D3DCAPS2_CANSHARERESOURCE</span><span class="sxs-lookup"><span data-stu-id="85b16-118">D3DCAPS2_CANSHARERESOURCE</span></span></td>
<td><span data-ttu-id="85b16-119">0x80000000L</span><span class="sxs-lookup"><span data-stu-id="85b16-119">0x80000000L</span></span></td>
<td><span data-ttu-id="85b16-120">O dispositivo pode criar recursos compartilháveis.</span><span class="sxs-lookup"><span data-stu-id="85b16-120">The device can create sharable resources.</span></span> <span data-ttu-id="85b16-121">Os métodos que criam recursos podem definir valores não nulos para seus parâmetros <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="85b16-121">Methods that create resources can set non-NULL values for their <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> parameters.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85b16-122">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="85b16-122">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="85b16-123">Esse sinalizador está disponível apenas no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="85b16-123">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b16-124">D3DCAPS2_CANMANAGERESOURCE</span><span class="sxs-lookup"><span data-stu-id="85b16-124">D3DCAPS2_CANMANAGERESOURCE</span></span></td>
<td><span data-ttu-id="85b16-125">0x10000000L</span><span class="sxs-lookup"><span data-stu-id="85b16-125">0x10000000L</span></span></td>
<td><span data-ttu-id="85b16-126">O driver é capaz de gerenciar recursos.</span><span class="sxs-lookup"><span data-stu-id="85b16-126">The driver is capable of managing resources.</span></span> <span data-ttu-id="85b16-127">Nesses drivers, D3DPOOL_MANAGED recursos serão gerenciados pelo driver.</span><span class="sxs-lookup"><span data-stu-id="85b16-127">On such drivers, D3DPOOL_MANAGED resources will be managed by the driver.</span></span> <span data-ttu-id="85b16-128">Para que o Direct3D substitua o driver para que o Direct3D gerencie recursos, use o sinalizador D3DCREATE_DISABLE_DRIVER_MANAGEMENT ao chamar <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="85b16-128">To have Direct3D override the driver so that Direct3D manages resources, use the D3DCREATE_DISABLE_DRIVER_MANAGEMENT flag when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b16-129">D3DCAPS2_DYNAMICTEXTURES</span><span class="sxs-lookup"><span data-stu-id="85b16-129">D3DCAPS2_DYNAMICTEXTURES</span></span></td>
<td><span data-ttu-id="85b16-130">0x20000000L</span><span class="sxs-lookup"><span data-stu-id="85b16-130">0x20000000L</span></span></td>
<td><span data-ttu-id="85b16-131">O driver dá suporte a texturas dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="85b16-131">The driver supports dynamic textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85b16-132">D3DCAPS2_FULLSCREENGAMMA</span><span class="sxs-lookup"><span data-stu-id="85b16-132">D3DCAPS2_FULLSCREENGAMMA</span></span></td>
<td><span data-ttu-id="85b16-133">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="85b16-133">0x00020000L</span></span></td>
<td><span data-ttu-id="85b16-134">O driver dá suporte ao ajuste dinâmico de rampa gama no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="85b16-134">The driver supports dynamic gamma ramp adjustment in full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85b16-135">D3DCAPS2_RESERVED</span><span class="sxs-lookup"><span data-stu-id="85b16-135">D3DCAPS2_RESERVED</span></span></td>
<td><span data-ttu-id="85b16-136">0x02000000L</span><span class="sxs-lookup"><span data-stu-id="85b16-136">0x02000000L</span></span></td>
<td><span data-ttu-id="85b16-137">Reservado; não usado.</span><span class="sxs-lookup"><span data-stu-id="85b16-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="85b16-138">Essas constantes são usadas pelo membro D3CAPS2 [**de D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="85b16-138">These constants are used by the D3CAPS2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="85b16-139">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="85b16-139">Constant Information</span></span>



|  <span data-ttu-id="85b16-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="85b16-140">Requirement</span></span>                        | <span data-ttu-id="85b16-141">Valor</span><span class="sxs-lookup"><span data-stu-id="85b16-141">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="85b16-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85b16-142">Header</span></span>                   | <span data-ttu-id="85b16-143">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="85b16-143">d3d9caps.h</span></span> |
| <span data-ttu-id="85b16-144">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="85b16-144">Minimum operating system</span></span> | <span data-ttu-id="85b16-145">Windows 98</span><span class="sxs-lookup"><span data-stu-id="85b16-145">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="85b16-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85b16-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85b16-147">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="85b16-147">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

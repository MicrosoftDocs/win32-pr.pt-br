---
description: Consulte uma lista de sinalizadores de capacidade do driver D3DCAPS2. Inclui as definições, os valores e as descrições com links para APIs.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2266073c2d803f9bf11f4a3548078c0d34e5f78
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408289"
---
# <a name="d3dcaps2"></a><span data-ttu-id="73778-104">D3DCAPS2</span><span class="sxs-lookup"><span data-stu-id="73778-104">D3DCAPS2</span></span>

<span data-ttu-id="73778-105">Sinalizadores de capacidade do driver.</span><span class="sxs-lookup"><span data-stu-id="73778-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73778-106">#definir</span><span class="sxs-lookup"><span data-stu-id="73778-106">#define</span></span></td>
<td><span data-ttu-id="73778-107">Valor</span><span class="sxs-lookup"><span data-stu-id="73778-107">Value</span></span></td>
<td><span data-ttu-id="73778-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="73778-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73778-109">D3DCAPS2_CANAUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="73778-109">D3DCAPS2_CANAUTOGENMIPMAP</span></span></td>
<td><span data-ttu-id="73778-110">0x40000000L</span><span class="sxs-lookup"><span data-stu-id="73778-110">0x40000000L</span></span></td>
<td><span data-ttu-id="73778-111">O driver é capaz de gerar automaticamente mipmaps.</span><span class="sxs-lookup"><span data-stu-id="73778-111">The driver is capable of automatically generating mipmaps.</span></span> <span data-ttu-id="73778-112">Para obter mais informações, consulte <a href="automatic-generation-of-mipmaps.md">geração automática de mipmaps (Direct3D 9)</a>.</span><span class="sxs-lookup"><span data-stu-id="73778-112">For more information, see <a href="automatic-generation-of-mipmaps.md">Automatic Generation of Mipmaps (Direct3D 9)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73778-113">D3DCAPS2_CANCALIBRATEGAMMA</span><span class="sxs-lookup"><span data-stu-id="73778-113">D3DCAPS2_CANCALIBRATEGAMMA</span></span></td>
<td><span data-ttu-id="73778-114">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="73778-114">0x00100000L</span></span></td>
<td><span data-ttu-id="73778-115">O sistema tem um calibrador instalado que pode ajustar automaticamente a rampa de gama para que o resultado seja idêntico em todos os sistemas que têm um calibrador.</span><span class="sxs-lookup"><span data-stu-id="73778-115">The system has a calibrator installed that can automatically adjust the gamma ramp so that the result is identical on all systems that have a calibrator.</span></span> <span data-ttu-id="73778-116">Para invocar o calibrador ao definir novos níveis de gama, use o sinalizador D3DSGR_CALIBRATE ao chamar <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="73778-116">To invoke the calibrator when setting new gamma levels, use the D3DSGR_CALIBRATE flag when calling <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span></span> <span data-ttu-id="73778-117">A calibragem de rampas de gama gera uma sobrecarga de processamento e não deve ser usada com frequência.</span><span class="sxs-lookup"><span data-stu-id="73778-117">Calibrating gamma ramps incurs some processing overhead and should not be used frequently.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73778-118">D3DCAPS2_CANSHARERESOURCE</span><span class="sxs-lookup"><span data-stu-id="73778-118">D3DCAPS2_CANSHARERESOURCE</span></span></td>
<td><span data-ttu-id="73778-119">0x80000000L</span><span class="sxs-lookup"><span data-stu-id="73778-119">0x80000000L</span></span></td>
<td><span data-ttu-id="73778-120">O dispositivo pode criar recursos compartilháveis.</span><span class="sxs-lookup"><span data-stu-id="73778-120">The device can create sharable resources.</span></span> <span data-ttu-id="73778-121">Os métodos que criam recursos podem definir valores não nulos para seus parâmetros <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="73778-121">Methods that create resources can set non-NULL values for their <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> parameters.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73778-122">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="73778-122">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="73778-123">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="73778-123">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73778-124">D3DCAPS2_CANMANAGERESOURCE</span><span class="sxs-lookup"><span data-stu-id="73778-124">D3DCAPS2_CANMANAGERESOURCE</span></span></td>
<td><span data-ttu-id="73778-125">0x10000000L</span><span class="sxs-lookup"><span data-stu-id="73778-125">0x10000000L</span></span></td>
<td><span data-ttu-id="73778-126">O driver é capaz de gerenciar recursos.</span><span class="sxs-lookup"><span data-stu-id="73778-126">The driver is capable of managing resources.</span></span> <span data-ttu-id="73778-127">Nesses drivers, D3DPOOL_MANAGED recursos serão gerenciados pelo driver.</span><span class="sxs-lookup"><span data-stu-id="73778-127">On such drivers, D3DPOOL_MANAGED resources will be managed by the driver.</span></span> <span data-ttu-id="73778-128">Para que o Direct3D substitua o driver para que o Direct3D gerencie os recursos, use o sinalizador D3DCREATE_DISABLE_DRIVER_MANAGEMENT ao chamar <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="73778-128">To have Direct3D override the driver so that Direct3D manages resources, use the D3DCREATE_DISABLE_DRIVER_MANAGEMENT flag when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73778-129">D3DCAPS2_DYNAMICTEXTURES</span><span class="sxs-lookup"><span data-stu-id="73778-129">D3DCAPS2_DYNAMICTEXTURES</span></span></td>
<td><span data-ttu-id="73778-130">0x20000000L</span><span class="sxs-lookup"><span data-stu-id="73778-130">0x20000000L</span></span></td>
<td><span data-ttu-id="73778-131">O driver dá suporte a texturas dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="73778-131">The driver supports dynamic textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73778-132">D3DCAPS2_FULLSCREENGAMMA</span><span class="sxs-lookup"><span data-stu-id="73778-132">D3DCAPS2_FULLSCREENGAMMA</span></span></td>
<td><span data-ttu-id="73778-133">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="73778-133">0x00020000L</span></span></td>
<td><span data-ttu-id="73778-134">O driver dá suporte ao ajuste de rampa de gama dinâmico no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="73778-134">The driver supports dynamic gamma ramp adjustment in full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73778-135">D3DCAPS2_RESERVED</span><span class="sxs-lookup"><span data-stu-id="73778-135">D3DCAPS2_RESERVED</span></span></td>
<td><span data-ttu-id="73778-136">0x02000000L</span><span class="sxs-lookup"><span data-stu-id="73778-136">0x02000000L</span></span></td>
<td><span data-ttu-id="73778-137">Reservado Não usado.</span><span class="sxs-lookup"><span data-stu-id="73778-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="73778-138">Essas constantes são usadas pelo membro D3CAPS2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="73778-138">These constants are used by the D3CAPS2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="73778-139">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="73778-139">Constant Information</span></span>



|  <span data-ttu-id="73778-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="73778-140">Requirement</span></span>                        | <span data-ttu-id="73778-141">Valor</span><span class="sxs-lookup"><span data-stu-id="73778-141">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="73778-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73778-142">Header</span></span>                   | <span data-ttu-id="73778-143">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="73778-143">d3d9caps.h</span></span> |
| <span data-ttu-id="73778-144">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="73778-144">Minimum operating system</span></span> | <span data-ttu-id="73778-145">Windows 98</span><span class="sxs-lookup"><span data-stu-id="73778-145">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="73778-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73778-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73778-147">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="73778-147">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

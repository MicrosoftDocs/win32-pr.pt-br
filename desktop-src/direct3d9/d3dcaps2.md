---
description: Sinalizadores de capacidade do driver.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953e73c0ea6b079a6b8f0658790c749b4f30a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773917"
---
# <a name="d3dcaps2"></a><span data-ttu-id="a1502-103">D3DCAPS2</span><span class="sxs-lookup"><span data-stu-id="a1502-103">D3DCAPS2</span></span>

<span data-ttu-id="a1502-104">Sinalizadores de capacidade do driver.</span><span class="sxs-lookup"><span data-stu-id="a1502-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a1502-105">#definir</span><span class="sxs-lookup"><span data-stu-id="a1502-105">#define</span></span></td>
<td><span data-ttu-id="a1502-106">Valor</span><span class="sxs-lookup"><span data-stu-id="a1502-106">Value</span></span></td>
<td><span data-ttu-id="a1502-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1502-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1502-108">D3DCAPS2_CANAUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="a1502-108">D3DCAPS2_CANAUTOGENMIPMAP</span></span></td>
<td><span data-ttu-id="a1502-109">0x40000000L</span><span class="sxs-lookup"><span data-stu-id="a1502-109">0x40000000L</span></span></td>
<td><span data-ttu-id="a1502-110">O driver é capaz de gerar automaticamente mipmaps.</span><span class="sxs-lookup"><span data-stu-id="a1502-110">The driver is capable of automatically generating mipmaps.</span></span> <span data-ttu-id="a1502-111">Para obter mais informações, consulte <a href="automatic-generation-of-mipmaps.md">geração automática de mipmaps (Direct3D 9)</a>.</span><span class="sxs-lookup"><span data-stu-id="a1502-111">For more information, see <a href="automatic-generation-of-mipmaps.md">Automatic Generation of Mipmaps (Direct3D 9)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1502-112">D3DCAPS2_CANCALIBRATEGAMMA</span><span class="sxs-lookup"><span data-stu-id="a1502-112">D3DCAPS2_CANCALIBRATEGAMMA</span></span></td>
<td><span data-ttu-id="a1502-113">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="a1502-113">0x00100000L</span></span></td>
<td><span data-ttu-id="a1502-114">O sistema tem um calibrador instalado que pode ajustar automaticamente a rampa de gama para que o resultado seja idêntico em todos os sistemas que têm um calibrador.</span><span class="sxs-lookup"><span data-stu-id="a1502-114">The system has a calibrator installed that can automatically adjust the gamma ramp so that the result is identical on all systems that have a calibrator.</span></span> <span data-ttu-id="a1502-115">Para invocar o calibrador ao definir novos níveis de gama, use o sinalizador D3DSGR_CALIBRATE ao chamar <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a1502-115">To invoke the calibrator when setting new gamma levels, use the D3DSGR_CALIBRATE flag when calling <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span></span> <span data-ttu-id="a1502-116">A calibragem de rampas de gama gera uma sobrecarga de processamento e não deve ser usada com frequência.</span><span class="sxs-lookup"><span data-stu-id="a1502-116">Calibrating gamma ramps incurs some processing overhead and should not be used frequently.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1502-117">D3DCAPS2_CANSHARERESOURCE</span><span class="sxs-lookup"><span data-stu-id="a1502-117">D3DCAPS2_CANSHARERESOURCE</span></span></td>
<td><span data-ttu-id="a1502-118">0x80000000L</span><span class="sxs-lookup"><span data-stu-id="a1502-118">0x80000000L</span></span></td>
<td><span data-ttu-id="a1502-119">O dispositivo pode criar recursos compartilháveis.</span><span class="sxs-lookup"><span data-stu-id="a1502-119">The device can create sharable resources.</span></span> <span data-ttu-id="a1502-120">Os métodos que criam recursos podem definir valores não nulos para seus parâmetros <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a1502-120">Methods that create resources can set non-NULL values for their <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> parameters.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a1502-121">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a1502-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a1502-122">Esse sinalizador está disponível somente no Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="a1502-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1502-123">D3DCAPS2_CANMANAGERESOURCE</span><span class="sxs-lookup"><span data-stu-id="a1502-123">D3DCAPS2_CANMANAGERESOURCE</span></span></td>
<td><span data-ttu-id="a1502-124">0x10000000L</span><span class="sxs-lookup"><span data-stu-id="a1502-124">0x10000000L</span></span></td>
<td><span data-ttu-id="a1502-125">O driver é capaz de gerenciar recursos.</span><span class="sxs-lookup"><span data-stu-id="a1502-125">The driver is capable of managing resources.</span></span> <span data-ttu-id="a1502-126">Nesses drivers, D3DPOOL_MANAGED recursos serão gerenciados pelo driver.</span><span class="sxs-lookup"><span data-stu-id="a1502-126">On such drivers, D3DPOOL_MANAGED resources will be managed by the driver.</span></span> <span data-ttu-id="a1502-127">Para que o Direct3D substitua o driver para que o Direct3D gerencie os recursos, use o sinalizador D3DCREATE_DISABLE_DRIVER_MANAGEMENT ao chamar <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a1502-127">To have Direct3D override the driver so that Direct3D manages resources, use the D3DCREATE_DISABLE_DRIVER_MANAGEMENT flag when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1502-128">D3DCAPS2_DYNAMICTEXTURES</span><span class="sxs-lookup"><span data-stu-id="a1502-128">D3DCAPS2_DYNAMICTEXTURES</span></span></td>
<td><span data-ttu-id="a1502-129">0x20000000L</span><span class="sxs-lookup"><span data-stu-id="a1502-129">0x20000000L</span></span></td>
<td><span data-ttu-id="a1502-130">O driver dá suporte a texturas dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="a1502-130">The driver supports dynamic textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1502-131">D3DCAPS2_FULLSCREENGAMMA</span><span class="sxs-lookup"><span data-stu-id="a1502-131">D3DCAPS2_FULLSCREENGAMMA</span></span></td>
<td><span data-ttu-id="a1502-132">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="a1502-132">0x00020000L</span></span></td>
<td><span data-ttu-id="a1502-133">O driver dá suporte ao ajuste de rampa de gama dinâmico no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="a1502-133">The driver supports dynamic gamma ramp adjustment in full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1502-134">D3DCAPS2_RESERVED</span><span class="sxs-lookup"><span data-stu-id="a1502-134">D3DCAPS2_RESERVED</span></span></td>
<td><span data-ttu-id="a1502-135">0x02000000L</span><span class="sxs-lookup"><span data-stu-id="a1502-135">0x02000000L</span></span></td>
<td><span data-ttu-id="a1502-136">Reservado Não usado.</span><span class="sxs-lookup"><span data-stu-id="a1502-136">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a1502-137">Essas constantes são usadas pelo membro D3CAPS2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="a1502-137">These constants are used by the D3CAPS2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="a1502-138">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="a1502-138">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="a1502-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1502-139">Header</span></span>                   | <span data-ttu-id="a1502-140">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="a1502-140">d3d9caps.h</span></span> |
| <span data-ttu-id="a1502-141">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="a1502-141">Minimum operating system</span></span> | <span data-ttu-id="a1502-142">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a1502-142">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a1502-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1502-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1502-144">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="a1502-144">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

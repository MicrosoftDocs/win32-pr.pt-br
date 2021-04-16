---
description: Este tópico descreve o que há de novo na infra-estrutura de gráficos do Microsoft DirectX (DXGI) 1,6 para várias versões do Windows 10.
ms.assetid: C68EC437-7600-43A8-8DEA-5A6AEE75D5AA
title: Aprimoramentos de DXGI 1,6
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 03961b4f9af50675ee157c4840b9ed744c54f423
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500633"
---
# <a name="dxgi-16-improvements"></a><span data-ttu-id="39a07-103">Aprimoramentos de DXGI 1,6</span><span class="sxs-lookup"><span data-stu-id="39a07-103">DXGI 1.6 improvements</span></span>

<span data-ttu-id="39a07-104">Este tópico descreve o que há de novo na infra-estrutura de gráficos do Microsoft DirectX (DXGI) 1,6 para várias versões do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="39a07-104">This topic describes what's new in Microsoft DirectX Graphics Infrastructure (DXGI) 1.6 for various releases of Windows 10.</span></span>

## <a name="windows-10-october-2018-update"></a><span data-ttu-id="39a07-105">Atualização de outubro de 2018 para o Windows 10</span><span class="sxs-lookup"><span data-stu-id="39a07-105">Windows 10 October 2018 Update</span></span>

<span data-ttu-id="39a07-106">Essas APIs foram adicionadas para o Windows 10, versão 1809 (10,0; Build 17763) &mdash; também conhecido como atualização do Windows 10 de outubro de 2018.</span><span class="sxs-lookup"><span data-stu-id="39a07-106">These APIs were added for Windows 10, version 1809 (10.0; Build 17763)&mdash;also known as Windows 10 October 2018 Update.</span></span>

- <span data-ttu-id="39a07-107">Interface [**IDXGIFactory7**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory7) e seus métodos.</span><span class="sxs-lookup"><span data-stu-id="39a07-107">[**IDXGIFactory7**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory7) interface, and its methods.</span></span>

## <a name="windows-10-april-2018-update"></a><span data-ttu-id="39a07-108">Atualização de abril de 2018 do Windows 10</span><span class="sxs-lookup"><span data-stu-id="39a07-108">Windows 10 April 2018 Update</span></span>

<span data-ttu-id="39a07-109">Essas APIs foram adicionadas para o Windows 10, versão 1803 (10,0; Build 17134) &mdash; também conhecido como atualização do Windows 10 de abril de 2018.</span><span class="sxs-lookup"><span data-stu-id="39a07-109">These APIs were added for Windows 10, version 1803 (10.0; Build 17134)&mdash;also known as Windows 10 April 2018 Update.</span></span>

- <span data-ttu-id="39a07-110">Enumeração de [**DXGI_GPU_PREFERENCE**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference) .</span><span class="sxs-lookup"><span data-stu-id="39a07-110">[**DXGI_GPU_PREFERENCE**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference) enumeration.</span></span>
- <span data-ttu-id="39a07-111">Interface [**IDXGIFactory6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6) e seus métodos.</span><span class="sxs-lookup"><span data-stu-id="39a07-111">[**IDXGIFactory6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6) interface, and its methods.</span></span>

## <a name="windows-10-fall-creators-update"></a><span data-ttu-id="39a07-112">Windows 10 Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="39a07-112">Windows 10 Fall Creators Update</span></span>

<span data-ttu-id="39a07-113">Para Windows 10, versão 1709 (10,0; Build 16299) &mdash; também conhecido como atualização dos criadores de outono do Windows 10 &mdash; essas constantes foram adicionadas à enumeração de [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) .</span><span class="sxs-lookup"><span data-stu-id="39a07-113">For Windows 10, version 1709 (10.0; Build 16299)&mdash;also known as Windows 10 Fall Creators Update&mdash;these constants have been added to the [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) enumeration.</span></span> 

- <span data-ttu-id="39a07-114">**DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES**</span><span class="sxs-lookup"><span data-stu-id="39a07-114">**DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES**</span></span>
- <span data-ttu-id="39a07-115">**DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES**</span><span class="sxs-lookup"><span data-stu-id="39a07-115">**DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES**</span></span>
- <span data-ttu-id="39a07-116">**DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE**</span><span class="sxs-lookup"><span data-stu-id="39a07-116">**DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE**</span></span>

## <a name="windows-10-creators-update"></a><span data-ttu-id="39a07-117">Atualização do Windows 10 para Criadores</span><span class="sxs-lookup"><span data-stu-id="39a07-117">Windows 10 Creators Update</span></span>

<span data-ttu-id="39a07-118">Para Windows 10, versão 1703 (10,0; Build 15063) &mdash; também conhecido como atualização do Windows 10 para criadores, &mdash; a seguinte funcionalidade foi adicionada à Microsoft DirectX Graphics Infrastructure (DXGI) 1,6 para detectar exibições HDR.</span><span class="sxs-lookup"><span data-stu-id="39a07-118">For Windows 10, version 1703 (10.0; Build 15063)&mdash;also known as Windows 10 Creators Update&mdash;the following functionality has been added to Microsoft DirectX Graphics Infrastructure (DXGI) 1.6 in order to detect HDR displays.</span></span>

### <a name="high-dynamic-range-hdr-detection"></a><span data-ttu-id="39a07-119">Detecção de grande alcance de intervalo dinâmico (HDR)</span><span class="sxs-lookup"><span data-stu-id="39a07-119">High dynamic range (HDR) detection</span></span>

<span data-ttu-id="39a07-120">Essas APIs foram adicionadas para detectar exibições HDR.</span><span class="sxs-lookup"><span data-stu-id="39a07-120">These APIs have been added in order to detect HDR displays.</span></span>

- <span data-ttu-id="39a07-121">Estrutura de [**DXGI_ADAPTER_DESC3**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3)</span><span class="sxs-lookup"><span data-stu-id="39a07-121">[**DXGI_ADAPTER_DESC3**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3) structure</span></span>
- <span data-ttu-id="39a07-122">Enumeração de [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)</span><span class="sxs-lookup"><span data-stu-id="39a07-122">[**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) enumeration</span></span>
- <span data-ttu-id="39a07-123">Enumeração de [**DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)</span><span class="sxs-lookup"><span data-stu-id="39a07-123">[**DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags) enumeration</span></span>
- <span data-ttu-id="39a07-124">Estrutura de [**DXGI_OUTPUT_DESC1**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)</span><span class="sxs-lookup"><span data-stu-id="39a07-124">[**DXGI_OUTPUT_DESC1**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) structure</span></span>
- <span data-ttu-id="39a07-125">Função [**DXGIDeclareAdapterRemovalSupport**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)</span><span class="sxs-lookup"><span data-stu-id="39a07-125">[**DXGIDeclareAdapterRemovalSupport**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport) function</span></span>
- <span data-ttu-id="39a07-126">Interface [**IDXGIAdapter4**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgiadapter4) e seus métodos</span><span class="sxs-lookup"><span data-stu-id="39a07-126">[**IDXGIAdapter4**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgiadapter4) interface, and its methods</span></span>
- <span data-ttu-id="39a07-127">Interface [**IDXGIOutput6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgioutput6) e seus métodos</span><span class="sxs-lookup"><span data-stu-id="39a07-127">[**IDXGIOutput6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgioutput6) interface, and its methods</span></span>

<span data-ttu-id="39a07-128">Além disso, as constantes foram adicionadas à enumeração de [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) para dar suporte a essas APIs.</span><span class="sxs-lookup"><span data-stu-id="39a07-128">Also, constants have been added to the [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) enumeration to support these APIs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39a07-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="39a07-129">Related topics</span></span>
[<span data-ttu-id="39a07-130">Guia de programação para DXGI</span><span class="sxs-lookup"><span data-stu-id="39a07-130">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)

---
title: Limitações ao criar dispositivos de referência e detorção
description: Existem algumas limitações para a criação de dispositivos WARP e de referência no Direct3D 10,1 e no Direct3D 11,0. Este tópico discute essas limitações.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12540b1fdb8f2bc00ef2a0e596904e0b717bed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294080"
---
# <a name="limitations-creating-warp-and-reference-devices"></a><span data-ttu-id="19080-104">Limitações ao criar dispositivos de referência e detorção</span><span class="sxs-lookup"><span data-stu-id="19080-104">Limitations Creating WARP and Reference Devices</span></span>

<span data-ttu-id="19080-105">Existem algumas limitações para a criação de dispositivos WARP e de referência no Direct3D 10,1 e no Direct3D 11,0.</span><span class="sxs-lookup"><span data-stu-id="19080-105">Some limitations exist for creating WARP and Reference devices in Direct3D 10.1 and Direct3D 11.0.</span></span> <span data-ttu-id="19080-106">Este tópico discute essas limitações.</span><span class="sxs-lookup"><span data-stu-id="19080-106">This topic discusses those limitations.</span></span>

<span data-ttu-id="19080-107">Os tipos de driver D3D10 \_ \_ \_ e \_ referência de tipo de driver d3d10 não têm \_ \_ suporte nos níveis de recurso D3D10 \_ \_ \_ de nível 9 \_ 1 a d3d10 \_ Feature \_ nível \_ 9 \_ 3 no Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="19080-107">The D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE driver types are not supported on the D3D10\_FEATURE\_LEVEL\_9\_1 through D3D10\_FEATURE\_LEVEL\_9\_3 feature levels in Direct3D 10.1.</span></span> <span data-ttu-id="19080-108">Além disso, o tipo de driver de \_ Warp do tipo de driver D3D \_ \_ não tem suporte no \_ nível de recurso do D3D \_ \_ 11 \_ 0 no Direct3D 11,0.</span><span class="sxs-lookup"><span data-stu-id="19080-108">Additionally, the D3D\_DRIVER\_TYPE\_WARP driver type is not supported on D3D\_FEATURE\_LEVEL\_11\_0 in Direct3D 11.0.</span></span> <span data-ttu-id="19080-109">Ou seja, quando você chama [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para criar um dispositivo Direct3D 10,1 ou quando chama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para criar um dispositivo Direct3D 11,0, se você especificar uma combinação de um desses tipos de driver com um desses níveis de recurso na chamada, a chamada será inválida.</span><span class="sxs-lookup"><span data-stu-id="19080-109">That is, when you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device or when you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.0 device, if you specify a combination of one of these driver types with one of these feature levels in the call, the call is invalid.</span></span> <span data-ttu-id="19080-110">Somente as seguintes combinações de níveis de recurso, tempos de execução e tipos de driver são válidas para dispositivos de detorção e referência:</span><span class="sxs-lookup"><span data-stu-id="19080-110">Only the following combinations of feature levels, runtimes, and driver types are valid for WARP and Reference devices:</span></span>

-   <span data-ttu-id="19080-111">\_Tipo de driver D3D \_ \_ Warp em todos os níveis de recurso no Direct3D 11,1, que o Windows 8 inclui</span><span class="sxs-lookup"><span data-stu-id="19080-111">D3D\_DRIVER\_TYPE\_WARP on all feature levels in Direct3D 11.1, which Windows 8 includes</span></span>

    <span data-ttu-id="19080-112">\_ \_ \_ Referência de tipo de driver D3D em todos os níveis de recurso no Direct3D 11,1</span><span class="sxs-lookup"><span data-stu-id="19080-112">D3D\_DRIVER\_TYPE\_REFERENCE on all feature levels in Direct3D 11.1</span></span>

    <span data-ttu-id="19080-113">Quando você chamar [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para criar um dispositivo Direct3D 11,1, a chamada será válida se você especificar uma combinação de um desses tipos de driver com um desses níveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="19080-113">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="19080-114">\_ \_ Tipo de driver D3D \_ Warp no \_ nível de recurso do D3D \_ \_ 9 \_ 1 por meio \_ \_ \_ \_ de níveis de recurso do nível de recurso do D3D 10 1 no Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="19080-114">D3D\_DRIVER\_TYPE\_WARP on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="19080-115">\_ \_ \_ Referência de tipo de driver D3D no nível de recurso do D3D \_ \_ \_ 9 \_ 1 por meio dos \_ \_ \_ \_ níveis de recurso do nível de recurso do D3D 11 0 no Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="19080-115">D3D\_DRIVER\_TYPE\_REFERENCE on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_11\_0 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="19080-116">Quando você chamar [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para criar um dispositivo Direct3D 11, a chamada será válida se você especificar uma combinação de um desses tipos de driver com um desses níveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="19080-116">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="19080-117">D3D10 \_ tipo de driver \_ \_ dewarpe e \_ \_ \_ referência de tipo de driver d3d10 no nível de recurso d3d10 \_ \_ \_ \_ de 10 0 a D3D10 \_ \_ \_ de nível de recurso \_ de 10 1 no Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="19080-117">D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE on D3D10\_FEATURE\_LEVEL\_10\_0 through D3D10\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 10.1</span></span>

    <span data-ttu-id="19080-118">Quando você chamar [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para criar um dispositivo Direct3D 10,1, a chamada será válida se você especificar uma combinação de um desses tipos de driver com um desses níveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="19080-118">When you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19080-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19080-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19080-120">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="19080-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="19080-121">Introdução ao Direct3D 11 no hardware de nível inferior</span><span class="sxs-lookup"><span data-stu-id="19080-121">Introduction to Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[<span data-ttu-id="19080-122">Como: criar um dispositivo de detorção</span><span class="sxs-lookup"><span data-stu-id="19080-122">How To: Create a WARP Device</span></span>](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[<span data-ttu-id="19080-123">Como: criar um dispositivo de referência</span><span class="sxs-lookup"><span data-stu-id="19080-123">How To: Create a Reference Device</span></span>](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[<span data-ttu-id="19080-124">**\_Tipo de driver d3d10 \_**</span><span class="sxs-lookup"><span data-stu-id="19080-124">**D3D10\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[<span data-ttu-id="19080-125">**\_LEVEL1 do recurso d3d10 \_**</span><span class="sxs-lookup"><span data-stu-id="19080-125">**D3D10\_FEATURE\_LEVEL1**</span></span>](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[<span data-ttu-id="19080-126">**\_Tipo de driver do D3D \_**</span><span class="sxs-lookup"><span data-stu-id="19080-126">**D3D\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[<span data-ttu-id="19080-127">**\_Nível de recurso do D3D \_**</span><span class="sxs-lookup"><span data-stu-id="19080-127">**D3D\_FEATURE\_LEVEL**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 
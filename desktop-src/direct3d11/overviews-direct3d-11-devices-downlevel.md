---
title: Direct3D 11 em hardware de nível inferior
description: Esta seção discute como o Direct3D 11 foi projetado para dar suporte a hardware novo e existente, do DirectX 9 ao DirectX 11.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f730a43db803e1e5198794167d0078a5b2896f6c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104562420"
---
# <a name="direct3d-11-on-downlevel-hardware"></a><span data-ttu-id="d80b9-103">Direct3D 11 em hardware de nível inferior</span><span class="sxs-lookup"><span data-stu-id="d80b9-103">Direct3D 11 on Downlevel Hardware</span></span>

<span data-ttu-id="d80b9-104">Esta seção discute como o Direct3D 11 foi projetado para dar suporte a hardware novo e existente, do DirectX 9 ao DirectX 11.</span><span class="sxs-lookup"><span data-stu-id="d80b9-104">This section discusses how Direct3D 11 is designed to support both new and existing hardware, from DirectX 9 to DirectX 11.</span></span>

<span data-ttu-id="d80b9-105">Este diagrama mostra como o Direct3D 11 dá suporte a hardware novo e existente.</span><span class="sxs-lookup"><span data-stu-id="d80b9-105">This diagram shows how Direct3D 11 supports new and existing hardware.</span></span>

![diagrama do hardware ao qual o Direct3D 11 dá suporte](images/d3d11-on-downlevel-hardware.png)

<span data-ttu-id="d80b9-107">Com o Direct3D 11, é introduzido um novo paradigma chamado níveis de recursos.</span><span class="sxs-lookup"><span data-stu-id="d80b9-107">With Direct3D 11, a new paradigm is introduced called feature levels.</span></span> <span data-ttu-id="d80b9-108">Um nível de recurso é um conjunto bem definido de funcionalidades de GPU.</span><span class="sxs-lookup"><span data-stu-id="d80b9-108">A feature level is a well defined set of GPU functionality.</span></span> <span data-ttu-id="d80b9-109">Usando um nível de recurso, você pode direcionar um aplicativo Direct3D para ser executado em uma versão de nível inferior do hardware do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d80b9-109">Using a feature level, you can target a Direct3D application to run on a downlevel version of Direct3D hardware.</span></span>

<span data-ttu-id="d80b9-110">A seção de [referência do 10Level9](d3d11-graphics-reference-10level9.md) lista as diferenças entre o comportamento de vários métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) em vários níveis de recursos do 10Level9.</span><span class="sxs-lookup"><span data-stu-id="d80b9-110">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="d80b9-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d80b9-111">In this section</span></span>



| <span data-ttu-id="d80b9-112">Tópico</span><span class="sxs-lookup"><span data-stu-id="d80b9-112">Topic</span></span>                                                                                                                  | <span data-ttu-id="d80b9-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="d80b9-113">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d80b9-114">Níveis de recursos do Direct3D</span><span class="sxs-lookup"><span data-stu-id="d80b9-114">Direct3D feature levels</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | <span data-ttu-id="d80b9-115">Este tópico discute os níveis de recurso do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d80b9-115">This topic discusses Direct3D feature levels.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="d80b9-116">Exceções</span><span class="sxs-lookup"><span data-stu-id="d80b9-116">Exceptions</span></span>](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | <span data-ttu-id="d80b9-117">Este tópico descreve as exceções ao usar o Direct3D 11 em hardware de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="d80b9-117">This topic describes exceptions when using Direct3D 11 on downlevel hardware.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="d80b9-118">Sombreadores de computação em hardware de nível inferior</span><span class="sxs-lookup"><span data-stu-id="d80b9-118">Compute Shaders on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | <span data-ttu-id="d80b9-119">Este tópico discute como usar [sombreadores de computação](direct3d-11-advanced-stages-compute-shader.md) em um aplicativo do Direct3D 11 no hardware do Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="d80b9-119">This topic discusses how to make use of [compute shaders](direct3d-11-advanced-stages-compute-shader.md) in a Direct3D 11 app on Direct3D 10 hardware.</span></span><br/>             |
| [<span data-ttu-id="d80b9-120">Impedindo SRVs de sombreador de pixel nulo indesejado</span><span class="sxs-lookup"><span data-stu-id="d80b9-120">Preventing Unwanted NULL Pixel Shader SRVs</span></span>](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | <span data-ttu-id="d80b9-121">Este tópico discute como contornar o driver recebendo exibições de recurso de sombreador **nulo** (SRVs) mesmo quando SRVs não **nulo** estão associados ao estágio de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="d80b9-121">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span><br/> |



 

## <a name="how-to-topics-about-feature-levels"></a><span data-ttu-id="d80b9-122">Tópicos sobre como obter os níveis de recurso</span><span class="sxs-lookup"><span data-stu-id="d80b9-122">How to topics about feature levels</span></span>



| <span data-ttu-id="d80b9-123">Tópico</span><span class="sxs-lookup"><span data-stu-id="d80b9-123">Topic</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="d80b9-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="d80b9-124">Description</span></span>                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="d80b9-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Como: obter o nível de recurso do dispositivo](overviews-direct3d-11-devices-downlevel-get.md)</span><span class="sxs-lookup"><span data-stu-id="d80b9-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[How To: Get the Device Feature Level](overviews-direct3d-11-devices-downlevel-get.md)</span></span><br/> | <span data-ttu-id="d80b9-126">Como obter um nível de recurso.</span><span class="sxs-lookup"><span data-stu-id="d80b9-126">How to get a feature level.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="d80b9-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d80b9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d80b9-128">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="d80b9-128">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 






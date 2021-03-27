---
title: Como obter o nível de recurso do dispositivo
description: Este tópico mostra como obter o nível de recurso mais alto com suporte de um dispositivo.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e587ad488a84641a92f0058d201014030e3467e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822910"
---
# <a name="how-to-get-the-device-feature-level"></a><span data-ttu-id="572c0-103">Como: obter o nível de recurso do dispositivo</span><span class="sxs-lookup"><span data-stu-id="572c0-103">How To: Get the Device Feature Level</span></span>

<span data-ttu-id="572c0-104">Este tópico mostra como obter o nível de [recurso](overviews-direct3d-11-devices-downlevel-intro.md) mais alto com suporte de um [dispositivo](overviews-direct3d-11-devices-intro.md).</span><span class="sxs-lookup"><span data-stu-id="572c0-104">This topics shows how to get the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a [device](overviews-direct3d-11-devices-intro.md).</span></span> <span data-ttu-id="572c0-105">Os dispositivos do Direct3D 11 dão suporte a um conjunto fixo de níveis de recursos que são definidos na enumeração de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="572c0-105">Direct3D 11 devices support a fixed set of feature levels that are defined in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span> <span data-ttu-id="572c0-106">Quando você souber o [nível de recurso](overviews-direct3d-11-devices-downlevel-intro.md) mais alto com suporte de um dispositivo, poderá executar caminhos de código apropriados para esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="572c0-106">When you know the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a device, you can run code paths that are appropriate for that device.</span></span>

<span data-ttu-id="572c0-107">**Para obter o nível de recurso do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="572c0-107">**To get the device feature level**</span></span>

1.  <span data-ttu-id="572c0-108">Chame a função [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou as funções [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) ao especificar **NULL** para o parâmetro *ppDevice* .</span><span class="sxs-lookup"><span data-stu-id="572c0-108">Call either the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) functions while specifying **NULL** for the *ppDevice* parameter.</span></span> <span data-ttu-id="572c0-109">Você pode fazer isso antes da criação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="572c0-109">You can do this before device creation.</span></span>

    <span data-ttu-id="572c0-110">\- ou –</span><span class="sxs-lookup"><span data-stu-id="572c0-110">\- or -</span></span>

    <span data-ttu-id="572c0-111">Chame [**ID3D11Device:: GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) após a criação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="572c0-111">Call [**ID3D11Device::GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) after device creation.</span></span>

2.  <span data-ttu-id="572c0-112">Examine o valor da enumeração de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) retornado da última etapa para determinar o nível de recurso com suporte.</span><span class="sxs-lookup"><span data-stu-id="572c0-112">Examine the value of the returned [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration from the last step to determine the supported feature level.</span></span>

<span data-ttu-id="572c0-113">O exemplo de código a seguir demonstra como determinar o nível de recurso com suporte mais alto chamando a função [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) .</span><span class="sxs-lookup"><span data-stu-id="572c0-113">The following code example demonstrates how to determine the highest supported feature level by calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function.</span></span> <span data-ttu-id="572c0-114">O **D3D11CreateDevice** armazena o nível de recurso mais alto com suporte na variável nível.</span><span class="sxs-lookup"><span data-stu-id="572c0-114">**D3D11CreateDevice** stores the highest supported feature level in the FeatureLevel variable.</span></span> <span data-ttu-id="572c0-115">Você pode usar esse código para examinar o valor do tipo enumerado de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) que **D3D11CreateDevice** retorna.</span><span class="sxs-lookup"><span data-stu-id="572c0-115">You can use this code to examine the value of the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumerated type that **D3D11CreateDevice** returns.</span></span> <span data-ttu-id="572c0-116">Observe que esse código lista todos os níveis de recursos explicitamente (para Direct3D 11,1 e Direct3D 11,2).</span><span class="sxs-lookup"><span data-stu-id="572c0-116">Note that this code lists all feature levels explicitly (for Direct3D 11.1 and Direct3D 11.2).</span></span>

> [!Note]  
> <span data-ttu-id="572c0-117">Se o tempo de execução do Direct3D 11,1 estiver presente no computador e *pFeatureLevels* estiver definido como **NULL**, essa função não criará um dispositivo de nível de [**recurso do D3D \_ \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="572c0-117">If the Direct3D 11.1 runtime is present on the computer and *pFeatureLevels* is set to **NULL**, this function won't create a [**D3D\_FEATURE\_LEVEL\_11\_1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) device.</span></span> <span data-ttu-id="572c0-118">Para criar um dispositivo de **nível de recurso do D3D \_ \_ \_ 11 \_ 1** , você deve fornecer explicitamente uma matriz de **nível de \_ recurso \_ do D3D** que inclua o **nível de recurso do D3D \_ \_ \_ 11 \_ 1**.</span><span class="sxs-lookup"><span data-stu-id="572c0-118">To create a **D3D\_FEATURE\_LEVEL\_11\_1** device, you must explicitly provide a **D3D\_FEATURE\_LEVEL** array that includes **D3D\_FEATURE\_LEVEL\_11\_1**.</span></span> <span data-ttu-id="572c0-119">Se você fornecer uma matriz de **\_ \_ nível de recurso do D3D** que contém o nível de recurso do **D3D \_ \_ \_ 11 \_ 1** em um computador que não tem o tempo de execução do Direct3D 11,1 instalado, essa função falhará imediatamente com E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="572c0-119">If you provide a **D3D\_FEATURE\_LEVEL** array that contains **D3D\_FEATURE\_LEVEL\_11\_1** on a computer that doesn't have the Direct3D 11.1 runtime installed, this function immediately fails with E\_INVALIDARG.</span></span>

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



<span data-ttu-id="572c0-120">A seção de [referência do 10Level9](d3d11-graphics-reference-10level9.md) lista as diferenças entre o comportamento de vários métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) em vários níveis de recursos do 10Level9.</span><span class="sxs-lookup"><span data-stu-id="572c0-120">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="572c0-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="572c0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="572c0-122">Direct3D 11 em hardware de nível inferior</span><span class="sxs-lookup"><span data-stu-id="572c0-122">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[<span data-ttu-id="572c0-123">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="572c0-123">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 





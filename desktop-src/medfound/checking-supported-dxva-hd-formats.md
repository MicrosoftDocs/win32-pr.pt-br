---
description: Verificando os formatos de DXVA-HD com suporte
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Verificando os formatos de DXVA-HD com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07d47043ed200d256e2bef8fa2c9ab6717f3b82
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090004"
---
# <a name="checking-supported-dxva-hd-formats"></a><span data-ttu-id="d5118-103">Verificando os formatos de DXVA-HD com suporte</span><span class="sxs-lookup"><span data-stu-id="d5118-103">Checking Supported DXVA-HD Formats</span></span>

## <a name="checking-supported-input-formats"></a><span data-ttu-id="d5118-104">Verificando formatos de entrada com suporte</span><span class="sxs-lookup"><span data-stu-id="d5118-104">Checking Supported Input Formats</span></span>

<span data-ttu-id="d5118-105">Para obter uma lista dos formatos de entrada para os quais o dispositivo de alta definição de aceleração de vídeo do Microsoft DirectX (DXVA-HD) dá suporte, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d5118-105">To get a list of the input formats that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports, do the following:</span></span>

1.  <span data-ttu-id="d5118-106">Chame [**o \_ dispositivo IDXVAHD:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) para obter os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5118-106">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="d5118-107">Verifique o membro **InputFormatCount** da estrutura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="d5118-107">Check the **InputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="d5118-108">Esse membro fornece o número de formatos de entrada com suporte.</span><span class="sxs-lookup"><span data-stu-id="d5118-108">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="d5118-109">Aloque uma matriz de valores **D3DFORMAT** , de tamanho **InputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="d5118-109">Allocate an array of **D3DFORMAT** values, of size **InputFormatCount**.</span></span>
4.  <span data-ttu-id="d5118-110">Passe essa matriz para o método [**IDXVAHD \_ Device:: GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) .</span><span class="sxs-lookup"><span data-stu-id="d5118-110">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) method.</span></span> <span data-ttu-id="d5118-111">Os métodos preenchem a matriz com uma lista de formatos de entrada.</span><span class="sxs-lookup"><span data-stu-id="d5118-111">The methods fills the array with a list of input formats.</span></span>

<span data-ttu-id="d5118-112">O código a seguir mostra essas etapas:</span><span class="sxs-lookup"><span data-stu-id="d5118-112">The following code shows these steps:</span></span>


```C++
// Checks whether a DXVA-HD device supports a specified input format.

HRESULT CheckInputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[ caps.InputFormatCount ];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorInputFormats(
        caps.InputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.InputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.InputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="checking-supported-output-formats"></a><span data-ttu-id="d5118-113">Verificando formatos de saída com suporte</span><span class="sxs-lookup"><span data-stu-id="d5118-113">Checking Supported Output Formats</span></span>

<span data-ttu-id="d5118-114">Para obter uma lista dos formatos de saída aos quais o dispositivo DXVA-HD dá suporte, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d5118-114">To get a list of the output formats that the DXVA-HD device supports, do the following:</span></span>

1.  <span data-ttu-id="d5118-115">Chame [**o \_ dispositivo IDXVAHD:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) para obter os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5118-115">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="d5118-116">Verifique o membro **OutputFormatCount** da estrutura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="d5118-116">Check the **OutputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="d5118-117">Esse membro fornece o número de formatos de entrada com suporte.</span><span class="sxs-lookup"><span data-stu-id="d5118-117">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="d5118-118">Aloque uma matriz de valores **D3DFORMAT** , de tamanho **OutputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="d5118-118">Allocate an array of **D3DFORMAT** values, of size **OutputFormatCount**.</span></span>
4.  <span data-ttu-id="d5118-119">Passe essa matriz para o método [**IDXVAHD \_ Device:: GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) .</span><span class="sxs-lookup"><span data-stu-id="d5118-119">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) method.</span></span> <span data-ttu-id="d5118-120">Os métodos preenchem a matriz com uma lista de formatos de saída.</span><span class="sxs-lookup"><span data-stu-id="d5118-120">The methods fills the array with a list of output formats.</span></span>

<span data-ttu-id="d5118-121">O código a seguir mostra essas etapas:</span><span class="sxs-lookup"><span data-stu-id="d5118-121">The following code shows these steps:</span></span>


```C++
// Checks whether a DXVA-HD device supports a specified output format.

HRESULT CheckOutputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[caps.OutputFormatCount];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorOutputFormats(
        caps.OutputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.OutputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.OutputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d5118-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5118-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5118-123">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="d5118-123">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 




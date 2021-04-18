---
description: Método virtual puro que as classes derivadas substituem.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: Método CBaseControlVideo. GetStaticImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13b0515e20202373954050b6fa18f10a20a76a6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752915"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a><span data-ttu-id="1f260-103">Método CBaseControlVideo. GetStaticImage</span><span class="sxs-lookup"><span data-stu-id="1f260-103">CBaseControlVideo.GetStaticImage method</span></span>

<span data-ttu-id="1f260-104">Método virtual puro que as classes derivadas substituem.</span><span class="sxs-lookup"><span data-stu-id="1f260-104">Pure virtual method that derived classes override.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f260-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f260-105">Syntax</span></span>


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="1f260-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f260-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f260-107">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="1f260-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="1f260-108">Ponteiro para o tamanho do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="1f260-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1f260-109">*pDIBImage*</span><span class="sxs-lookup"><span data-stu-id="1f260-109">*pDIBImage*</span></span> 
</dt> <dd>

<span data-ttu-id="1f260-110">Ponteiro para o buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="1f260-110">Pointer to the output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f260-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f260-111">Return value</span></span>

<span data-ttu-id="1f260-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f260-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f260-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f260-113">Remarks</span></span>

<span data-ttu-id="1f260-114">Por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) , um aplicativo pode solicitar que ele receba uma cópia da imagem atual em um buffer de memória (alguns renderizadores podem retornar E \_ NOTIMPL para isso se não suportarem isso).</span><span class="sxs-lookup"><span data-stu-id="1f260-114">Through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface, an application can request that it be given a copy of the current image in a memory buffer (some renderers can return E\_NOTIMPL to this if they do not support it).</span></span> <span data-ttu-id="1f260-115">A classe derivada determina como recuperar a imagem.</span><span class="sxs-lookup"><span data-stu-id="1f260-115">The derived class determines how to retrieve the image.</span></span> <span data-ttu-id="1f260-116">Quando o aplicativo chama **CBaseControlVideo:: GetStaticImage**, ele chama esse método virtual puro que a classe derivada deve substituir para implementá-lo.</span><span class="sxs-lookup"><span data-stu-id="1f260-116">When the application calls **CBaseControlVideo::GetStaticImage**, it calls this pure virtual method that the derived class should override to implement it.</span></span> <span data-ttu-id="1f260-117">Isso também é chamado pela função de membro [**CBaseControlVideo:: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) .</span><span class="sxs-lookup"><span data-stu-id="1f260-117">This is also called by the [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) member function.</span></span>

<span data-ttu-id="1f260-118">A classe fornece uma função de membro auxiliar, [**CBaseControlVideo:: CopyImage**](cbasecontrolvideo-copyimage.md), que pode receber um exemplo que contém uma imagem, e a função de membro copiará a seção relevante dela (com base no retângulo de origem atual) para o buffer de saída fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1f260-118">The class provides a helper member function, [**CBaseControlVideo::CopyImage**](cbasecontrolvideo-copyimage.md), that can be given a sample that contains an image, and the member function will copy the relevant section of it (based on the current source rectangle) into the output buffer supplied by the application.</span></span>

<span data-ttu-id="1f260-119">O exemplo a seguir demonstra uma implementação dessa função de membro em uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="1f260-119">The following example demonstrates an implementation of this member function in a derived class.</span></span> <span data-ttu-id="1f260-120">Neste exemplo, m \_ pRenderer mantém um objeto de uma classe derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md).</span><span class="sxs-lookup"><span data-stu-id="1f260-120">In this example, m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md).</span></span>


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="1f260-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f260-121">Requirements</span></span>



| <span data-ttu-id="1f260-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f260-122">Requirement</span></span> | <span data-ttu-id="1f260-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1f260-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f260-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f260-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1f260-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f260-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1f260-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f260-126">Library</span></span><br/> | <dl> <span data-ttu-id="1f260-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1f260-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f260-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f260-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f260-129">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="1f260-129">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





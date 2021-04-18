---
description: O método IsDefaultSourceRect determina se o renderizador está usando o retângulo de origem padrão (virtual puro).
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: Método CBaseControlVideo. IsDefaultSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 390ae779eaa7d640d23b40a7e6f6579e158bf6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753365"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a><span data-ttu-id="6a1fa-103">Método CBaseControlVideo. IsDefaultSourceRect</span><span class="sxs-lookup"><span data-stu-id="6a1fa-103">CBaseControlVideo.IsDefaultSourceRect method</span></span>

<span data-ttu-id="6a1fa-104">O `IsDefaultSourceRect` método determina se o renderizador está usando o retângulo de origem padrão (virtual puro).</span><span class="sxs-lookup"><span data-stu-id="6a1fa-104">The `IsDefaultSourceRect` method determines if the renderer is using the default source rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a1fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a1fa-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="6a1fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a1fa-106">Parameters</span></span>

<span data-ttu-id="6a1fa-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6a1fa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a1fa-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a1fa-108">Return value</span></span>

<span data-ttu-id="6a1fa-109">Retornará S \_ OK se o renderizador estiver usando a origem padrão; caso contrário, retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="6a1fa-109">Returns S\_OK if the renderer is using the default source; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a1fa-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a1fa-110">Remarks</span></span>

<span data-ttu-id="6a1fa-111">Essa função de membro deve ser implementada na classe derivada.</span><span class="sxs-lookup"><span data-stu-id="6a1fa-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="6a1fa-112">Ele é chamado pela função de membro [**CBaseControlVideo:: IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) .</span><span class="sxs-lookup"><span data-stu-id="6a1fa-112">It is called by the [**CBaseControlVideo::IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) member function.</span></span>

<span data-ttu-id="6a1fa-113">O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="6a1fa-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default source; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultSourceRect()
{
    RECT SourceRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetSourceRect(&SourceRect);

    // Check the coordinates that match the video dimensions.

    if (SourceRect.left != 0 || SourceRect.top != 0 ||
            SourceRect.right != pHeader->biWidth ||
                SourceRect.bottom != pHeader->biHeight) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="6a1fa-114">Neste exemplo, CVideoText é uma classe derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer mantém um objeto de uma classe derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md), e o membro de \_ dados da DrawImage m, definido na classe derivada, mantém um objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="6a1fa-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="6a1fa-115">O \_ membro de dados m mtIn, também definido na classe derivada, mantém um objeto [**CMediaType**](cmediatype.md) com o tipo de mídia do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="6a1fa-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with the media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a1fa-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a1fa-116">Requirements</span></span>



| <span data-ttu-id="6a1fa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a1fa-117">Requirement</span></span> | <span data-ttu-id="6a1fa-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6a1fa-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1fa-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a1fa-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6a1fa-120"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a1fa-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6a1fa-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a1fa-121">Library</span></span><br/> | <dl> <span data-ttu-id="6a1fa-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6a1fa-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a1fa-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a1fa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a1fa-124">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="6a1fa-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





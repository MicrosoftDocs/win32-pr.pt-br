---
description: O método IsDefaultTargetRect determina se o renderizador está usando o retângulo de destino padrão (virtual puro).
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Método CBaseControlVideo. IsDefaultTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e267cc65345d18800beccbc80ac7952c89d781d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749856"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a><span data-ttu-id="35ec1-103">Método CBaseControlVideo. IsDefaultTargetRect</span><span class="sxs-lookup"><span data-stu-id="35ec1-103">CBaseControlVideo.IsDefaultTargetRect method</span></span>

<span data-ttu-id="35ec1-104">O `IsDefaultTargetRect` método determina se o renderizador está usando o retângulo de destino padrão (virtual puro).</span><span class="sxs-lookup"><span data-stu-id="35ec1-104">The `IsDefaultTargetRect` method determines if the renderer is using the default target rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="35ec1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35ec1-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="35ec1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35ec1-106">Parameters</span></span>

<span data-ttu-id="35ec1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="35ec1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35ec1-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35ec1-108">Return value</span></span>

<span data-ttu-id="35ec1-109">Retornará S \_ OK se o renderizador estiver usando o destino padrão; caso contrário, retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="35ec1-109">Returns S\_OK if the renderer is using the default target; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ec1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="35ec1-110">Remarks</span></span>

<span data-ttu-id="35ec1-111">Essa função de membro deve ser implementada na classe derivada.</span><span class="sxs-lookup"><span data-stu-id="35ec1-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="35ec1-112">Ele é chamado pela função de membro [**CBaseControlVideo:: IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) .</span><span class="sxs-lookup"><span data-stu-id="35ec1-112">It is called by the [**CBaseControlVideo::IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) member function.</span></span>

<span data-ttu-id="35ec1-113">O exemplo a seguir demonstra uma implementação dessa função em uma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="35ec1-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default target; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultTargetRect()
{
    RECT TargetRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetTargetRect(&TargetRect);

    // Check the destination that matches the initial client area.

    if (TargetRect.left != 0 || TargetRect.top != 0 ||
            TargetRect.right != m_Size.cx ||
                TargetRect.bottom != m_Size.cy) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="35ec1-114">Neste exemplo, CVideoText é uma classe derivada de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer mantém um objeto de uma classe derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md), e o membro de \_ dados da DrawImage m, definido na classe derivada, mantém um objeto [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="35ec1-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="35ec1-115">O \_ membro de dados m mtIn, também definido na classe derivada, mantém um objeto [**CMediaType**](cmediatype.md) com o tipo de mídia do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="35ec1-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ec1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35ec1-116">Requirements</span></span>



| <span data-ttu-id="35ec1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ec1-117">Requirement</span></span> | <span data-ttu-id="35ec1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="35ec1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ec1-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35ec1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="35ec1-120"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35ec1-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="35ec1-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35ec1-121">Library</span></span><br/> | <dl> <span data-ttu-id="35ec1-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="35ec1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ec1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="35ec1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ec1-124">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="35ec1-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 





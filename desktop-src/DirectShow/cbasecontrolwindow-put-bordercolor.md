---
description: O \_ método Put BorderColor altera a cor da borda.
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: Método de CBaseControlWindow.put_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751279"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a><span data-ttu-id="b3287-103">Método BorderColor CBaseControlWindow. put \_</span><span class="sxs-lookup"><span data-stu-id="b3287-103">CBaseControlWindow.put\_BorderColor method</span></span>

<span data-ttu-id="b3287-104">O `put_BorderColor` método altera a cor da borda.</span><span class="sxs-lookup"><span data-stu-id="b3287-104">The `put_BorderColor` method changes the border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3287-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3287-105">Syntax</span></span>


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a><span data-ttu-id="b3287-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3287-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3287-107">*Cor*</span><span class="sxs-lookup"><span data-stu-id="b3287-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="b3287-108">Nova cor da borda.</span><span class="sxs-lookup"><span data-stu-id="b3287-108">New border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3287-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3287-109">Return value</span></span>

<span data-ttu-id="b3287-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b3287-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3287-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3287-111">Remarks</span></span>

<span data-ttu-id="b3287-112">Um aplicativo pode estabelecer um retângulo de destino no qual o vídeo deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="b3287-112">An application can establish a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="b3287-113">Esse retângulo é relativo à área do cliente para a janela.</span><span class="sxs-lookup"><span data-stu-id="b3287-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="b3287-114">Se isso for feito (o padrão é sempre pintar toda a janela), haverá uma borda ao redor do vídeo.</span><span class="sxs-lookup"><span data-stu-id="b3287-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="b3287-115">Essa propriedade afeta a cor usada pela borda.</span><span class="sxs-lookup"><span data-stu-id="b3287-115">This property affects the color used by the border.</span></span> <span data-ttu-id="b3287-116">Embora o parâmetro seja especificado como um tipo **longo** , na verdade ele é um valor **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="b3287-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3287-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3287-117">Requirements</span></span>



| <span data-ttu-id="b3287-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3287-118">Requirement</span></span> | <span data-ttu-id="b3287-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b3287-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3287-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3287-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b3287-121"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3287-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b3287-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3287-122">Library</span></span><br/> | <dl> <span data-ttu-id="b3287-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b3287-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3287-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3287-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3287-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="b3287-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





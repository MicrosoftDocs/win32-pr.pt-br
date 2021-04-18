---
description: O \_ método Get Caption recupera a legenda da janela atual.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: Método de CBaseControlWindow.get_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8d743c746f833007d91afd4346f7f48c6218dde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752113"
---
# <a name="cbasecontrolwindowget_caption-method"></a><span data-ttu-id="c5bb0-103">Método de legenda CBaseControlWindow. get \_</span><span class="sxs-lookup"><span data-stu-id="c5bb0-103">CBaseControlWindow.get\_Caption method</span></span>

<span data-ttu-id="c5bb0-104">O `get_Caption` método recupera a legenda da janela atual.</span><span class="sxs-lookup"><span data-stu-id="c5bb0-104">The `get_Caption` method retrieves the current window caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5bb0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5bb0-105">Syntax</span></span>


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a><span data-ttu-id="c5bb0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5bb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5bb0-107">*pstrCaption*</span><span class="sxs-lookup"><span data-stu-id="c5bb0-107">*pstrCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="c5bb0-108">Ponteiro para a legenda da janela atual.</span><span class="sxs-lookup"><span data-stu-id="c5bb0-108">Pointer to the current window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5bb0-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5bb0-109">Return value</span></span>

<span data-ttu-id="c5bb0-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c5bb0-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5bb0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5bb0-111">Remarks</span></span>

<span data-ttu-id="c5bb0-112">A maioria das janelas de nível superior em uma área de trabalho baseada no Windows tem um título (legenda) associado a elas.</span><span class="sxs-lookup"><span data-stu-id="c5bb0-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="c5bb0-113">Essa propriedade pode ser consultada e definida por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="c5bb0-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="c5bb0-114">Qualquer conjunto de legendas será visível somente se a janela tiver o \_ estilo de legenda WS aplicado.</span><span class="sxs-lookup"><span data-stu-id="c5bb0-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="c5bb0-115">Se não tiver, a legenda ainda poderá ser definida (e recuperada), embora não seja visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="c5bb0-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5bb0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5bb0-116">Requirements</span></span>



| <span data-ttu-id="c5bb0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5bb0-117">Requirement</span></span> | <span data-ttu-id="c5bb0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c5bb0-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5bb0-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5bb0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c5bb0-120"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5bb0-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c5bb0-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5bb0-121">Library</span></span><br/> | <dl> <span data-ttu-id="c5bb0-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c5bb0-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5bb0-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5bb0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5bb0-124">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="c5bb0-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





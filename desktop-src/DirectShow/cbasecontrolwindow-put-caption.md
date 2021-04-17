---
description: O \_ método Put Caption define o título ou a legenda da janela.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: Método de CBaseControlWindow.put_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749855"
---
# <a name="cbasecontrolwindowput_caption-method"></a><span data-ttu-id="7afdd-103">Método de legenda CBaseControlWindow. put \_</span><span class="sxs-lookup"><span data-stu-id="7afdd-103">CBaseControlWindow.put\_Caption method</span></span>

<span data-ttu-id="7afdd-104">O `put_Caption` método define o título ou a legenda da janela.</span><span class="sxs-lookup"><span data-stu-id="7afdd-104">The `put_Caption` method sets the window title or caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="7afdd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7afdd-105">Syntax</span></span>


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a><span data-ttu-id="7afdd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7afdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7afdd-107">*strCaption*</span><span class="sxs-lookup"><span data-stu-id="7afdd-107">*strCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="7afdd-108">Nova legenda da janela.</span><span class="sxs-lookup"><span data-stu-id="7afdd-108">New window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7afdd-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7afdd-109">Return value</span></span>

<span data-ttu-id="7afdd-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7afdd-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7afdd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7afdd-111">Remarks</span></span>

<span data-ttu-id="7afdd-112">A maioria das janelas de nível superior em uma área de trabalho baseada no Windows tem um título (legenda) associado a elas.</span><span class="sxs-lookup"><span data-stu-id="7afdd-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="7afdd-113">Essa propriedade pode ser consultada e definida por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="7afdd-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="7afdd-114">Qualquer conjunto de legendas será visível somente se a janela tiver o \_ estilo de legenda WS aplicado.</span><span class="sxs-lookup"><span data-stu-id="7afdd-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="7afdd-115">Se não tiver, a legenda ainda poderá ser definida (e recuperada), embora não seja visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="7afdd-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="7afdd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7afdd-116">Requirements</span></span>



| <span data-ttu-id="7afdd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7afdd-117">Requirement</span></span> | <span data-ttu-id="7afdd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7afdd-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7afdd-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7afdd-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7afdd-120"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7afdd-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7afdd-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7afdd-121">Library</span></span><br/> | <dl> <span data-ttu-id="7afdd-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7afdd-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7afdd-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7afdd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7afdd-124">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="7afdd-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 





---
description: Ocorre quando a posição da seleção atual é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: Evento InkOverlay. SelectionMoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f254b5e3ae3c23f50b12c097608946aad3b3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297382"
---
# <a name="inkoverlayselectionmoved-event"></a><span data-ttu-id="5ebbe-103">Evento InkOverlay. SelectionMoved</span><span class="sxs-lookup"><span data-stu-id="5ebbe-103">InkOverlay.SelectionMoved event</span></span>

<span data-ttu-id="5ebbe-104">Ocorre quando a posição da seleção atual é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="5ebbe-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ebbe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ebbe-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="5ebbe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ebbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ebbe-107">*OldSelectionRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ebbe-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ebbe-108">O retângulo delimitador da coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selecionada como existia antes de o evento **SelectionMoved** ser acionado.</span><span class="sxs-lookup"><span data-stu-id="5ebbe-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="5ebbe-109">Esse retângulo é especificado em coordenadas de espaço de tinta, o que permite cenários de desfazer.</span><span class="sxs-lookup"><span data-stu-id="5ebbe-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ebbe-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ebbe-110">Return value</span></span>

<span data-ttu-id="5ebbe-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5ebbe-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ebbe-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ebbe-112">Remarks</span></span>

<span data-ttu-id="5ebbe-113">O método de evento este é definido nas \_ interfaces somente de expedição de IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de \_ IOESelectionMoved DISPID.</span><span class="sxs-lookup"><span data-stu-id="5ebbe-113">TThis event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="5ebbe-114">Para obter o novo retângulo delimitador da coleção de traços que foram movidos, chame o método [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) .</span><span class="sxs-lookup"><span data-stu-id="5ebbe-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ebbe-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ebbe-115">Requirements</span></span>



| <span data-ttu-id="5ebbe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ebbe-116">Requirement</span></span> | <span data-ttu-id="5ebbe-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5ebbe-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebbe-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ebbe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5ebbe-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5ebbe-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5ebbe-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ebbe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5ebbe-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5ebbe-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5ebbe-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ebbe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ebbe-123"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5ebbe-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5ebbe-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ebbe-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ebbe-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ebbe-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5ebbe-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ebbe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebbe-127">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="5ebbe-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="5ebbe-128">**Propriedade de seleção**</span><span class="sxs-lookup"><span data-stu-id="5ebbe-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="5ebbe-129">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="5ebbe-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 


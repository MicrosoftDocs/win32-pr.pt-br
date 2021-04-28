---
description: Evento InkOverlay. SelectionMoved-ocorre quando a posição da seleção atual é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: Evento InkOverlay. SelectionMoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27bf1600683b5258bf899692b692c8cdcabb359
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116864"
---
# <a name="inkoverlayselectionmoved-event"></a><span data-ttu-id="4274d-103">Evento InkOverlay. SelectionMoved</span><span class="sxs-lookup"><span data-stu-id="4274d-103">InkOverlay.SelectionMoved event</span></span>

<span data-ttu-id="4274d-104">Ocorre quando a posição da seleção atual é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="4274d-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4274d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4274d-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="4274d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4274d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4274d-107">*OldSelectionRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4274d-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4274d-108">O retângulo delimitador da coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selecionada como existia antes de o evento **SelectionMoved** ser acionado.</span><span class="sxs-lookup"><span data-stu-id="4274d-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="4274d-109">Esse retângulo é especificado em coordenadas de espaço de tinta, o que permite cenários de desfazer.</span><span class="sxs-lookup"><span data-stu-id="4274d-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4274d-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4274d-110">Return value</span></span>

<span data-ttu-id="4274d-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4274d-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4274d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4274d-112">Remarks</span></span>

<span data-ttu-id="4274d-113">O método de evento este é definido nas \_ interfaces somente de expedição de IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de \_ IOESelectionMoved DISPID.</span><span class="sxs-lookup"><span data-stu-id="4274d-113">TThis event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="4274d-114">Para obter o novo retângulo delimitador da coleção de traços que foram movidos, chame o método [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) .</span><span class="sxs-lookup"><span data-stu-id="4274d-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4274d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4274d-115">Requirements</span></span>



| <span data-ttu-id="4274d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4274d-116">Requirement</span></span> | <span data-ttu-id="4274d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4274d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4274d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4274d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4274d-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4274d-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4274d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4274d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4274d-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4274d-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4274d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4274d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4274d-123"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4274d-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4274d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4274d-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="4274d-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4274d-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4274d-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4274d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4274d-127">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="4274d-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="4274d-128">**Propriedade de seleção**</span><span class="sxs-lookup"><span data-stu-id="4274d-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="4274d-129">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="4274d-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 


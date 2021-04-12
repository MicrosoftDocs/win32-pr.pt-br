---
description: Ocorre quando a posição da seleção atual é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: 669dc6c2-1620-40f3-b4b5-7ab8967e739a
title: Evento InkPicture. SelectionMoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25810b87d5a0a3554c46b1a3869bb9b6c88d2fb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297024"
---
# <a name="inkpictureselectionmoved-event"></a><span data-ttu-id="04d54-103">Evento InkPicture. SelectionMoved</span><span class="sxs-lookup"><span data-stu-id="04d54-103">InkPicture.SelectionMoved event</span></span>

<span data-ttu-id="04d54-104">Ocorre quando a posição da seleção atual é alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="04d54-104">Occurs when the position of the current selection has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d54-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04d54-105">Syntax</span></span>


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="04d54-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04d54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d54-107">*OldSelectionRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04d54-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04d54-108">O retângulo delimitador da coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selecionada como existia antes de o evento **SelectionMoved** ser acionado.</span><span class="sxs-lookup"><span data-stu-id="04d54-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionMoved** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="04d54-109">Esse retângulo é especificado em coordenadas de espaço de tinta, o que permite cenários de desfazer.</span><span class="sxs-lookup"><span data-stu-id="04d54-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04d54-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04d54-110">Return value</span></span>

<span data-ttu-id="04d54-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="04d54-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04d54-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="04d54-112">Remarks</span></span>

<span data-ttu-id="04d54-113">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de DISPID \_ IOESelectionMoved.</span><span class="sxs-lookup"><span data-stu-id="04d54-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoved.</span></span>

<span data-ttu-id="04d54-114">Para obter o novo retângulo delimitador da coleção de traços que foram movidos, chame o método [**Selection. GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) .</span><span class="sxs-lookup"><span data-stu-id="04d54-114">To get the new bounding rectangle of the collection of strokes that have been moved, call the [**Selection.GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="04d54-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04d54-115">Requirements</span></span>



| <span data-ttu-id="04d54-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="04d54-116">Requirement</span></span> | <span data-ttu-id="04d54-117">Valor</span><span class="sxs-lookup"><span data-stu-id="04d54-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04d54-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04d54-118">Minimum supported client</span></span><br/> | <span data-ttu-id="04d54-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="04d54-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="04d54-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04d54-120">Minimum supported server</span></span><br/> | <span data-ttu-id="04d54-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="04d54-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="04d54-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04d54-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="04d54-123"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="04d54-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="04d54-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04d54-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="04d54-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04d54-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="04d54-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="04d54-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d54-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="04d54-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="04d54-128">[**Controle de propriedade de seleção \[ InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="04d54-128">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="04d54-129">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="04d54-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 


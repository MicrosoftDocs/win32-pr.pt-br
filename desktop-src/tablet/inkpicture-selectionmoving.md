---
description: Evento InkPicture. SelectionMoving – ocorre quando a posição da seleção atual está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: Evento InkPicture. SelectionMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eee50fe1115ce72dff0674ad4e6c2457500c7de8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086454"
---
# <a name="inkpictureselectionmoving-event"></a><span data-ttu-id="79e24-103">Evento InkPicture. SelectionMoving</span><span class="sxs-lookup"><span data-stu-id="79e24-103">InkPicture.SelectionMoving event</span></span>

<span data-ttu-id="79e24-104">Ocorre quando a posição da seleção atual está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="79e24-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e24-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79e24-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="79e24-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79e24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79e24-107">*CurSelectionRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79e24-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e24-108">O retângulo para o qual a seleção é movida após o evento **SelectionMoving** .</span><span class="sxs-lookup"><span data-stu-id="79e24-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="79e24-109">Esse retângulo é especificado em coordenadas da janela do cliente, o que permite cenários como manter a taxa de proporção ao redimensionar.</span><span class="sxs-lookup"><span data-stu-id="79e24-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79e24-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="79e24-110">Return value</span></span>

<span data-ttu-id="79e24-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="79e24-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79e24-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="79e24-112">Remarks</span></span>

<span data-ttu-id="79e24-113">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de DISPID \_ IOESelectionMoving.</span><span class="sxs-lookup"><span data-stu-id="79e24-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="79e24-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79e24-114">Requirements</span></span>



| <span data-ttu-id="79e24-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="79e24-115">Requirement</span></span> | <span data-ttu-id="79e24-116">Valor</span><span class="sxs-lookup"><span data-stu-id="79e24-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79e24-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79e24-117">Minimum supported client</span></span><br/> | <span data-ttu-id="79e24-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="79e24-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="79e24-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79e24-119">Minimum supported server</span></span><br/> | <span data-ttu-id="79e24-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="79e24-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="79e24-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79e24-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="79e24-122"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="79e24-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="79e24-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79e24-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="79e24-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e24-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="79e24-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="79e24-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e24-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="79e24-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="79e24-127">[**Controle de propriedade de seleção \[ InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="79e24-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="79e24-128">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="79e24-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 





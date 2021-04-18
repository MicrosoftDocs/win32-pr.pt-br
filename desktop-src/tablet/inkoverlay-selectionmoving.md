---
description: Ocorre quando a posição da seleção atual está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: 7cd7a5b1-4ae6-4038-afd0-6ef9d0700938
title: Evento InkOverlay. SelectionMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9afc77198a6a7228e44b3f2bad8015c25a939812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782679"
---
# <a name="inkoverlayselectionmoving-event"></a><span data-ttu-id="106eb-103">Evento InkOverlay. SelectionMoving</span><span class="sxs-lookup"><span data-stu-id="106eb-103">InkOverlay.SelectionMoving event</span></span>

<span data-ttu-id="106eb-104">Ocorre quando a posição da seleção atual está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="106eb-104">Occurs when the position of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="106eb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="106eb-105">Syntax</span></span>


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="106eb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="106eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="106eb-107">*CurSelectionRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="106eb-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="106eb-108">O retângulo para o qual a seleção é movida após o evento **SelectionMoving** .</span><span class="sxs-lookup"><span data-stu-id="106eb-108">The rectangle to which the selection is moved after the **SelectionMoving** event.</span></span>

> [!Note]  
> <span data-ttu-id="106eb-109">Esse retângulo é especificado em coordenadas da janela do cliente, o que permite cenários como manter a taxa de proporção ao redimensionar.</span><span class="sxs-lookup"><span data-stu-id="106eb-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="106eb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="106eb-110">Return value</span></span>

<span data-ttu-id="106eb-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="106eb-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="106eb-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="106eb-112">Remarks</span></span>

<span data-ttu-id="106eb-113">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkOverlayEvents e IInkPictureEvents (dispinterfaces) com uma ID fora do DISPID \_ IOESelectionMoving.</span><span class="sxs-lookup"><span data-stu-id="106eb-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID off DISPID\_IOESelectionMoving.</span></span>

## <a name="requirements"></a><span data-ttu-id="106eb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="106eb-114">Requirements</span></span>



| <span data-ttu-id="106eb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="106eb-115">Requirement</span></span> | <span data-ttu-id="106eb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="106eb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="106eb-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="106eb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="106eb-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="106eb-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="106eb-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="106eb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="106eb-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="106eb-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="106eb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="106eb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="106eb-122"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="106eb-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="106eb-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="106eb-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="106eb-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="106eb-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="106eb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="106eb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="106eb-126">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="106eb-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="106eb-127">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="106eb-127">**InkOverlay Class**</span></span>
</dt> <dt>

[<span data-ttu-id="106eb-128">**Propriedade de seleção**</span><span class="sxs-lookup"><span data-stu-id="106eb-128">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="106eb-129">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="106eb-129">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 





---
description: Ocorre quando o tamanho da seleção atual está prestes a ser alterado, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: 7fe0249c-c43d-498b-9029-cf5969201d96
title: Evento InkOverlay. SelectionResizing (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7debb9461aae39c0549bce863a0513b86c53ffa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171163"
---
# <a name="inkoverlayselectionresizing-event"></a><span data-ttu-id="8ddb3-103">Evento InkOverlay. SelectionResizing</span><span class="sxs-lookup"><span data-stu-id="8ddb3-103">InkOverlay.SelectionResizing event</span></span>

<span data-ttu-id="8ddb3-104">Ocorre quando o tamanho da seleção atual está prestes a ser alterado, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="8ddb3-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ddb3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ddb3-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="8ddb3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ddb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ddb3-107">*CurSelectionRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8ddb3-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ddb3-108">O retângulo delimitador da seleção após o evento **SelectionResizing** .</span><span class="sxs-lookup"><span data-stu-id="8ddb3-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="8ddb3-109">Esse retângulo é especificado em coordenadas da janela do cliente, o que permite cenários como manter a taxa de proporção ao redimensionar.</span><span class="sxs-lookup"><span data-stu-id="8ddb3-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ddb3-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ddb3-110">Return value</span></span>

<span data-ttu-id="8ddb3-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8ddb3-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ddb3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ddb3-112">Remarks</span></span>

<span data-ttu-id="8ddb3-113">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkOverlayEvents e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ IOESelectionResizing.</span><span class="sxs-lookup"><span data-stu-id="8ddb3-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ddb3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ddb3-114">Requirements</span></span>



| <span data-ttu-id="8ddb3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ddb3-115">Requirement</span></span> | <span data-ttu-id="8ddb3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8ddb3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ddb3-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ddb3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8ddb3-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8ddb3-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8ddb3-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ddb3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8ddb3-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8ddb3-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8ddb3-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ddb3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ddb3-122"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8ddb3-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8ddb3-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ddb3-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ddb3-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ddb3-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8ddb3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ddb3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ddb3-126">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="8ddb3-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="8ddb3-127">**Propriedade de seleção**</span><span class="sxs-lookup"><span data-stu-id="8ddb3-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="8ddb3-128">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="8ddb3-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 





---
description: Evento InkPicture. SelectionResizing – ocorre quando o tamanho da seleção atual está prestes a ser alterado, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: Evento InkPicture. SelectionResizing (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8f70b0b502fe426cfd94ce9002e8bbfc5260a88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086414"
---
# <a name="inkpictureselectionresizing-event"></a><span data-ttu-id="2e9d8-103">Evento InkPicture. SelectionResizing</span><span class="sxs-lookup"><span data-stu-id="2e9d8-103">InkPicture.SelectionResizing event</span></span>

<span data-ttu-id="2e9d8-104">Ocorre quando o tamanho da seleção atual está prestes a ser alterado, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="2e9d8-104">Occurs when the size of the current selection is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e9d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e9d8-105">Syntax</span></span>


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="2e9d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e9d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e9d8-107">*CurSelectionRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e9d8-107">*CurSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e9d8-108">O retângulo delimitador da seleção após o evento **SelectionResizing** .</span><span class="sxs-lookup"><span data-stu-id="2e9d8-108">The bounding rectangle of the selection after the **SelectionResizing** event.</span></span>

> [!Note]  
> <span data-ttu-id="2e9d8-109">Esse retângulo é especificado em coordenadas da janela do cliente, o que permite cenários como manter a taxa de proporção ao redimensionar.</span><span class="sxs-lookup"><span data-stu-id="2e9d8-109">This rectangle is specified in client window coordinates, which allows for scenarios such as maintaining the aspect ratio when resizing.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e9d8-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2e9d8-110">Return value</span></span>

<span data-ttu-id="2e9d8-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2e9d8-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e9d8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e9d8-112">Remarks</span></span>

<span data-ttu-id="2e9d8-113">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de DISPID \_ IOESelectionResizing.</span><span class="sxs-lookup"><span data-stu-id="2e9d8-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResizing.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e9d8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e9d8-114">Requirements</span></span>



| <span data-ttu-id="2e9d8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e9d8-115">Requirement</span></span> | <span data-ttu-id="2e9d8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2e9d8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e9d8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e9d8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2e9d8-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2e9d8-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2e9d8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e9d8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2e9d8-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2e9d8-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2e9d8-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e9d8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e9d8-122"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2e9d8-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2e9d8-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e9d8-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e9d8-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e9d8-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2e9d8-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2e9d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e9d8-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="2e9d8-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="2e9d8-127">[**Controle de propriedade de seleção \[ InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="2e9d8-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="2e9d8-128">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="2e9d8-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 

 





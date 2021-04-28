---
description: Evento InkPicture. SelectionResized – ocorre quando o tamanho da seleção atual é alterado, por exemplo, por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: Evento InkPicture. SelectionResized (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dcad4b84cd21ee9b4d385f24033c56913765810
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086464"
---
# <a name="inkpictureselectionresized-event"></a><span data-ttu-id="4b15f-103">Evento InkPicture. SelectionResized</span><span class="sxs-lookup"><span data-stu-id="4b15f-103">InkPicture.SelectionResized event</span></span>

<span data-ttu-id="4b15f-104">Ocorre quando o tamanho da seleção atual é alterado, por exemplo, por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="4b15f-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b15f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b15f-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="4b15f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b15f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b15f-107">*OldSelectionRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4b15f-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b15f-108">O retângulo delimitador da coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selecionada como existia antes de o evento **SelectionResized** ser acionado.</span><span class="sxs-lookup"><span data-stu-id="4b15f-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="4b15f-109">Esse retângulo é especificado em coordenadas de espaço de tinta, o que permite cenários de desfazer.</span><span class="sxs-lookup"><span data-stu-id="4b15f-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b15f-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4b15f-110">Return value</span></span>

<span data-ttu-id="4b15f-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4b15f-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b15f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b15f-112">Remarks</span></span>

<span data-ttu-id="4b15f-113">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de DISPID \_ IOESelectionResized.</span><span class="sxs-lookup"><span data-stu-id="4b15f-113">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b15f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b15f-114">Requirements</span></span>



| <span data-ttu-id="4b15f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b15f-115">Requirement</span></span> | <span data-ttu-id="4b15f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4b15f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b15f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b15f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4b15f-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4b15f-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4b15f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b15f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4b15f-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4b15f-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4b15f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b15f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b15f-122"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4b15f-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4b15f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b15f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b15f-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b15f-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4b15f-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4b15f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b15f-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="4b15f-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="4b15f-127">[**Controle de propriedade de seleção \[ InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="4b15f-127">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> <dt>

[<span data-ttu-id="4b15f-128">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="4b15f-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 


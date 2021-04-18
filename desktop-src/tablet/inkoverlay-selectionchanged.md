---
description: Ocorre quando a seleção de tinta dentro do controle é alterada, como por meio de alterações para a interface do usuário, procedimentos de recortar e colar ou a propriedade Selection.
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: Evento InkOverlay. SelectionChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997e0c8e9620b0a269ff8cd97ff04aa3abfb1df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796182"
---
# <a name="inkoverlayselectionchanged-event"></a><span data-ttu-id="fa5f2-103">Evento InkOverlay. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="fa5f2-103">InkOverlay.SelectionChanged event</span></span>

<span data-ttu-id="fa5f2-104">Ocorre quando a seleção de tinta dentro do controle é alterada, como por meio de alterações para a interface do usuário, procedimentos de recortar e colar ou a propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="fa5f2-104">Occurs when the selection of ink within the control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa5f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa5f2-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="fa5f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa5f2-106">Parameters</span></span>

<span data-ttu-id="fa5f2-107">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fa5f2-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa5f2-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa5f2-108">Return value</span></span>

<span data-ttu-id="fa5f2-109">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fa5f2-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa5f2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa5f2-110">Remarks</span></span>

<span data-ttu-id="fa5f2-111">Não há dados de evento.</span><span class="sxs-lookup"><span data-stu-id="fa5f2-111">There are no event data.</span></span>

<span data-ttu-id="fa5f2-112">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkOverlayEvents e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ IOESelectionChanged.</span><span class="sxs-lookup"><span data-stu-id="fa5f2-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa5f2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa5f2-113">Requirements</span></span>



| <span data-ttu-id="fa5f2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa5f2-114">Requirement</span></span> | <span data-ttu-id="fa5f2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fa5f2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa5f2-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa5f2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fa5f2-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fa5f2-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fa5f2-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa5f2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fa5f2-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fa5f2-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fa5f2-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa5f2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa5f2-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fa5f2-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fa5f2-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa5f2-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa5f2-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa5f2-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fa5f2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa5f2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa5f2-125">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="fa5f2-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="fa5f2-126">**Propriedade de seleção**</span><span class="sxs-lookup"><span data-stu-id="fa5f2-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

 





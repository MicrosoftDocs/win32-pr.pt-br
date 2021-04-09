---
description: Ocorre quando o tamanho da seleção atual é alterado, por exemplo, por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: Evento InkOverlay. SelectionResized (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf9cbb01821756d830b7c0a24adc55dad11b403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171535"
---
# <a name="inkoverlayselectionresized-event"></a><span data-ttu-id="00207-103">Evento InkOverlay. SelectionResized</span><span class="sxs-lookup"><span data-stu-id="00207-103">InkOverlay.SelectionResized event</span></span>

<span data-ttu-id="00207-104">Ocorre quando o tamanho da seleção atual é alterado, por exemplo, por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="00207-104">Occurs when the size of the current selection has changed, for example through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="00207-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00207-105">Syntax</span></span>


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a><span data-ttu-id="00207-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00207-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00207-107">*OldSelectionRect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00207-107">*OldSelectionRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00207-108">O retângulo delimitador da coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) selecionada como existia antes de o evento **SelectionResized** ser acionado.</span><span class="sxs-lookup"><span data-stu-id="00207-108">The bounding rectangle of the selected [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection as it existed before the **SelectionResized** event fired.</span></span>

> [!Note]  
> <span data-ttu-id="00207-109">Esse retângulo é especificado em coordenadas de espaço de tinta, o que permite cenários de desfazer.</span><span class="sxs-lookup"><span data-stu-id="00207-109">This rectangle is specified in ink space coordinates, which allows for undo scenarios.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00207-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00207-110">Return value</span></span>

<span data-ttu-id="00207-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="00207-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00207-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="00207-112">Remarks</span></span>

<span data-ttu-id="00207-113">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkOverlayEvents e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ IOESelectionResized.</span><span class="sxs-lookup"><span data-stu-id="00207-113">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionResized.</span></span>

## <a name="requirements"></a><span data-ttu-id="00207-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00207-114">Requirements</span></span>



| <span data-ttu-id="00207-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="00207-115">Requirement</span></span> | <span data-ttu-id="00207-116">Valor</span><span class="sxs-lookup"><span data-stu-id="00207-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00207-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00207-117">Minimum supported client</span></span><br/> | <span data-ttu-id="00207-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="00207-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="00207-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00207-119">Minimum supported server</span></span><br/> | <span data-ttu-id="00207-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="00207-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="00207-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00207-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="00207-122"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="00207-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="00207-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00207-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="00207-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00207-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="00207-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="00207-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00207-126">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="00207-126">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="00207-127">**Propriedade de seleção**</span><span class="sxs-lookup"><span data-stu-id="00207-127">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[<span data-ttu-id="00207-128">**Classe InkRectangle**</span><span class="sxs-lookup"><span data-stu-id="00207-128">**InkRectangle Class**</span></span>](inkrectangle-class.md)
</dt> </dl>

 


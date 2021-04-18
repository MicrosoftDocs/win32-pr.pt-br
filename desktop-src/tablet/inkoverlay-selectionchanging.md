---
description: Ocorre quando a seleção de tinta dentro do controle está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na Propriedade Selection.
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: Evento InkOverlay. SelectionChanging (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e830a9ea97f6722dd8ab9bdb782e4ae4ac5f44fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781535"
---
# <a name="inkoverlayselectionchanging-event"></a><span data-ttu-id="17626-103">Evento InkOverlay. SelectionChanging</span><span class="sxs-lookup"><span data-stu-id="17626-103">InkOverlay.SelectionChanging event</span></span>

<span data-ttu-id="17626-104">Ocorre quando a seleção de tinta dentro do controle está prestes a ser alterada, como por meio de alterações na interface do usuário, nos procedimentos de recortar e colar ou na propriedade [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="17626-104">Occurs when the selection of ink within the control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="17626-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17626-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="17626-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17626-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17626-107">*NewSelection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17626-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17626-108">A nova coleção de [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que está sendo selecionada.</span><span class="sxs-lookup"><span data-stu-id="17626-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17626-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17626-109">Return value</span></span>

<span data-ttu-id="17626-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="17626-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17626-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="17626-111">Remarks</span></span>

<span data-ttu-id="17626-112">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkOverlayEvents e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ IOESelectionChanging.</span><span class="sxs-lookup"><span data-stu-id="17626-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="17626-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17626-113">Requirements</span></span>



| <span data-ttu-id="17626-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="17626-114">Requirement</span></span> | <span data-ttu-id="17626-115">Valor</span><span class="sxs-lookup"><span data-stu-id="17626-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17626-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17626-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17626-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="17626-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="17626-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17626-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17626-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="17626-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="17626-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17626-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="17626-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="17626-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="17626-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17626-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="17626-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17626-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="17626-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="17626-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17626-125">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="17626-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="17626-126">**Propriedade de seleção**</span><span class="sxs-lookup"><span data-stu-id="17626-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 


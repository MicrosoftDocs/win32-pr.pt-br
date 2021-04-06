---
description: Ocorre antes de os objetos IInkStrokeDisp serem excluídos da Propriedade Ink.
ms.assetid: 747e0fdf-c68b-4805-bdc8-aa05e95ec0f7
title: Evento InkPicture. StrokesDeleting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef70e8526798f306f99c17b511b5c18c502858a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011478"
---
# <a name="inkpicturestrokesdeleting-event"></a><span data-ttu-id="588b1-103">Evento InkPicture. StrokesDeleting</span><span class="sxs-lookup"><span data-stu-id="588b1-103">InkPicture.StrokesDeleting event</span></span>

<span data-ttu-id="588b1-104">Ocorre antes de os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) serem excluídos da propriedade [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="588b1-104">Occurs before [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="588b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="588b1-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="588b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="588b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="588b1-107">*Traços* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="588b1-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="588b1-108">A coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) excluída quando o evento **StrokesDeleting** é acionado.</span><span class="sxs-lookup"><span data-stu-id="588b1-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="588b1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="588b1-109">Return value</span></span>

<span data-ttu-id="588b1-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="588b1-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="588b1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="588b1-111">Remarks</span></span>

<span data-ttu-id="588b1-112">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de DISPID \_ IOEStrokesDeleting.</span><span class="sxs-lookup"><span data-stu-id="588b1-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="588b1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="588b1-113">Requirements</span></span>



| <span data-ttu-id="588b1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="588b1-114">Requirement</span></span> | <span data-ttu-id="588b1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="588b1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="588b1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="588b1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="588b1-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="588b1-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="588b1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="588b1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="588b1-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="588b1-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="588b1-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="588b1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="588b1-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="588b1-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="588b1-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="588b1-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="588b1-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="588b1-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="588b1-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="588b1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="588b1-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="588b1-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 


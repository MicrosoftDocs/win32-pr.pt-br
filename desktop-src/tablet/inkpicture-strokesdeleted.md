---
description: Ocorre após a exclusão dos objetos IInkStrokeDisp da Propriedade Ink.
ms.assetid: 395544e1-dc93-45d3-ac7a-d54712f3c027
title: Evento InkPicture. StrokesDeleted (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf98e51196d760f467d507c133429201883b340e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772592"
---
# <a name="inkpicturestrokesdeleted-event"></a><span data-ttu-id="3ba03-103">Evento InkPicture. StrokesDeleted</span><span class="sxs-lookup"><span data-stu-id="3ba03-103">InkPicture.StrokesDeleted event</span></span>

<span data-ttu-id="3ba03-104">Ocorre após a exclusão dos objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) da propriedade [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="3ba03-104">Occurs after [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ba03-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ba03-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="3ba03-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ba03-106">Parameters</span></span>

<span data-ttu-id="3ba03-107">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3ba03-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ba03-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ba03-108">Return value</span></span>

<span data-ttu-id="3ba03-109">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3ba03-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ba03-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ba03-110">Remarks</span></span>

<span data-ttu-id="3ba03-111">Não há dados de evento.</span><span class="sxs-lookup"><span data-stu-id="3ba03-111">There is no event data.</span></span>

<span data-ttu-id="3ba03-112">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de DISPID \_ IOEStrokesDeleted.</span><span class="sxs-lookup"><span data-stu-id="3ba03-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba03-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ba03-113">Requirements</span></span>



| <span data-ttu-id="3ba03-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ba03-114">Requirement</span></span> | <span data-ttu-id="3ba03-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3ba03-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba03-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ba03-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba03-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3ba03-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3ba03-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ba03-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba03-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3ba03-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3ba03-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ba03-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ba03-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3ba03-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3ba03-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ba03-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ba03-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ba03-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3ba03-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ba03-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba03-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="3ba03-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 





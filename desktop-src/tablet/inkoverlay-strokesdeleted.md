---
description: Ocorre após os traços serem excluídos da Propriedade Ink.
ms.assetid: 60ee8bbd-9230-4b6a-a4b0-4783195e3173
title: Evento InkOverlay. StrokesDeleted (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc37b0de7f86f7d2b68df7074a0f3bb6c9e075e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169900"
---
# <a name="inkoverlaystrokesdeleted-event"></a><span data-ttu-id="fc4d3-103">Evento InkOverlay. StrokesDeleted</span><span class="sxs-lookup"><span data-stu-id="fc4d3-103">InkOverlay.StrokesDeleted event</span></span>

<span data-ttu-id="fc4d3-104">Ocorre após os traços serem excluídos da propriedade [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="fc4d3-104">Occurs after strokes have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc4d3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc4d3-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="fc4d3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc4d3-106">Parameters</span></span>

<span data-ttu-id="fc4d3-107">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fc4d3-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc4d3-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc4d3-108">Return value</span></span>

<span data-ttu-id="fc4d3-109">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fc4d3-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc4d3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc4d3-110">Remarks</span></span>

<span data-ttu-id="fc4d3-111">Não há dados de evento.</span><span class="sxs-lookup"><span data-stu-id="fc4d3-111">There is no event data.</span></span>

<span data-ttu-id="fc4d3-112">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkOverlayEvents e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ IOEStrokesDeleted.</span><span class="sxs-lookup"><span data-stu-id="fc4d3-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc4d3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc4d3-113">Requirements</span></span>



| <span data-ttu-id="fc4d3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc4d3-114">Requirement</span></span> | <span data-ttu-id="fc4d3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fc4d3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc4d3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc4d3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fc4d3-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fc4d3-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fc4d3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc4d3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fc4d3-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fc4d3-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fc4d3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc4d3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc4d3-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fc4d3-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fc4d3-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc4d3-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc4d3-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc4d3-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fc4d3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc4d3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc4d3-125">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="fc4d3-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="fc4d3-126">[**Classe de propriedade de tinta \[ InkCollector/InkOverLay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="fc4d3-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 

 





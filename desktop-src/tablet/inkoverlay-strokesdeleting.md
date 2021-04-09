---
description: Ocorre antes de os traços serem excluídos da Propriedade Ink.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: Evento InkOverlay. StrokesDeleting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64422e61869c633514c3e219e3d090476a693dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922482"
---
# <a name="inkoverlaystrokesdeleting-event"></a><span data-ttu-id="47d24-103">Evento InkOverlay. StrokesDeleting</span><span class="sxs-lookup"><span data-stu-id="47d24-103">InkOverlay.StrokesDeleting event</span></span>

<span data-ttu-id="47d24-104">Ocorre antes de os traços serem excluídos da propriedade [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="47d24-104">Occurs before strokes are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d24-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47d24-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="47d24-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47d24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47d24-107">*Traços* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47d24-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47d24-108">A coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) excluída quando o evento **StrokesDeleting** é acionado.</span><span class="sxs-lookup"><span data-stu-id="47d24-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47d24-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47d24-109">Return value</span></span>

<span data-ttu-id="47d24-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="47d24-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47d24-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="47d24-111">Remarks</span></span>

<span data-ttu-id="47d24-112">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkOverlayEvents e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ IOEStrokesDeleting.</span><span class="sxs-lookup"><span data-stu-id="47d24-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="47d24-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47d24-113">Requirements</span></span>



| <span data-ttu-id="47d24-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="47d24-114">Requirement</span></span> | <span data-ttu-id="47d24-115">Valor</span><span class="sxs-lookup"><span data-stu-id="47d24-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47d24-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47d24-116">Minimum supported client</span></span><br/> | <span data-ttu-id="47d24-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="47d24-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="47d24-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47d24-118">Minimum supported server</span></span><br/> | <span data-ttu-id="47d24-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="47d24-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="47d24-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47d24-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="47d24-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="47d24-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="47d24-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47d24-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="47d24-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47d24-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="47d24-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="47d24-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d24-125">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="47d24-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="47d24-126">[**Classe de propriedade de tinta \[ InkCollector/InkOverLay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="47d24-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 


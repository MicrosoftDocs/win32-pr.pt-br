---
description: Evento InkOverlay. Stroke – ocorre quando o usuário desenha um novo traço em qualquer Tablet.
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: Evento InkOverlay. Stroke (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408c44cf47ecfbf3ea0cfd0f8306be61efb0f8e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116844"
---
# <a name="inkoverlaystroke-event"></a><span data-ttu-id="effe0-103">Evento InkOverlay. Stroke</span><span class="sxs-lookup"><span data-stu-id="effe0-103">InkOverlay.Stroke event</span></span>

<span data-ttu-id="effe0-104">Ocorre quando o usuário desenha um novo traço em qualquer mesa digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="effe0-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="effe0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="effe0-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="effe0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="effe0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="effe0-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="effe0-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="effe0-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento [**Stroke**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="effe0-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**Stroke**](inkcollector-stroke.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="effe0-109">*Traço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="effe0-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="effe0-110">O objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) coletado.</span><span class="sxs-lookup"><span data-stu-id="effe0-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="effe0-111">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="effe0-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="effe0-112">Especifica se o evento deve ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="effe0-112">Specifies whether the event should be canceled.</span></span> <span data-ttu-id="effe0-113">Se **for true**, a coleção do traço será cancelada.</span><span class="sxs-lookup"><span data-stu-id="effe0-113">If **TRUE**, the collection of the stroke is canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="effe0-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="effe0-114">Return value</span></span>

<span data-ttu-id="effe0-115">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="effe0-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="effe0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="effe0-116">Remarks</span></span>

<span data-ttu-id="effe0-117">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICEStroke de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="effe0-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="effe0-118">O evento [**Stroke**](inkcollector-stroke.md) é acionado no modo de seleção ou apagamento, não apenas ao inserir tinta.</span><span class="sxs-lookup"><span data-stu-id="effe0-118">The [**Stroke**](inkcollector-stroke.md) event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="effe0-119">Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento.</span><span class="sxs-lookup"><span data-stu-id="effe0-119">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="effe0-120">A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.</span><span class="sxs-lookup"><span data-stu-id="effe0-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="effe0-121">O evento [**Stroke**](inkcollector-stroke.md) é acionado quando o usuário termina de desenhar um traço, não quando um traço é adicionado à coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="effe0-121">The [**Stroke**](inkcollector-stroke.md) event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="effe0-122">Quando o usuário começa a desenhar um traço pela primeira vez, ele é adicionado imediatamente à coleção InkStrokes; no entanto, o evento **Stroke** não é acionado até que o traço seja concluído.</span><span class="sxs-lookup"><span data-stu-id="effe0-122">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="effe0-123">Portanto, os traços podem existir na coleção InkStrokes que o manipulador de eventos **Stroke** não viu.</span><span class="sxs-lookup"><span data-stu-id="effe0-123">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="effe0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="effe0-124">Requirements</span></span>



| <span data-ttu-id="effe0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="effe0-125">Requirement</span></span> | <span data-ttu-id="effe0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="effe0-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="effe0-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="effe0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="effe0-128">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="effe0-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="effe0-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="effe0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="effe0-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="effe0-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="effe0-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="effe0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="effe0-132"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="effe0-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="effe0-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="effe0-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="effe0-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="effe0-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="effe0-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="effe0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="effe0-136">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="effe0-136">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="effe0-137">[**Coleção de InkStrokes de eventos StrokesAdded \[\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="effe0-137">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="effe0-138">[**Classe InkOverlay do evento StrokesDeleted \[\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="effe0-138">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="effe0-139">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="effe0-139">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="effe0-140">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="effe0-140">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 


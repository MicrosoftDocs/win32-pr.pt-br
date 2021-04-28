---
description: Evento InkPicture. Stroke – ocorre quando o usuário desenha um novo traço em qualquer Tablet.
ms.assetid: 2829b65a-6120-402e-91e3-5587d1f456f9
title: Evento InkPicture. Stroke (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b181c8dc46348c76bd9c2d015d4a97c1f6911ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113694"
---
# <a name="inkpicturestroke-event"></a><span data-ttu-id="fe348-103">Evento InkPicture. Stroke</span><span class="sxs-lookup"><span data-stu-id="fe348-103">InkPicture.Stroke event</span></span>

<span data-ttu-id="fe348-104">Ocorre quando o usuário desenha um novo traço em qualquer mesa digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="fe348-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe348-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe348-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="fe348-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe348-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe348-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe348-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe348-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="fe348-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Stroke** event.</span></span>

</dd> <dt>

<span data-ttu-id="fe348-109">*Traço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe348-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe348-110">O objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) coletado.</span><span class="sxs-lookup"><span data-stu-id="fe348-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="fe348-111">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="fe348-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe348-112">**Variante \_ TRUE** para cancelar a coleção do traço; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="fe348-112">**VARIANT\_TRUE** to cancel the collection of the stroke; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe348-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fe348-113">Return value</span></span>

<span data-ttu-id="fe348-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fe348-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe348-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe348-115">Remarks</span></span>

<span data-ttu-id="fe348-116">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de ICEStroke de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="fe348-116">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="fe348-117">O evento **Stroke** ocorre no modo de seleção ou apagamento, não apenas ao inserir tinta.</span><span class="sxs-lookup"><span data-stu-id="fe348-117">The **Stroke** event occurs when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="fe348-118">Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento.</span><span class="sxs-lookup"><span data-stu-id="fe348-118">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="fe348-119">A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.</span><span class="sxs-lookup"><span data-stu-id="fe348-119">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="fe348-120">O evento **Stroke** ocorre quando o usuário termina de desenhar um traço, não quando um traço é adicionado à coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fe348-120">The **Stroke** event occurs when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="fe348-121">Quando o usuário começa a desenhar um traço pela primeira vez, ele é adicionado imediatamente à coleção InkStrokes; no entanto, o evento **Stroke** não ocorre até que o traço seja concluído.</span><span class="sxs-lookup"><span data-stu-id="fe348-121">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not occur until the stroke is complete.</span></span> <span data-ttu-id="fe348-122">Portanto, os traços podem existir na coleção InkStrokes que o manipulador de eventos **Stroke** não viu.</span><span class="sxs-lookup"><span data-stu-id="fe348-122">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe348-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe348-123">Requirements</span></span>



| <span data-ttu-id="fe348-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe348-124">Requirement</span></span> | <span data-ttu-id="fe348-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fe348-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe348-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe348-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fe348-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fe348-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fe348-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe348-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fe348-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fe348-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fe348-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe348-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe348-131"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fe348-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fe348-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe348-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe348-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe348-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fe348-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fe348-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe348-135">InkPicture</span><span class="sxs-lookup"><span data-stu-id="fe348-135">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="fe348-136">[**Controle InkPicture de evento StrokesAdded \[\]**](inkpicture-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="fe348-136">[**StrokesAdded Event \[InkPicture Control\]**](inkpicture-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="fe348-137">[**Controle InkPicture de evento StrokesDeleted \[\]**](inkpicture-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="fe348-137">[**StrokesDeleted Event \[InkPicture Control\]**](inkpicture-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="fe348-138">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="fe348-138">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="fe348-139">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="fe348-139">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 


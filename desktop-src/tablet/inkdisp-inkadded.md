---
description: Ocorre quando um traço é adicionado ao objeto InkDisp.
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: Evento InkDisp. InkAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d25266a8cd75f873c5a7c1c18fa20fcf5126faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010463"
---
# <a name="inkdispinkadded-event"></a><span data-ttu-id="55aa3-103">Evento InkDisp. InkAdded</span><span class="sxs-lookup"><span data-stu-id="55aa3-103">InkDisp.InkAdded event</span></span>

<span data-ttu-id="55aa3-104">Ocorre quando um traço é adicionado ao objeto [**InkDisp**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="55aa3-104">Occurs when a stroke is added to the [**InkDisp**](inkdisp-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="55aa3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55aa3-105">Syntax</span></span>


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="55aa3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55aa3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55aa3-107">*StrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55aa3-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55aa3-108">A matriz de inteiros de informações de ID de traço para todos os traços que foram adicionados quando esse evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="55aa3-108">The integer array of stroke ID information for all of the strokes that have been added when this event occurs.</span></span>

<span data-ttu-id="55aa3-109">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="55aa3-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55aa3-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55aa3-110">Return value</span></span>

<span data-ttu-id="55aa3-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="55aa3-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55aa3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="55aa3-112">Remarks</span></span>

<span data-ttu-id="55aa3-113">Se você usar o objeto [**InkOverlay**](inkoverlay-class.md) ou o [controle InkPicture](inkpicture-control-reference.md) (em que [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) é igual a [**delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) e [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) é igual a [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) e passar a borracha sobre um traço, você obterá a seguinte sequência de eventos:</span><span class="sxs-lookup"><span data-stu-id="55aa3-113">If you use the [**InkOverlay**](inkoverlay-class.md) object or the [InkPicture](inkpicture-control-reference.md) control (where [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) equals [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) and [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) equals [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) and pass the eraser over a stroke, you get the following sequence of events:</span></span>

-   [<span data-ttu-id="55aa3-114">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="55aa3-114">**InkDeleted**</span></span>](inkdisp-inkdeleted.md)
-   <span data-ttu-id="55aa3-115">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="55aa3-115">**InkAdded**</span></span>
-   [<span data-ttu-id="55aa3-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="55aa3-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md)

<span data-ttu-id="55aa3-117">Os eventos **InkAdded** e [**InkDeleted**](inkdisp-inkdeleted.md) adicionais ocorrem porque o código subjacente adiciona um traço interno e invisível para rastrear a borracha.</span><span class="sxs-lookup"><span data-stu-id="55aa3-117">The additional **InkAdded** and [**InkDeleted**](inkdisp-inkdeleted.md) events occur because the underlying code adds an internal, invisible stroke to track the eraser.</span></span>

<span data-ttu-id="55aa3-118">Esse método de evento é definido na \_ interface IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="55aa3-118">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="55aa3-119">A \_ interface IInkEvents implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IEInkAdded DISPID.</span><span class="sxs-lookup"><span data-stu-id="55aa3-119">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IEInkAdded.</span></span>

<span data-ttu-id="55aa3-120">O evento **InkAdded** é acionado mesmo quando no modo de seleção ou apagamento, não apenas ao inserir tinta.</span><span class="sxs-lookup"><span data-stu-id="55aa3-120">The **InkAdded** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="55aa3-121">Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento.</span><span class="sxs-lookup"><span data-stu-id="55aa3-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="55aa3-122">A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.</span><span class="sxs-lookup"><span data-stu-id="55aa3-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="55aa3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55aa3-123">Requirements</span></span>



| <span data-ttu-id="55aa3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="55aa3-124">Requirement</span></span> | <span data-ttu-id="55aa3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="55aa3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55aa3-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55aa3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="55aa3-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="55aa3-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="55aa3-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55aa3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="55aa3-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="55aa3-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="55aa3-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55aa3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="55aa3-131"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="55aa3-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="55aa3-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55aa3-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="55aa3-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55aa3-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="55aa3-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="55aa3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55aa3-135">**Classe InkDisp**</span><span class="sxs-lookup"><span data-stu-id="55aa3-135">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

<span data-ttu-id="55aa3-136">[**Classe InkOverlay da propriedade EditingMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span><span class="sxs-lookup"><span data-stu-id="55aa3-136">[**EditingMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span></span>
</dt> <dt>

<span data-ttu-id="55aa3-137">[**Classe InkOverlay da Propriedade EraserMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span><span class="sxs-lookup"><span data-stu-id="55aa3-137">[**EraserMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span></span>
</dt> <dt>

[<span data-ttu-id="55aa3-138">**Evento InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="55aa3-138">**InkDeleted Event**</span></span>](inkdisp-inkdeleted.md)
</dt> <dt>

[<span data-ttu-id="55aa3-139">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="55aa3-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="55aa3-140">Referência de controle InkPicture</span><span class="sxs-lookup"><span data-stu-id="55aa3-140">InkPicture Control Reference</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="55aa3-141">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="55aa3-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 


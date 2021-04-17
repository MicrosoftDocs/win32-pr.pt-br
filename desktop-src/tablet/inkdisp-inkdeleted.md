---
description: Ocorre quando um traço é excluído do objeto InkDisp.
ms.assetid: 59ada470-6620-411d-889e-882f41ccea3e
title: Evento InkDisp. InkDeleted (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9022b34b128f92530761a0093b2e7c1823dd88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780209"
---
# <a name="inkdispinkdeleted-event"></a><span data-ttu-id="93f4e-103">Evento InkDisp. InkDeleted</span><span class="sxs-lookup"><span data-stu-id="93f4e-103">InkDisp.InkDeleted event</span></span>

<span data-ttu-id="93f4e-104">Ocorre quando um traço é excluído do objeto [**InkDisp**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="93f4e-104">Occurs when a stroke is deleted from the [**InkDisp**](inkdisp-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="93f4e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93f4e-105">Syntax</span></span>


```C++
void InkDeleted(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="93f4e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93f4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93f4e-107">*StrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93f4e-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93f4e-108">Especifica a matriz de inteiros de informações de ID de traço para todos os traços que foram excluídos quando esse evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="93f4e-108">Specifies the integer array of stroke ID information for all of the strokes that have been deleted when this event occurs.</span></span>

<span data-ttu-id="93f4e-109">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="93f4e-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93f4e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93f4e-110">Return value</span></span>

<span data-ttu-id="93f4e-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="93f4e-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93f4e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="93f4e-112">Remarks</span></span>

<span data-ttu-id="93f4e-113">Se você usar o objeto [**InkOverlay**](inkoverlay-class.md) ou o [controle InkPicture](inkpicture-control-reference.md) (em que [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) é igual a [**delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) e [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) é igual a [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) e passar a borracha sobre um traço, você obterá a seguinte sequência de eventos:</span><span class="sxs-lookup"><span data-stu-id="93f4e-113">If you use the [**InkOverlay**](inkoverlay-class.md) object or the [InkPicture](inkpicture-control-reference.md) control (where [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) equals [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) and [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) equals [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) and pass the eraser over a stroke, you get the following sequence of events:</span></span>

-   <span data-ttu-id="93f4e-114">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="93f4e-114">**InkDeleted**</span></span>
-   [<span data-ttu-id="93f4e-115">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="93f4e-115">**InkAdded**</span></span>](inkdisp-inkadded.md)
-   <span data-ttu-id="93f4e-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="93f4e-116">**InkDeleted**</span></span>

<span data-ttu-id="93f4e-117">Os eventos [**InkAdded**](inkdisp-inkadded.md) e **InkDeleted** adicionais ocorrem porque o código subjacente adiciona um traço interno e invisível para rastrear a borracha.</span><span class="sxs-lookup"><span data-stu-id="93f4e-117">The additional [**InkAdded**](inkdisp-inkadded.md) and **InkDeleted** events occur because the underlying code adds an internal, invisible stroke to track the eraser.</span></span>

<span data-ttu-id="93f4e-118">Esse método de evento é definido na \_ interface IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="93f4e-118">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="93f4e-119">A \_ interface IInkEvents implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IEInkDeleted DISPID.</span><span class="sxs-lookup"><span data-stu-id="93f4e-119">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IEInkDeleted.</span></span>

<span data-ttu-id="93f4e-120">O evento **InkDeleted** é acionado mesmo quando no modo de seleção ou apagamento, não apenas ao inserir tinta.</span><span class="sxs-lookup"><span data-stu-id="93f4e-120">The **InkDeleted** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="93f4e-121">Isso requer que você monitore o modo de edição (que é responsável pela configuração) e esteja ciente do modo antes de interpretar o evento.</span><span class="sxs-lookup"><span data-stu-id="93f4e-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="93f4e-122">A vantagem desse requisito é maior liberdade para inovar na plataforma por meio de maior conscientização dos eventos da plataforma.</span><span class="sxs-lookup"><span data-stu-id="93f4e-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="93f4e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93f4e-123">Requirements</span></span>



| <span data-ttu-id="93f4e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="93f4e-124">Requirement</span></span> | <span data-ttu-id="93f4e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="93f4e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93f4e-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93f4e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="93f4e-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="93f4e-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="93f4e-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93f4e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="93f4e-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="93f4e-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="93f4e-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93f4e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="93f4e-131"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="93f4e-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="93f4e-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93f4e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="93f4e-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93f4e-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="93f4e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="93f4e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f4e-135">**Classe InkDisp**</span><span class="sxs-lookup"><span data-stu-id="93f4e-135">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

<span data-ttu-id="93f4e-136">[**Classe InkOverlay da propriedade EditingMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span><span class="sxs-lookup"><span data-stu-id="93f4e-136">[**EditingMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span></span>
</dt> <dt>

<span data-ttu-id="93f4e-137">[**Classe InkOverlay da Propriedade EraserMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span><span class="sxs-lookup"><span data-stu-id="93f4e-137">[**EraserMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span></span>
</dt> <dt>

[<span data-ttu-id="93f4e-138">**Evento InkAdded**</span><span class="sxs-lookup"><span data-stu-id="93f4e-138">**InkAdded Event**</span></span>](inkdisp-inkadded.md)
</dt> <dt>

[<span data-ttu-id="93f4e-139">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="93f4e-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="93f4e-140">Referência de controle InkPicture</span><span class="sxs-lookup"><span data-stu-id="93f4e-140">InkPicture Control Reference</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="93f4e-141">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="93f4e-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 


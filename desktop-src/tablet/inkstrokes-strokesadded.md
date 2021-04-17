---
description: Ocorre quando um ou mais traços são adicionados à coleção InkStrokes.
ms.assetid: d32dcaef-3beb-4ee1-84d6-5944278936f6
title: Evento InkStrokes. StrokesAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a53bf1f511b5809cfb9a6ca0a2f683f0e85540af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811730"
---
# <a name="inkstrokesstrokesadded-event"></a><span data-ttu-id="c18fa-103">Evento InkStrokes. StrokesAdded</span><span class="sxs-lookup"><span data-stu-id="c18fa-103">InkStrokes.StrokesAdded event</span></span>

<span data-ttu-id="c18fa-104">Ocorre quando um ou mais traços são adicionados à coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c18fa-104">Occurs when one or more strokes are added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c18fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c18fa-105">Syntax</span></span>


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="c18fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c18fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c18fa-107">*StrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c18fa-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c18fa-108">A matriz de inteiros de identificadores para cada objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) adicionado quando esse evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="c18fa-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object added when this event occurs.</span></span>

<span data-ttu-id="c18fa-109">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="c18fa-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c18fa-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c18fa-110">Return value</span></span>

<span data-ttu-id="c18fa-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c18fa-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c18fa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c18fa-112">Remarks</span></span>

<span data-ttu-id="c18fa-113">Esse método de evento é definido na \_ interface IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="c18fa-113">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="c18fa-114">A \_ interface IInkEvents implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ SEStrokesAdded DISPID.</span><span class="sxs-lookup"><span data-stu-id="c18fa-114">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="c18fa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c18fa-115">Requirements</span></span>



| <span data-ttu-id="c18fa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c18fa-116">Requirement</span></span> | <span data-ttu-id="c18fa-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c18fa-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c18fa-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c18fa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c18fa-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c18fa-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c18fa-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c18fa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c18fa-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c18fa-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c18fa-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c18fa-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c18fa-123"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c18fa-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c18fa-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c18fa-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="c18fa-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c18fa-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c18fa-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c18fa-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="c18fa-127">[Coleção InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c18fa-127">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c18fa-128">[**Adicionar coleção de métodos \[ InkStrokes\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add)</span><span class="sxs-lookup"><span data-stu-id="c18fa-128">[**Add Method \[InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add)</span></span>
</dt> <dt>

[<span data-ttu-id="c18fa-129">**Classe InkDisp**</span><span class="sxs-lookup"><span data-stu-id="c18fa-129">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> </dl>

 


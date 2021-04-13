---
description: Ocorre quando um ou mais traços são excluídos da coleção InkStrokes.
ms.assetid: 58d78143-c733-45dc-ae5f-fe13136010db
title: Evento InkStrokes. StrokesRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86448f9676e07a11effe683ecd883874791ff3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297627"
---
# <a name="inkstrokesstrokesremoved-event"></a><span data-ttu-id="3333a-103">Evento InkStrokes. StrokesRemoved</span><span class="sxs-lookup"><span data-stu-id="3333a-103">InkStrokes.StrokesRemoved event</span></span>

<span data-ttu-id="3333a-104">Ocorre quando um ou mais traços são excluídos da coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3333a-104">Occurs when one or more strokes are deleted from the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3333a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3333a-105">Syntax</span></span>


```C++
void StrokesRemoved(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="3333a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3333a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3333a-107">*StrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3333a-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3333a-108">A matriz de inteiros de identificadores para cada objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) excluído quando esse evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="3333a-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object deleted when this event occurs.</span></span>

<span data-ttu-id="3333a-109">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="3333a-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3333a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3333a-110">Return value</span></span>

<span data-ttu-id="3333a-111">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3333a-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3333a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3333a-112">Remarks</span></span>

<span data-ttu-id="3333a-113">Esse método de evento é definido na \_ interface IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="3333a-113">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="3333a-114">A \_ interface IInkEvents implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ SEStrokesRemoved DISPID.</span><span class="sxs-lookup"><span data-stu-id="3333a-114">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="3333a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3333a-115">Requirements</span></span>



| <span data-ttu-id="3333a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3333a-116">Requirement</span></span> | <span data-ttu-id="3333a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3333a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3333a-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3333a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3333a-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3333a-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3333a-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3333a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3333a-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3333a-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3333a-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3333a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3333a-123"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3333a-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3333a-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3333a-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="3333a-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3333a-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3333a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3333a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="3333a-127">[Coleção InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3333a-127">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3333a-128">[**Remover \[ coleção InkStrokes do método\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)</span><span class="sxs-lookup"><span data-stu-id="3333a-128">[**Remove Method \[InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)</span></span>
</dt> <dt>

[<span data-ttu-id="3333a-129">**Classe InkDisp**</span><span class="sxs-lookup"><span data-stu-id="3333a-129">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> </dl>

 


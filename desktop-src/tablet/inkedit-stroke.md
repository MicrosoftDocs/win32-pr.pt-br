---
description: Ocorre quando o usuário desenha um novo objeto IInkStrokeDisp em qualquer objeto IInkTablet.
ms.assetid: fac5104d-d0da-40b1-a4a6-00a34718d09f
title: Evento InkEdit. Stroke (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d21abde9deb565f207a44ddd44b51681f1bfa6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663168"
---
# <a name="inkeditstroke-event"></a><span data-ttu-id="6fbf9-103">Evento InkEdit. Stroke</span><span class="sxs-lookup"><span data-stu-id="6fbf9-103">InkEdit.Stroke event</span></span>

<span data-ttu-id="6fbf9-104">Ocorre quando o usuário desenha um novo objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) em qualquer objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .</span><span class="sxs-lookup"><span data-stu-id="6fbf9-104">Occurs when the user draws a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object on any [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fbf9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fbf9-105">Syntax</span></span>


```C++
HRESULT Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="6fbf9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fbf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fbf9-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fbf9-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fbf9-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="6fbf9-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="6fbf9-109">*Traço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fbf9-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fbf9-110">O objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) coletado.</span><span class="sxs-lookup"><span data-stu-id="6fbf9-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="6fbf9-111">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6fbf9-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fbf9-112">**Variante \_ TRUE** para cancelar a coleção do objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ; **Variante \_ FALSE** para coletar o objeto **IInkStrokeDisp** e continuar com o **traço** mesmo.</span><span class="sxs-lookup"><span data-stu-id="6fbf9-112">**VARIANT\_TRUE** to cancel the collection of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object; **VARIANT\_FALSE** to collect the **IInkStrokeDisp** object and continue with the **Stroke** even.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fbf9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fbf9-113">Return value</span></span>

<span data-ttu-id="6fbf9-114">Se esse evento for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6fbf9-114">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fbf9-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6fbf9-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fbf9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fbf9-116">Remarks</span></span>

<span data-ttu-id="6fbf9-117">Esse método de evento é definido na interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="6fbf9-117">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="6fbf9-118">A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IeeStroke DISPID.</span><span class="sxs-lookup"><span data-stu-id="6fbf9-118">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeStroke.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fbf9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fbf9-119">Requirements</span></span>



| <span data-ttu-id="6fbf9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fbf9-120">Requirement</span></span> | <span data-ttu-id="6fbf9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6fbf9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fbf9-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fbf9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6fbf9-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6fbf9-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6fbf9-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fbf9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6fbf9-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6fbf9-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6fbf9-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fbf9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fbf9-127"><dt>Inked. h (também requer Inked \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6fbf9-127"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6fbf9-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6fbf9-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="6fbf9-129"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fbf9-129"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6fbf9-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fbf9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fbf9-131">InkEdit</span><span class="sxs-lookup"><span data-stu-id="6fbf9-131">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="6fbf9-132">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="6fbf9-132">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="6fbf9-133">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="6fbf9-133">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 


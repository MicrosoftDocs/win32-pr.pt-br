---
description: Preterido. O PenInputPanel foi substituído pelo painel de entrada de texto (TIP). Ocorre quando o objeto PenInputPanel é exibido ou oculto.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: Evento PenInputPanel. VisibleChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c739f3517ad9739f1d1ba95af9e5001dfbe659a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781427"
---
# <a name="peninputpanelvisiblechanged-event"></a><span data-ttu-id="7897d-104">Evento PenInputPanel. VisibleChanged</span><span class="sxs-lookup"><span data-stu-id="7897d-104">PenInputPanel.VisibleChanged event</span></span>

<span data-ttu-id="7897d-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="7897d-105">Deprecated.</span></span> <span data-ttu-id="7897d-106">O [**PenInputPanel**](peninputpanel-class.md) foi substituído pelo painel de [entrada de texto (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7897d-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="7897d-107">Ocorre quando o objeto [**PenInputPanel**](peninputpanel-class.md) é exibido ou oculto.</span><span class="sxs-lookup"><span data-stu-id="7897d-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object has shown or hidden itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="7897d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7897d-108">Syntax</span></span>


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a><span data-ttu-id="7897d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7897d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7897d-110">*NewVisibility* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7897d-110">*NewVisibility* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7897d-111">**Variante \_ TRUE** para fazer com que o objeto [**PenInputPanel**](peninputpanel-class.md) se torne visível; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="7897d-111">**VARIANT\_TRUE** to cause the [**PenInputPanel**](peninputpanel-class.md) object to become visible; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7897d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7897d-112">Return value</span></span>

<span data-ttu-id="7897d-113">Se esse evento for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7897d-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7897d-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7897d-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7897d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7897d-115">Remarks</span></span>

<span data-ttu-id="7897d-116">O evento **VisibleChanged** se aplica ao destino de foco do painel de entrada do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="7897d-116">The **VisibleChanged** event applies to the Tablet PC Input Panel hover target.</span></span> <span data-ttu-id="7897d-117">No entanto, ele não é gerado quando o destino de foco se expande para mostrar o painel de entrada completo do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="7897d-117">However, it is not raised when the hover target expands to show the full Tablet PC Input Panel.</span></span>

## <a name="requirements"></a><span data-ttu-id="7897d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7897d-118">Requirements</span></span>



| <span data-ttu-id="7897d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7897d-119">Requirement</span></span> | <span data-ttu-id="7897d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7897d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7897d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7897d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7897d-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7897d-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7897d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7897d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7897d-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7897d-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7897d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7897d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7897d-126"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7897d-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7897d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7897d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="7897d-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7897d-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7897d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7897d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7897d-130">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="7897d-130">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 





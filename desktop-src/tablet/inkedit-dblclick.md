---
description: Ocorre quando o controle InkEdit é clicado duas vezes.
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: Evento InkEdit. DblClick (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fee0ec42171c9abbe0c99691f881b99db512869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105794450"
---
# <a name="inkeditdblclick-event"></a><span data-ttu-id="cac84-103">Evento InkEdit. DblClick</span><span class="sxs-lookup"><span data-stu-id="cac84-103">InkEdit.DblClick event</span></span>

<span data-ttu-id="cac84-104">Ocorre quando o controle [InkEdit](inkedit-control-reference.md) é clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="cac84-104">Occurs when the [InkEdit](inkedit-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac84-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cac84-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="cac84-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cac84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac84-107">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="cac84-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cac84-108">**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="cac84-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac84-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cac84-109">Return value</span></span>

<span data-ttu-id="cac84-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cac84-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cac84-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cac84-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cac84-112">Para distinguir entre os botões esquerdo, direito e do meio do mouse, use os eventos [**MouseDown**](inkedit-mousedown.md) e [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="cac84-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span> <span data-ttu-id="cac84-113">Se houver código no evento de [**clique**](inkedit-click.md) , o evento **DblClick** nunca será disparado.</span><span class="sxs-lookup"><span data-stu-id="cac84-113">If there is code in the [**Click**](inkedit-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="cac84-114">Esse método de evento é definido na interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="cac84-114">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="cac84-115">A interface **\_ IInkEditEvents** implementa a interface IDispatch com um identificador de **\_ IeeDblClick DISPID**.</span><span class="sxs-lookup"><span data-stu-id="cac84-115">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac84-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cac84-116">Requirements</span></span>



| <span data-ttu-id="cac84-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cac84-117">Requirement</span></span> | <span data-ttu-id="cac84-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cac84-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac84-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cac84-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cac84-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cac84-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cac84-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cac84-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cac84-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cac84-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cac84-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cac84-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cac84-124"><dt>Inked. h (também requer Inked \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cac84-124"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cac84-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cac84-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="cac84-126"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cac84-126"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cac84-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="cac84-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac84-128">InkEdit</span><span class="sxs-lookup"><span data-stu-id="cac84-128">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 





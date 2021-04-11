---
description: Ocorre quando o controle InkPicture é clicado duas vezes.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: Evento InkPicture. DblClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c3d9bb9125c8142186da969acf6ce03f5f76b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297226"
---
# <a name="inkpicturedblclick-event"></a><span data-ttu-id="f4e47-103">Evento InkPicture. DblClick</span><span class="sxs-lookup"><span data-stu-id="f4e47-103">InkPicture.DblClick event</span></span>

<span data-ttu-id="f4e47-104">Ocorre quando o controle [InkPicture](inkpicture-control-reference.md) é clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="f4e47-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4e47-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4e47-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="f4e47-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4e47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4e47-107">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f4e47-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4e47-108">Se o evento deve ser cancelado para o controle pai.</span><span class="sxs-lookup"><span data-stu-id="f4e47-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4e47-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4e47-109">Return value</span></span>

<span data-ttu-id="f4e47-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f4e47-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4e47-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4e47-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f4e47-112">Para distinguir entre os botões esquerdo, direito e do meio do mouse, use os eventos [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="f4e47-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="f4e47-113">Se houver código no evento de [**clique**](inkpicture-click.md) , o evento **DblClick** nunca será disparado.</span><span class="sxs-lookup"><span data-stu-id="f4e47-113">If there is code in the [**Click**](inkpicture-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="f4e47-114">Esse método de evento é definido na interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="f4e47-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="f4e47-115">A interface **\_ IInkPictureEvents** implementa a interface IDispatch com um identificador de **\_ IPEDblClick DISPID**.</span><span class="sxs-lookup"><span data-stu-id="f4e47-115">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4e47-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4e47-116">Requirements</span></span>



| <span data-ttu-id="f4e47-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4e47-117">Requirement</span></span> | <span data-ttu-id="f4e47-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f4e47-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e47-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4e47-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f4e47-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f4e47-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f4e47-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4e47-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f4e47-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f4e47-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f4e47-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4e47-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4e47-124"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e47-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f4e47-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4e47-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4e47-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4e47-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f4e47-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4e47-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e47-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="f4e47-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 





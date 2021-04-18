---
description: Ocorre quando o conteúdo do controle InkEdit é alterado.
ms.assetid: 6c65fcca-c84a-414c-a4e5-c5fdffb13e51
title: Evento InkEdit. Change (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ad11ef335a397070001f1ae6be785d60fe9cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796137"
---
# <a name="inkeditchange-event"></a><span data-ttu-id="4c97e-103">Evento InkEdit. Change</span><span class="sxs-lookup"><span data-stu-id="4c97e-103">InkEdit.Change event</span></span>

<span data-ttu-id="4c97e-104">Ocorre quando o conteúdo do controle [InkEdit](inkedit-control-reference.md) é alterado.</span><span class="sxs-lookup"><span data-stu-id="4c97e-104">Occurs when the content of the [InkEdit](inkedit-control-reference.md) control changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c97e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c97e-105">Syntax</span></span>


```C++
void Change();
```



## <a name="parameters"></a><span data-ttu-id="4c97e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c97e-106">Parameters</span></span>

<span data-ttu-id="4c97e-107">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4c97e-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c97e-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c97e-108">Return value</span></span>

<span data-ttu-id="4c97e-109">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4c97e-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c97e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c97e-110">Remarks</span></span>

<span data-ttu-id="4c97e-111">Esse evento ocorre sempre que qualquer propriedade que afete o conteúdo da alteração do controle [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="4c97e-111">This event occurs whenever any properties that affect the contents of the [InkEdit](inkedit-control-reference.md) control change.</span></span>

<span data-ttu-id="4c97e-112">Esse método de evento é definido na interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="4c97e-112">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="4c97e-113">A interface **\_ IInkEditEvents** implementa a interface IDispatch com um identificador de **\_ IeeChange DISPID**.</span><span class="sxs-lookup"><span data-stu-id="4c97e-113">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeChange**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c97e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c97e-114">Requirements</span></span>



| <span data-ttu-id="4c97e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c97e-115">Requirement</span></span> | <span data-ttu-id="4c97e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4c97e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c97e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c97e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4c97e-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4c97e-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4c97e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c97e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4c97e-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4c97e-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4c97e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c97e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c97e-122"><dt>Inked. h (também requer Inked \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4c97e-122"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4c97e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c97e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c97e-124"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c97e-124"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4c97e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c97e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c97e-126">InkEdit</span><span class="sxs-lookup"><span data-stu-id="4c97e-126">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 





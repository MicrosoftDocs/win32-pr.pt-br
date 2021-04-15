---
description: Preterido. O PenInputPanel foi substituído pelo painel de entrada de texto (TIP). Ocorre quando o objeto PenInputPanel está sendo movido.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: Evento PenInputPanel. PanelMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be69e227188739cb656e6a1eb471716e1aa4feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761048"
---
# <a name="peninputpanelpanelmoving-event"></a><span data-ttu-id="f0ee7-104">Evento PenInputPanel. PanelMoving</span><span class="sxs-lookup"><span data-stu-id="f0ee7-104">PenInputPanel.PanelMoving event</span></span>

<span data-ttu-id="f0ee7-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="f0ee7-105">Deprecated.</span></span> <span data-ttu-id="f0ee7-106">O [**PenInputPanel**](peninputpanel-class.md) foi substituído pelo painel de [entrada de texto (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f0ee7-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="f0ee7-107">Ocorre quando o objeto [**PenInputPanel**](peninputpanel-class.md) está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="f0ee7-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object is moving.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ee7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0ee7-108">Syntax</span></span>


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a><span data-ttu-id="f0ee7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0ee7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0ee7-110">*À esquerda* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f0ee7-110">*Left* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ee7-111">A nova posição horizontal, ou eixo x, da borda esquerda do objeto [**PenInputPanel**](peninputpanel-class.md) , em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="f0ee7-111">The new horizontal, or x-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="f0ee7-112">*Superior* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f0ee7-112">*Top* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ee7-113">A nova posição vertical, ou eixo y, da borda esquerda do objeto [**PenInputPanel**](peninputpanel-class.md) , em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="f0ee7-113">The new vertical, or y-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0ee7-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0ee7-114">Return value</span></span>

<span data-ttu-id="f0ee7-115">Se esse evento for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f0ee7-115">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f0ee7-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f0ee7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0ee7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0ee7-117">Remarks</span></span>

<span data-ttu-id="f0ee7-118">O evento **PanelMoving** foi projetado para ser usado para alterar a posição do painel de entrada da caneta, alterando os parâmetros *esquerdo* e *superior* .</span><span class="sxs-lookup"><span data-stu-id="f0ee7-118">The **PanelMoving** event is designed to be used to change the position of the pen input panel by changing the *Left* and *Top* parameters.</span></span>

<span data-ttu-id="f0ee7-119">Os métodos [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) e [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) fazem com que o objeto [**PenInputPanel**](peninputpanel-class.md) chame seu código de posicionamento automático, que dispara um evento **PanelMoving** .</span><span class="sxs-lookup"><span data-stu-id="f0ee7-119">The [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) and [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) methods cause the [**PenInputPanel**](peninputpanel-class.md) object to call its auto-positioning code which triggers a **PanelMoving** event.</span></span> <span data-ttu-id="f0ee7-120">Consequentemente, chamar esses métodos dentro de um manipulador **PanelMoving** pode resultar em um loop infinito recursivo.</span><span class="sxs-lookup"><span data-stu-id="f0ee7-120">Consequently, calling these methods inside a **PanelMoving** handler can result in a recursive endless loop.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ee7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0ee7-121">Requirements</span></span>



| <span data-ttu-id="f0ee7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0ee7-122">Requirement</span></span> | <span data-ttu-id="f0ee7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f0ee7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ee7-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0ee7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ee7-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f0ee7-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f0ee7-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0ee7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ee7-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f0ee7-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f0ee7-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0ee7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0ee7-129"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f0ee7-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f0ee7-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0ee7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0ee7-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0ee7-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f0ee7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0ee7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ee7-133">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="f0ee7-133">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 





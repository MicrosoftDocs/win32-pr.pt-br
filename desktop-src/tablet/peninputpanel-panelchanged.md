---
description: Preterido. O PenInputPanel foi substituído pelo painel de entrada de texto (TIP). Ocorre quando o objeto PenInputPanel é alterado entre layouts.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Evento PenInputPanel. Panelchanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297223"
---
# <a name="peninputpanelpanelchanged-event"></a><span data-ttu-id="3dd57-104">Evento PenInputPanel. Panelchanged</span><span class="sxs-lookup"><span data-stu-id="3dd57-104">PenInputPanel.PanelChanged event</span></span>

<span data-ttu-id="3dd57-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="3dd57-105">Deprecated.</span></span> <span data-ttu-id="3dd57-106">O [**PenInputPanel**](peninputpanel-class.md) foi substituído pelo painel de [entrada de texto (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="3dd57-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="3dd57-107">Ocorre quando o objeto [**PenInputPanel**](peninputpanel-class.md) é alterado entre layouts.</span><span class="sxs-lookup"><span data-stu-id="3dd57-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object changes between layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd57-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3dd57-108">Syntax</span></span>


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a><span data-ttu-id="3dd57-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3dd57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dd57-110">*NewPanelType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3dd57-110">*NewPanelType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd57-111">O novo tipo de painel usado para entrada dentro do objeto [**PenInputPanel**](peninputpanel-class.md) , após o evento **panelchanged** ser acionado.</span><span class="sxs-lookup"><span data-stu-id="3dd57-111">The new panel type used for input within the [**PenInputPanel**](peninputpanel-class.md) object, after the **PanelChanged** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dd57-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3dd57-112">Return value</span></span>

<span data-ttu-id="3dd57-113">Se esse evento for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3dd57-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3dd57-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3dd57-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd57-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dd57-115">Remarks</span></span>

<span data-ttu-id="3dd57-116">Ao criar um objeto [**PenInputPanel**](peninputpanel-class.md) , o [**manuscrito**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) é o **PanelType** padrão.</span><span class="sxs-lookup"><span data-stu-id="3dd57-116">When creating a [**PenInputPanel**](peninputpanel-class.md) object, [**Handwriting**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) is the default **PanelType**.</span></span> <span data-ttu-id="3dd57-117">Se você alterar o painel definindo a propriedade [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) antes que o painel de entrada da caneta se torne ativo pela primeira vez, ocorrerá um evento **panelchanged** .</span><span class="sxs-lookup"><span data-stu-id="3dd57-117">If you change the panel by setting the [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) property before the pen input panel becomes active for the first time, a **PanelChanged** event occurs.</span></span>

<span data-ttu-id="3dd57-118">O evento **panelchanged** não é gerado quando o usuário muda entre os pads de escrita alinhado e na caixa.</span><span class="sxs-lookup"><span data-stu-id="3dd57-118">The **PanelChanged** event is not raised when the user changes between Lined and Boxed writing pads.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd57-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dd57-119">Requirements</span></span>



| <span data-ttu-id="3dd57-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dd57-120">Requirement</span></span> | <span data-ttu-id="3dd57-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3dd57-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd57-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dd57-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd57-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3dd57-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3dd57-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dd57-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd57-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3dd57-125">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3dd57-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3dd57-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dd57-127"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3dd57-127"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3dd57-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3dd57-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="3dd57-129"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dd57-129"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3dd57-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dd57-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd57-131">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="3dd57-131">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 

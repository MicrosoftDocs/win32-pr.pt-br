---
description: Preterido. O PenInputPanel foi substituído pelo painel de entrada de texto (TIP). Ocorre quando o foco de entrada é alterado antes que o objeto PenInputPanel pudesse inserir a entrada do usuário no controle anexado.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Evento PenInputPanel. InputFailed (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 198c2b466dc03357d9851d7c8a6b7f44c6bf6884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763258"
---
# <a name="peninputpanelinputfailed-event"></a><span data-ttu-id="dde2b-104">Evento PenInputPanel. InputFailed</span><span class="sxs-lookup"><span data-stu-id="dde2b-104">PenInputPanel.InputFailed event</span></span>

<span data-ttu-id="dde2b-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="dde2b-105">Deprecated.</span></span> <span data-ttu-id="dde2b-106">O [**PenInputPanel**](peninputpanel-class.md) foi substituído pelo painel de [entrada de texto (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="dde2b-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="dde2b-107">Ocorre quando o foco de entrada é alterado antes que o objeto [**PenInputPanel**](peninputpanel-class.md) pudesse inserir a entrada do usuário no controle anexado.</span><span class="sxs-lookup"><span data-stu-id="dde2b-107">Occurs when input focus changes before the [**PenInputPanel**](peninputpanel-class.md) object was able to insert user input into the attached control.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde2b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dde2b-108">Syntax</span></span>


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="dde2b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dde2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dde2b-110">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dde2b-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde2b-111">O identificador de janela do controle que invocou o objeto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="dde2b-111">The window handle of the control that invoked the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="dde2b-112">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dde2b-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde2b-113">A chave virtual correspondente à chave foi pressionada.</span><span class="sxs-lookup"><span data-stu-id="dde2b-113">The virtual key corresponding to the key pressed.</span></span>

</dd> <dt>

<span data-ttu-id="dde2b-114">*Texto* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="dde2b-114">*Text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde2b-115">A cadeia de caracteres que deve ser inserida no controle representado pelo parâmetro *HWND* quando o evento **InputFailed** foi gerado.</span><span class="sxs-lookup"><span data-stu-id="dde2b-115">The string that was to be inserted into the control represented by the *hWnd* parameter when the **InputFailed** event was raised.</span></span>

<span data-ttu-id="dde2b-116">Para obter mais informações sobre o tipo de dados BSTR, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="dde2b-116">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="dde2b-117">*ShiftKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dde2b-117">*ShiftKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde2b-118">O estado dos modificadores de teclado, incluindo SHIFT, CAPS, CTRL e ALT.</span><span class="sxs-lookup"><span data-stu-id="dde2b-118">The state of the keyboard modifiers, including SHIFT, CAPS, CTRL, and ALT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dde2b-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dde2b-119">Return value</span></span>

<span data-ttu-id="dde2b-120">Se esse evento for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dde2b-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dde2b-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dde2b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dde2b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="dde2b-122">Remarks</span></span>

<span data-ttu-id="dde2b-123">O evento **InputFailed** ocorre quando o foco de entrada é alterado antes que a entrada do usuário seja inserida no controle anexado.</span><span class="sxs-lookup"><span data-stu-id="dde2b-123">The **InputFailed** event occurs when input focus changes before user input was inserted into the attached control.</span></span> <span data-ttu-id="dde2b-124">Por exemplo, se o usuário inserir a tinta no painel de escrita, tocará em outro controle de edição antes que o reconhecedor tenha tido a oportunidade de concluir, esse evento será acionado.</span><span class="sxs-lookup"><span data-stu-id="dde2b-124">For example, if the user enters ink into the writing pad, then taps on another edit control before the recognizer has had a chance to finish, this event fires.</span></span>

<span data-ttu-id="dde2b-125">Usando o identificador de janela passado para esse evento, você pode optar por inserir o texto por conta própria quando esse evento ocorrer.</span><span class="sxs-lookup"><span data-stu-id="dde2b-125">Using the window handle passed into this event, you can choose to insert the text yourself when this event occurs.</span></span>

> [!Note]  
> <span data-ttu-id="dde2b-126">A partir do Microsoft Windows XP Tablet PC Edition 2005, o evento **InputFailed** não se aplica mais.</span><span class="sxs-lookup"><span data-stu-id="dde2b-126">Starting with Microsoft Windows XP Tablet PC Edition 2005, the **InputFailed** event no longer applies.</span></span> <span data-ttu-id="dde2b-127">O texto sempre é inserido antes do foco ser alterado.</span><span class="sxs-lookup"><span data-stu-id="dde2b-127">Text is always inserted before focus changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dde2b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dde2b-128">Requirements</span></span>



| <span data-ttu-id="dde2b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dde2b-129">Requirement</span></span> | <span data-ttu-id="dde2b-130">Valor</span><span class="sxs-lookup"><span data-stu-id="dde2b-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dde2b-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dde2b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dde2b-132">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dde2b-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="dde2b-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dde2b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dde2b-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dde2b-134">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="dde2b-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dde2b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dde2b-136"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dde2b-136"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dde2b-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dde2b-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="dde2b-138"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dde2b-138"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="dde2b-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="dde2b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde2b-140">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="dde2b-140">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 





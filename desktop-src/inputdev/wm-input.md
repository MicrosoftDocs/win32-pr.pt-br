---
title: Mensagem de WM_INPUT (WinUser. h)
description: Enviado para a janela que está obtendo entrada bruta. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- Entrada de mouse e teclado de mensagem WM_INPUT
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369497"
---
# <a name="wm_input-message"></a><span data-ttu-id="ec163-105">Mensagem de entrada do WM \_</span><span class="sxs-lookup"><span data-stu-id="ec163-105">WM\_INPUT message</span></span>

<span data-ttu-id="ec163-106">Enviado para a janela que está obtendo entrada bruta.</span><span class="sxs-lookup"><span data-stu-id="ec163-106">Sent to the window that is getting raw input.</span></span>

<span data-ttu-id="ec163-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ec163-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a><span data-ttu-id="ec163-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec163-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec163-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec163-109">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="ec163-110">O código de entrada.</span><span class="sxs-lookup"><span data-stu-id="ec163-110">The input code.</span></span> <span data-ttu-id="ec163-111">Use a macro [**\_ \_ \_ wParam do código rawinput**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="ec163-111">Use [**GET\_RAWINPUT\_CODE\_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) macro to get the value.</span></span>

<span data-ttu-id="ec163-112">Pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ec163-112">Can be one of the following values:</span></span>

| <span data-ttu-id="ec163-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ec163-113">Value</span></span> | <span data-ttu-id="ec163-114">Significado</span><span class="sxs-lookup"><span data-stu-id="ec163-114">Meaning</span></span> |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <span data-ttu-id="ec163-115"><dt>**Rim \_ ENTRADA**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ec163-115"><dt>**RIM\_INPUT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="ec163-116">Ocorreu uma entrada enquanto o aplicativo estava em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="ec163-116">Input occurred while the application was in the foreground.</span></span> </br> <span data-ttu-id="ec163-117">O aplicativo deve chamar [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para que o sistema possa executar a limpeza.</span><span class="sxs-lookup"><span data-stu-id="ec163-117">The application must call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) so the system can perform cleanup.</span></span> |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <span data-ttu-id="ec163-118"><dt>**Rim \_ INPUTSINK**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ec163-118"><dt>**RIM\_INPUTSINK**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="ec163-119">Ocorreu uma entrada enquanto o aplicativo não estava em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="ec163-119">Input occurred while the application was not in the foreground.</span></span> |

</dd> <dt>

<span data-ttu-id="ec163-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec163-120">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="ec163-121">Um identificador **HRAWINPUT** para a estrutura [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) que contém a entrada bruta do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ec163-121">A **HRAWINPUT** handle to the [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structure that contains the raw input from the device.</span></span> <span data-ttu-id="ec163-122">Para obter os dados brutos, use esse identificador na chamada para [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).</span><span class="sxs-lookup"><span data-stu-id="ec163-122">To get the raw data, use this handle in the call to [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec163-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ec163-123">Return value</span></span>

<span data-ttu-id="ec163-124">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="ec163-124">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec163-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec163-125">Remarks</span></span>

<span data-ttu-id="ec163-126">A entrada bruta está disponível somente quando o aplicativo chama [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) com especificações de dispositivo válidas.</span><span class="sxs-lookup"><span data-stu-id="ec163-126">Raw input is available only when the application calls [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with valid device specifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec163-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec163-127">Requirements</span></span>

| <span data-ttu-id="ec163-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec163-128">Requirement</span></span> | <span data-ttu-id="ec163-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ec163-129">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="ec163-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec163-130">Minimum supported client</span></span> | <span data-ttu-id="ec163-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ec163-131">Windows XP \[desktop apps only\]</span></span> |
| <span data-ttu-id="ec163-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec163-132">Minimum supported server</span></span> | <span data-ttu-id="ec163-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec163-133">Windows Server 2003 \[desktop apps only\]</span></span> |
| <span data-ttu-id="ec163-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec163-134">Header</span></span> | <dl> <span data-ttu-id="ec163-135"><dt>**WinUser. h (incluir Windows. h)**</dt></span><span class="sxs-lookup"><span data-stu-id="ec163-135"><dt>**Winuser.h (include Windows.h)** </dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="ec163-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec163-136">See also</span></span>

<span data-ttu-id="ec163-137">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ec163-137">**Reference**</span></span>

[<span data-ttu-id="ec163-138">**GetRawInputData**</span><span class="sxs-lookup"><span data-stu-id="ec163-138">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[<span data-ttu-id="ec163-139">**RegisterRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="ec163-139">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="ec163-140">**RAWINPUT**</span><span class="sxs-lookup"><span data-stu-id="ec163-140">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)

[<span data-ttu-id="ec163-141">**OBTER \_ \_ wParam do código rawinput \_**</span><span class="sxs-lookup"><span data-stu-id="ec163-141">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

<span data-ttu-id="ec163-142">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ec163-142">**Conceptual**</span></span>

[<span data-ttu-id="ec163-143">Entrada bruta</span><span class="sxs-lookup"><span data-stu-id="ec163-143">Raw Input</span></span>](raw-input.md)

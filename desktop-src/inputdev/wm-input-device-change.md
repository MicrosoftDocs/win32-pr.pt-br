---
title: Mensagem de WM_INPUT_DEVICE_CHANGE (WinUser. h)
description: Enviado para a janela que está registrada para receber entrada bruta. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- Entrada de mouse e teclado de mensagem WM_INPUT_DEVICE_CHANGE
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0edb6dbfbcfa9e024ba85613e3b7671e5f416397
ms.sourcegitcommit: 47d1f3859035a69340571bf50c3d36e0abeb2126
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "104008541"
---
# <a name="wm_input_device_change-message"></a><span data-ttu-id="d8d7d-105">WM_INPUT_DEVICE_CHANGE mensagem</span><span class="sxs-lookup"><span data-stu-id="d8d7d-105">WM_INPUT_DEVICE_CHANGE message</span></span>

## <a name="description"></a><span data-ttu-id="d8d7d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8d7d-106">Description</span></span>

<span data-ttu-id="d8d7d-107">Enviado para a janela que está registrada para receber entrada bruta.</span><span class="sxs-lookup"><span data-stu-id="d8d7d-107">Sent to the window that registered to receive raw input.</span></span> 

<span data-ttu-id="d8d7d-108">As notificações de entrada brutas estão disponíveis somente depois que o aplicativo chama [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) com [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) sinalizador.</span><span class="sxs-lookup"><span data-stu-id="d8d7d-108">Raw input notifications are available only after the application calls [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) with [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) flag.</span></span>

<span data-ttu-id="d8d7d-109">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d8d7d-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a><span data-ttu-id="d8d7d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8d7d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8d7d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d8d7d-111">*wParam*</span></span>

</dt> <dd>

<span data-ttu-id="d8d7d-112">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="d8d7d-112">Type: **WPARAM**</span></span>

<span data-ttu-id="d8d7d-113">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8d7d-113">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="d8d7d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d8d7d-114">Value</span></span>                    | <span data-ttu-id="d8d7d-115">Significado</span><span class="sxs-lookup"><span data-stu-id="d8d7d-115">Meaning</span></span>                                    |
|--------------------------|--------------------------------------------|
| <span data-ttu-id="d8d7d-116">**chegada de GIDC \_**</span><span class="sxs-lookup"><span data-stu-id="d8d7d-116">**GIDC\_ARRIVAL**</span></span> </br><span data-ttu-id="d8d7d-117">1</span><span class="sxs-lookup"><span data-stu-id="d8d7d-117">1</span></span> | <span data-ttu-id="d8d7d-118">Um novo dispositivo foi adicionado ao sistema.</span><span class="sxs-lookup"><span data-stu-id="d8d7d-118">A new device has been added to the system.</span></span> </br> <span data-ttu-id="d8d7d-119">Você pode chamar [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) para obter mais informações sobre o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8d7d-119">You can call [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) to get more information regarding the device.</span></span> |
| <span data-ttu-id="d8d7d-120">**remoção de GIDC \_**</span><span class="sxs-lookup"><span data-stu-id="d8d7d-120">**GIDC\_REMOVAL**</span></span> </br><span data-ttu-id="d8d7d-121">2</span><span class="sxs-lookup"><span data-stu-id="d8d7d-121">2</span></span> | <span data-ttu-id="d8d7d-122">Um dispositivo foi removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="d8d7d-122">A device has been removed from the system.</span></span> |

</dd> <dt>

<span data-ttu-id="d8d7d-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d8d7d-123">*lParam*</span></span> 

</dt> <dd>

<span data-ttu-id="d8d7d-124">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="d8d7d-124">Type: **LPARAM**</span></span>

<span data-ttu-id="d8d7d-125">O **identificador** para o dispositivo de entrada bruto.</span><span class="sxs-lookup"><span data-stu-id="d8d7d-125">The **HANDLE** to the raw input device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8d7d-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8d7d-126">Return value</span></span>

<span data-ttu-id="d8d7d-127">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="d8d7d-127">If an application processes this message, it should return zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8d7d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8d7d-128">See also</span></span>

<span data-ttu-id="d8d7d-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="d8d7d-129">**Conceptual**</span></span>

[<span data-ttu-id="d8d7d-130">Entrada bruta</span><span class="sxs-lookup"><span data-stu-id="d8d7d-130">Raw Input</span></span>](/windows/desktop/inputdev/raw-input)

<span data-ttu-id="d8d7d-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d8d7d-131">**Reference**</span></span>

[<span data-ttu-id="d8d7d-132">RegisterRawInputDevices</span><span class="sxs-lookup"><span data-stu-id="d8d7d-132">RegisterRawInputDevices</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[<span data-ttu-id="d8d7d-133">Estrutura RAWINPUTDEVICE</span><span class="sxs-lookup"><span data-stu-id="d8d7d-133">RAWINPUTDEVICE structure</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 


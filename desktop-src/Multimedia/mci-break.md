---
title: MCI_BREAK comando (mmsystem. h)
description: O \_ comando MCI Break define uma chave de interrupção para um dispositivo MCI. O MCI dá suporte a esse comando diretamente, em vez de passá-lo para o dispositivo. Qualquer aplicativo MCI pode usar esse comando.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- Multimídia do Windows de comando MCI_BREAK
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b17e3796192344ef974fed1af7229d41746aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454987"
---
# <a name="mci_break-command"></a><span data-ttu-id="c071f-106">Comando de interrupção do MCI \_</span><span class="sxs-lookup"><span data-stu-id="c071f-106">MCI\_BREAK command</span></span>

<span data-ttu-id="c071f-107">O \_ comando MCI Break define uma chave de interrupção para um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c071f-107">The MCI\_BREAK command sets a break key for an MCI device.</span></span> <span data-ttu-id="c071f-108">O MCI dá suporte a esse comando diretamente, em vez de passá-lo para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c071f-108">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="c071f-109">Qualquer aplicativo MCI pode usar esse comando.</span><span class="sxs-lookup"><span data-stu-id="c071f-109">Any MCI application can use this command.</span></span>

<span data-ttu-id="c071f-110">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="c071f-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
);
```



## <a name="parameters"></a><span data-ttu-id="c071f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c071f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c071f-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c071f-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c071f-113">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="c071f-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c071f-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c071f-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c071f-115">\_Notificação MCI, espera de MCI \_ ou, para dispositivos de vídeo digital e gravador de fita de vídeo (VCR), \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="c071f-115">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and video-cassette recorder (VCR) devices, MCI\_TEST.</span></span> <span data-ttu-id="c071f-116">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c071f-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c071f-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*</span><span class="sxs-lookup"><span data-stu-id="c071f-117"><span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*</span></span>
</dt> <dd>

<span data-ttu-id="c071f-118">Ponteiro para uma estrutura de [**\_ \_ parâmetros de interrupção MCI**](mci-break-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c071f-118">Pointer to an [**MCI\_ BREAK\_PARMS**](mci-break-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c071f-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c071f-119">Return Value</span></span>

<span data-ttu-id="c071f-120">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="c071f-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c071f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c071f-121">Remarks</span></span>

<span data-ttu-id="c071f-122">Talvez seja necessário pressionar a tecla Break várias vezes para interromper uma operação de espera.</span><span class="sxs-lookup"><span data-stu-id="c071f-122">You might have to press the break key multiple times to interrupt a wait operation.</span></span> <span data-ttu-id="c071f-123">Pressionar a tecla Break depois que uma espera de dispositivo é cancelada pode enviar a interrupção para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c071f-123">Pressing the break key after a device wait is canceled can send the break to an application.</span></span> <span data-ttu-id="c071f-124">Se um aplicativo tiver uma ação definida para o código de chave virtual, ele poderá responder inadvertidamente à interrupção.</span><span class="sxs-lookup"><span data-stu-id="c071f-124">If an application has an action defined for the virtual-key code, then it can inadvertently respond to the break.</span></span> <span data-ttu-id="c071f-125">Por exemplo, um aplicativo que usa VK \_ Cancel para uma tecla aceleradora pode responder à tecla Ctrl + Break padrão se for pressionado após a cancelamento de uma espera.</span><span class="sxs-lookup"><span data-stu-id="c071f-125">For example, an application using VK\_CANCEL for an accelerator key can respond to the default CTRL+BREAK key if it is pressed after a wait is canceled.</span></span>

<span data-ttu-id="c071f-126">Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos:</span><span class="sxs-lookup"><span data-stu-id="c071f-126">The following additional flags apply to all devices:</span></span>

<dl> <dt>

<span data-ttu-id="c071f-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>\_HWND de interrupção de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c071f-127"><span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI\_BREAK\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="c071f-128">O membro **hwndBreak** da estrutura identificada por *lpBreak* contém um identificador de janela que deve ser a janela atual para habilitar a detecção de quebras para o dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="c071f-128">The **hwndBreak** member of the structure identified by *lpBreak* contains a window handle that must be the current window in order to enable break detection for that MCI device.</span></span> <span data-ttu-id="c071f-129">Normalmente, essa é a janela principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c071f-129">This is usually the application's main window.</span></span> <span data-ttu-id="c071f-130">Se omitido, o MCI não verificará o identificador de janela da janela atual.</span><span class="sxs-lookup"><span data-stu-id="c071f-130">If omitted, MCI does not check the window handle of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="c071f-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>\_chave de interrupção MCI \_</span><span class="sxs-lookup"><span data-stu-id="c071f-131"><span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>MCI\_BREAK\_KEY</span></span>
</dt> <dd>

<span data-ttu-id="c071f-132">O membro **nVirtKey** da estrutura identificada por *lpBreak* especifica o código de chave virtual usado para a chave de interrupção.</span><span class="sxs-lookup"><span data-stu-id="c071f-132">The **nVirtKey** member of the structure identified by *lpBreak* specifies the virtual-key code used for the break key.</span></span> <span data-ttu-id="c071f-133">Por padrão, o MCI atribui CTRL + BREAK como a tecla Break.</span><span class="sxs-lookup"><span data-stu-id="c071f-133">By default, MCI assigns CTRL+BREAK as the break key.</span></span> <span data-ttu-id="c071f-134">Esse sinalizador será necessário se a \_ interrupção do MCI \_ não for especificada.</span><span class="sxs-lookup"><span data-stu-id="c071f-134">This flag is required if MCI\_BREAK\_OFF is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="c071f-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>interrupção do MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="c071f-135"><span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI\_BREAK\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="c071f-136">Desabilita qualquer chave de interrupção existente para o dispositivo indicado.</span><span class="sxs-lookup"><span data-stu-id="c071f-136">Disables any existing break key for the indicated device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c071f-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c071f-137">Requirements</span></span>



| <span data-ttu-id="c071f-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c071f-138">Requirement</span></span> | <span data-ttu-id="c071f-139">Valor</span><span class="sxs-lookup"><span data-stu-id="c071f-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c071f-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c071f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c071f-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c071f-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c071f-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c071f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c071f-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c071f-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c071f-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c071f-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c071f-145"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c071f-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c071f-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="c071f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c071f-147">MCI</span><span class="sxs-lookup"><span data-stu-id="c071f-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c071f-148">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="c071f-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


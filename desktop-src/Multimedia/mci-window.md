---
title: MCI_WINDOW comando (mmsystem. h)
description: O \_ comando da janela MCI especifica a janela e as características da janela para dispositivos gráficos. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- Multimídia do Windows de comando MCI_WINDOW
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918595"
---
# <a name="mci_window-command"></a><span data-ttu-id="aaab8-105">\_Comando de janela MCI</span><span class="sxs-lookup"><span data-stu-id="aaab8-105">MCI\_WINDOW command</span></span>

<span data-ttu-id="aaab8-106">O \_ comando da janela MCI especifica a janela e as características da janela para dispositivos gráficos.</span><span class="sxs-lookup"><span data-stu-id="aaab8-106">The MCI\_WINDOW command specifies the window and the window characteristics for graphic devices.</span></span> <span data-ttu-id="aaab8-107">Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="aaab8-107">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="aaab8-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="aaab8-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
);
```



## <a name="parameters"></a><span data-ttu-id="aaab8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aaab8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaab8-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="aaab8-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="aaab8-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="aaab8-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="aaab8-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="aaab8-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="aaab8-113">\_Notificação MCI, \_ espera MCI ou, para dispositivos de vídeo digital, teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="aaab8-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="aaab8-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="aaab8-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="aaab8-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*</span><span class="sxs-lookup"><span data-stu-id="aaab8-115"><span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*</span></span>
</dt> <dd>

<span data-ttu-id="aaab8-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="aaab8-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="aaab8-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="aaab8-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaab8-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="aaab8-118">Return Value</span></span>

<span data-ttu-id="aaab8-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="aaab8-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaab8-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="aaab8-120">Remarks</span></span>

<span data-ttu-id="aaab8-121">Os dispositivos gráficos devem criar uma janela padrão quando um dispositivo é aberto, mas não deve exibi-la até receber o comando [MCI \_ Play](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="aaab8-121">Graphic devices should create a default window when a device is opened but should not display it until they receive the [MCI\_PLAY](mci-play.md) command.</span></span> <span data-ttu-id="aaab8-122">O \_ comando da janela MCI é usado para fornecer uma janela criada pelo aplicativo ao dispositivo e alterar as características de exibição de uma janela de exibição padrão ou definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aaab8-122">The MCI\_WINDOW command is used to supply an application-created window to the device and to change the display characteristics of an application-defined or default display window.</span></span> <span data-ttu-id="aaab8-123">Se o aplicativo fornecer a janela de exibição, ele deverá estar preparado para atualizar um retângulo inválido na janela.</span><span class="sxs-lookup"><span data-stu-id="aaab8-123">If the application supplies the display window, it should be prepared to update an invalid rectangle on the window.</span></span>

<span data-ttu-id="aaab8-124">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="aaab8-124">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="aaab8-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>\_HWND de \_ janela \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="aaab8-125"><span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>MCI\_DGV\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="aaab8-126">O identificador da janela necessária para uso como destino é incluído no membro **HWND** da estrutura identificada por *lpWindow*.</span><span class="sxs-lookup"><span data-stu-id="aaab8-126">The handle of the window needed for use as the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span>

</dd> <dt>

<span data-ttu-id="aaab8-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>\_estado da \_ janela MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="aaab8-127"><span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>MCI\_DGV\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="aaab8-128">O membro **nCmdShow** da estrutura identificada por *lpWindow* contém parâmetros para definir o estado da janela.</span><span class="sxs-lookup"><span data-stu-id="aaab8-128">The **nCmdShow** member of the structure identified by *lpWindow* contains parameters for setting the window state.</span></span>

</dd> <dt>

<span data-ttu-id="aaab8-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>\_texto da \_ janela MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="aaab8-129"><span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>MCI\_DGV\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="aaab8-130">O membro **lpstrText** da estrutura identificada por *lpWindow* contém um endereço de um buffer que contém a legenda usada na barra de título da janela.</span><span class="sxs-lookup"><span data-stu-id="aaab8-130">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used in the window title bar.</span></span>

</dd> </dl>

<span data-ttu-id="aaab8-131">Para dispositivos de vídeo digital, o parâmetro *lpWindow* aponta para uma estrutura de [**\_ \_ \_ parâmetros de janela DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="aaab8-131">For digital-video devices, the *lpWindow* parameter points to an [**MCI\_DGV\_WINDOW\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) structure.</span></span>

<span data-ttu-id="aaab8-132">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo de **sobreposição** :</span><span class="sxs-lookup"><span data-stu-id="aaab8-132">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="aaab8-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>janela do MCI \_ OVLY \_ \_ desabilitar \_ Stretch</span><span class="sxs-lookup"><span data-stu-id="aaab8-133"><span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>MCI\_OVLY\_WINDOW\_DISABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="aaab8-134">Desabilita o alongamento da imagem.</span><span class="sxs-lookup"><span data-stu-id="aaab8-134">Disables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="aaab8-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>\_janela MCI \_ OVLY \_ habilitar \_ Stretch</span><span class="sxs-lookup"><span data-stu-id="aaab8-135"><span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI\_OVLY\_WINDOW\_ENABLE\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="aaab8-136">Habilita o alongamento da imagem.</span><span class="sxs-lookup"><span data-stu-id="aaab8-136">Enables stretching of the image.</span></span>

</dd> <dt>

<span data-ttu-id="aaab8-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>\_HWND de \_ janela \_ OVLY MCI</span><span class="sxs-lookup"><span data-stu-id="aaab8-137"><span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI\_OVLY\_WINDOW\_HWND</span></span>
</dt> <dd>

<span data-ttu-id="aaab8-138">O identificador da janela usada para o destino é incluído no membro **HWND** da estrutura identificada por *lpWindow*.</span><span class="sxs-lookup"><span data-stu-id="aaab8-138">The handle of the window used for the destination is included in the **hWnd** member of the structure identified by *lpWindow*.</span></span> <span data-ttu-id="aaab8-139">Defina esse sinalizador como \_ \_ padrão da janela MCI OVLY \_ para retornar à janela padrão.</span><span class="sxs-lookup"><span data-stu-id="aaab8-139">Set this flag to MCI\_OVLY\_WINDOW\_DEFAULT to return to the default window.</span></span>

</dd> <dt>

<span data-ttu-id="aaab8-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>\_estado da \_ janela MCI OVLY \_</span><span class="sxs-lookup"><span data-stu-id="aaab8-140"><span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>MCI\_OVLY\_WINDOW\_STATE</span></span>
</dt> <dd>

<span data-ttu-id="aaab8-141">O membro **nCmdShow** da estrutura *lpWindow* contém parâmetros para definir o estado da janela.</span><span class="sxs-lookup"><span data-stu-id="aaab8-141">The **nCmdShow** member of the *lpWindow* structure contains parameters for setting the window state.</span></span> <span data-ttu-id="aaab8-142">Esse sinalizador é equivalente a chamar a ação de [janela](/windows/win32/api/winuser/nf-winuser-showwindow) com o parâmetro *State* .</span><span class="sxs-lookup"><span data-stu-id="aaab8-142">This flag is equivalent to calling [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) with the *state* parameter.</span></span> <span data-ttu-id="aaab8-143">As constantes são as mesmas definidas no WINDOWS. H (por exemplo \_ , ocultar SW, SW \_ minimize ou SW \_ normal).</span><span class="sxs-lookup"><span data-stu-id="aaab8-143">The constants are the same as those defined in WINDOWS.H (such as SW\_HIDE, SW\_MINIMIZE, or SW\_SHOWNORMAL).</span></span>

</dd> <dt>

<span data-ttu-id="aaab8-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>\_texto da \_ janela MCI OVLY \_</span><span class="sxs-lookup"><span data-stu-id="aaab8-144"><span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>MCI\_OVLY\_WINDOW\_TEXT</span></span>
</dt> <dd>

<span data-ttu-id="aaab8-145">O membro **lpstrText** da estrutura identificada por *lpWindow* contém um endereço de um buffer que contém a legenda usada para a janela.</span><span class="sxs-lookup"><span data-stu-id="aaab8-145">The **lpstrText** member of the structure identified by *lpWindow* contains an address of a buffer containing the caption used for the window.</span></span>

</dd> </dl>

<span data-ttu-id="aaab8-146">Para dispositivos de sobreposição de vídeo, o parâmetro *lpWindow* aponta para uma estrutura de [**\_ \_ \_ parâmetros de janela OVLY MCI**](mci-ovly-window-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="aaab8-146">For video-overlay devices, the *lpWindow* parameter points to an [**MCI\_OVLY\_WINDOW\_PARMS**](mci-ovly-window-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaab8-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aaab8-147">Requirements</span></span>



| <span data-ttu-id="aaab8-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaab8-148">Requirement</span></span> | <span data-ttu-id="aaab8-149">Valor</span><span class="sxs-lookup"><span data-stu-id="aaab8-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaab8-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aaab8-150">Minimum supported client</span></span><br/> | <span data-ttu-id="aaab8-151">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aaab8-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aaab8-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aaab8-152">Minimum supported server</span></span><br/> | <span data-ttu-id="aaab8-153">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aaab8-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="aaab8-154">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="aaab8-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="aaab8-155"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aaab8-155"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaab8-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="aaab8-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaab8-157">MCI</span><span class="sxs-lookup"><span data-stu-id="aaab8-157">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="aaab8-158">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="aaab8-158">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


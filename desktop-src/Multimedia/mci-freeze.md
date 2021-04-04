---
title: MCI_FREEZE comando (mmsystem. h)
description: O \_ comando congelar do MCI congela o movimento na tela. Dispositivos de vídeo digital, de sobreposição de vídeo e VCR reconhecem este comando.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- Multimídia do Windows de comando MCI_FREEZE
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009062"
---
# <a name="mci_freeze-command"></a><span data-ttu-id="07b15-105">\_Comando congelar MCI</span><span class="sxs-lookup"><span data-stu-id="07b15-105">MCI\_FREEZE command</span></span>

<span data-ttu-id="07b15-106">O \_ comando congelar do MCI congela o movimento na tela.</span><span class="sxs-lookup"><span data-stu-id="07b15-106">The MCI\_FREEZE command freezes motion on the display.</span></span> <span data-ttu-id="07b15-107">Dispositivos de vídeo digital, de sobreposição de vídeo e VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="07b15-107">Digital-video, video-overlay, and VCR devices recognize this command.</span></span>

<span data-ttu-id="07b15-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="07b15-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
);
```



## <a name="parameters"></a><span data-ttu-id="07b15-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07b15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07b15-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="07b15-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="07b15-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="07b15-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="07b15-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="07b15-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="07b15-113">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="07b15-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="07b15-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="07b15-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b15-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*</span><span class="sxs-lookup"><span data-stu-id="07b15-115"><span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*</span></span>
</dt> <dd>

<span data-ttu-id="07b15-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="07b15-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="07b15-117">(Dispositivos com parâmetros adicionais podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="07b15-117">(Devices with additional parameters might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07b15-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="07b15-118">Return Value</span></span>

<span data-ttu-id="07b15-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="07b15-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="07b15-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="07b15-120">Remarks</span></span>

<span data-ttu-id="07b15-121">Os seguintes sinalizadores adicionais são usados pelo tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="07b15-121">The following additional flags are used by the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="07b15-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>\_ \_ congelamento de DGV MCI \_ em</span><span class="sxs-lookup"><span data-stu-id="07b15-122"><span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>MCI\_DGV\_FREEZE\_AT</span></span>
</dt> <dd>

<span data-ttu-id="07b15-123">O membro **RC** da estrutura identificada por *lpFreeze* contém um retângulo válido.</span><span class="sxs-lookup"><span data-stu-id="07b15-123">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="07b15-124">O retângulo especifica uma região dentro do buffer de quadro que terá o bit de máscara de bloqueio para cada pixel ativado.</span><span class="sxs-lookup"><span data-stu-id="07b15-124">The rectangle specifies a region within the frame buffer that will have the lock mask bit for each pixel turned on.</span></span> <span data-ttu-id="07b15-125">Os pixels especificados não serão atualizados até que o bit de máscara de bloqueio seja desativado.</span><span class="sxs-lookup"><span data-stu-id="07b15-125">The specified pixels will not be updated until their lock mask bit is turned off.</span></span> <span data-ttu-id="07b15-126">Se esse sinalizador não for especificado, o retângulo padronizará para todo o buffer de quadro.</span><span class="sxs-lookup"><span data-stu-id="07b15-126">If this flag is not specified, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="07b15-127">Esse sinalizador só terá suporte se o comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) retornar **true** para o \_ DGV MCI \_ GETDEVCAPS \_ puder \_ bloquear o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="07b15-127">This flag is supported only if the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command returns **TRUE** for the MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK flag.</span></span>

</dd> <dt>

<span data-ttu-id="07b15-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>\_congelamento de DGV MCI \_ \_ fora do</span><span class="sxs-lookup"><span data-stu-id="07b15-128"><span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>MCI\_DGV\_FREEZE\_OUTSIDE</span></span>
</dt> <dd>

<span data-ttu-id="07b15-129">A área fora da região especificada para o \_ sinalizador MCI DGV \_ congelar \_ em está congelada.</span><span class="sxs-lookup"><span data-stu-id="07b15-129">The area outside the region specified for the MCI\_DGV\_FREEZE\_AT flag is frozen.</span></span>

</dd> </dl>

<span data-ttu-id="07b15-130">Para dispositivos de vídeo digital, o parâmetro *lpFreeze* aponta para uma estrutura [**MCI de \_ DGV \_ congelable \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="07b15-130">For digital-video devices, the *lpFreeze* parameter points to an [**MCI\_DGV\_FREEZE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="07b15-131">Os seguintes sinalizadores adicionais são usados pelo tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="07b15-131">The following additional flags are used by the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="07b15-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>\_campo de \_ congelamento de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="07b15-132"><span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>MCI\_VCR\_FREEZE\_FIELD</span></span>
</dt> <dd>

<span data-ttu-id="07b15-133">Congelar apenas um membro do quadro atual.</span><span class="sxs-lookup"><span data-stu-id="07b15-133">Freeze only one member of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="07b15-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>\_quadro de \_ congelamento de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="07b15-134"><span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>MCI\_VCR\_FREEZE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="07b15-135">Congele os dois campos do quadro atual.</span><span class="sxs-lookup"><span data-stu-id="07b15-135">Freeze both fields of the current frame.</span></span>

</dd> <dt>

<span data-ttu-id="07b15-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>\_entrada de \_ congelamento de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="07b15-136"><span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>MCI\_VCR\_FREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="07b15-137">Congelar o quadro atual na tela (usado para gravação).</span><span class="sxs-lookup"><span data-stu-id="07b15-137">Freeze the current frame on the screen (used for recording).</span></span>

</dd> <dt>

<span data-ttu-id="07b15-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>\_saída de \_ congelamento de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="07b15-138"><span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>MCI\_VCR\_FREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="07b15-139">Congele o quadro atual do VCR (usado com a captura de quadros).</span><span class="sxs-lookup"><span data-stu-id="07b15-139">Freeze the current frame from the VCR (used with frame capture).</span></span>

</dd> </dl>

<span data-ttu-id="07b15-140">Para dispositivos VCR, o parâmetro *lpFreeze* aponta para uma estrutura de [**\_ \_ parâmetros genéricos MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="07b15-140">For VCR devices, the *lpFreeze* parameter points to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

<span data-ttu-id="07b15-141">O seguinte sinalizador adicional é usado pelo tipo de dispositivo de **sobreposição** :</span><span class="sxs-lookup"><span data-stu-id="07b15-141">The following additional flag is used by the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="07b15-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect MCI</span><span class="sxs-lookup"><span data-stu-id="07b15-142"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="07b15-143">O membro **RC** da estrutura identificada por *lpFreeze* contém um retângulo válido.</span><span class="sxs-lookup"><span data-stu-id="07b15-143">The **rc** member of the structure identified by *lpFreeze* contains a valid rectangle.</span></span> <span data-ttu-id="07b15-144">Se esse sinalizador não for especificado, o driver do dispositivo congelará o quadro inteiro.</span><span class="sxs-lookup"><span data-stu-id="07b15-144">If this flag is not specified, the device driver will freeze the entire frame.</span></span>

</dd> </dl>

<span data-ttu-id="07b15-145">Para dispositivos de sobreposição de vídeo, o parâmetro *lpFreeze* aponta para uma estrutura de [**parâmetros MCI do \_ OVLY \_ Rect \_**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="07b15-145">For video-overlay devices, the *lpFreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="07b15-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07b15-146">Requirements</span></span>



| <span data-ttu-id="07b15-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b15-147">Requirement</span></span> | <span data-ttu-id="07b15-148">Valor</span><span class="sxs-lookup"><span data-stu-id="07b15-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b15-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07b15-149">Minimum supported client</span></span><br/> | <span data-ttu-id="07b15-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="07b15-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="07b15-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07b15-151">Minimum supported server</span></span><br/> | <span data-ttu-id="07b15-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="07b15-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="07b15-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="07b15-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="07b15-154"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07b15-154"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07b15-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="07b15-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b15-156">MCI</span><span class="sxs-lookup"><span data-stu-id="07b15-156">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="07b15-157">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="07b15-157">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


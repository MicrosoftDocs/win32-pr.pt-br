---
title: MCI_STEP comando (mmsystem. h)
description: O \_ comando da etapa MCI percorre o jogador um ou mais quadros. Dispositivos Digital-Video, VCR e CAV-Format VIDEODISC reconhecem este comando.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- Multimídia do Windows de comando MCI_STEP
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085146"
---
# <a name="mci_step-command"></a><span data-ttu-id="33416-105">\_Comando de etapa MCI</span><span class="sxs-lookup"><span data-stu-id="33416-105">MCI\_STEP command</span></span>

<span data-ttu-id="33416-106">O \_ comando da etapa MCI percorre o jogador um ou mais quadros.</span><span class="sxs-lookup"><span data-stu-id="33416-106">The MCI\_STEP command steps the player one or more frames.</span></span> <span data-ttu-id="33416-107">Dispositivos Digital-Video, VCR e CAV-Format VIDEODISC reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="33416-107">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="33416-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="33416-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
);
```



## <a name="parameters"></a><span data-ttu-id="33416-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33416-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33416-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="33416-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="33416-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="33416-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="33416-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="33416-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="33416-113">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="33416-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="33416-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="33416-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="33416-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*</span><span class="sxs-lookup"><span data-stu-id="33416-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*</span></span>
</dt> <dd>

<span data-ttu-id="33416-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="33416-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="33416-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="33416-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33416-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="33416-118">Return Value</span></span>

<span data-ttu-id="33416-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="33416-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="33416-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="33416-120">Remarks</span></span>

<span data-ttu-id="33416-121">Esse comando dá suporte a dispositivos que retornam **true** para o MCI \_ GETDEVCAPS \_ tem \_ um sinalizador de vídeo do comando [ \_ GETDEVCAPS MCI](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="33416-121">This command supports devices that return **TRUE** to the MCI\_GETDEVCAPS\_HAS\_VIDEO flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

<span data-ttu-id="33416-122">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="33416-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="33416-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>\_quadros de \_ etapa MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="33416-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>MCI\_DGV\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="33416-124">O membro **dwFrames** da estrutura identificada por *lpStep* especifica o número de quadros a serem adiantados antes de exibir outra imagem.</span><span class="sxs-lookup"><span data-stu-id="33416-124">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="33416-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>etapa do MCI \_ DGV \_ \_ inversa</span><span class="sxs-lookup"><span data-stu-id="33416-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>MCI\_DGV\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="33416-126">Etapas em ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="33416-126">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="33416-127">Para dispositivos de vídeo digital, o parâmetro *lpStep* aponta para uma estrutura de [**\_ \_ \_ parâmetros de etapa DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) .</span><span class="sxs-lookup"><span data-stu-id="33416-127">For digital-video devices, the *lpStep* parameter points to an [**MCI\_DGV\_STEP\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) structure.</span></span>

<span data-ttu-id="33416-128">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="33416-128">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="33416-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>\_quadros de \_ etapa do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="33416-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>MCI\_VCR\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="33416-130">O membro **dwFrames** da estrutura identificada por *lpStep* especifica o número de quadros a serem adiantados antes de exibir outra imagem.</span><span class="sxs-lookup"><span data-stu-id="33416-130">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="33416-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>\_etapa do VCR MCI \_ \_ inverso</span><span class="sxs-lookup"><span data-stu-id="33416-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>MCI\_VCR\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="33416-132">Etapas em ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="33416-132">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="33416-133">Para dispositivos VCR, o parâmetro *lpStep* aponta para uma estrutura de parâmetros de [**etapa de \_ VCR \_ \_ MCI**](mci-vcr-step-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="33416-133">For VCR devices, the *lpStep* parameter points to an [**MCI\_VCR\_STEP\_PARMS**](mci-vcr-step-parms.md) structure.</span></span>

<span data-ttu-id="33416-134">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VIDEODISC** :</span><span class="sxs-lookup"><span data-stu-id="33416-134">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="33416-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>\_quadros de \_ etapa de VD do MCI \_</span><span class="sxs-lookup"><span data-stu-id="33416-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>MCI\_VD\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="33416-136">O membro **dwFrames** da estrutura identificada por *lpStep* especifica o número de quadros a serem etapa.</span><span class="sxs-lookup"><span data-stu-id="33416-136">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to step.</span></span>

</dd> <dt>

<span data-ttu-id="33416-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>reversão de \_ etapa de VD MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="33416-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>MCI\_VD\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="33416-138">Etapas em ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="33416-138">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="33416-139">Para dispositivos VIDEODISC, o parâmetro *lpStep* aponta para uma estrutura de parâmetros de etapa de VD do [**MCI \_ \_ \_**](mci-vd-step-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="33416-139">For videodisc devices, the *lpStep* parameter points to an [**MCI\_VD\_STEP\_PARMS**](mci-vd-step-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="33416-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33416-140">Requirements</span></span>



| <span data-ttu-id="33416-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="33416-141">Requirement</span></span> | <span data-ttu-id="33416-142">Valor</span><span class="sxs-lookup"><span data-stu-id="33416-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33416-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33416-143">Minimum supported client</span></span><br/> | <span data-ttu-id="33416-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="33416-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="33416-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33416-145">Minimum supported server</span></span><br/> | <span data-ttu-id="33416-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="33416-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="33416-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="33416-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="33416-148"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33416-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33416-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="33416-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33416-150">MCI</span><span class="sxs-lookup"><span data-stu-id="33416-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="33416-151">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="33416-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


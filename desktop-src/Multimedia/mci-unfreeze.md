---
title: MCI_UNFREEZE comando (mmsystem. h)
description: O \_ comando de descongelar do MCI restaura o movimento para uma área do buffer de vídeo congelada com o \_ comando MCI Freeze. Dispositivos digitais de vídeo, VCR e de sobreposição de vídeo reconhecem este comando.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- Multimídia do Windows de comando MCI_UNFREEZE
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8736e27998330f9337bb21569e145a4395e90020
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086300"
---
# <a name="mci_unfreeze-command"></a><span data-ttu-id="9a602-105">\_Comando de DEScongelar do MCI</span><span class="sxs-lookup"><span data-stu-id="9a602-105">MCI\_UNFREEZE command</span></span>

<span data-ttu-id="9a602-106">O \_ comando de descongelar do MCI restaura o movimento para uma área do buffer de vídeo congelada com o comando [MCI \_ Freeze](mci-freeze.md) .</span><span class="sxs-lookup"><span data-stu-id="9a602-106">The MCI\_UNFREEZE command restores motion to an area of the video buffer frozen with the [MCI\_FREEZE](mci-freeze.md) command.</span></span> <span data-ttu-id="9a602-107">Dispositivos digitais de vídeo, VCR e de sobreposição de vídeo reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="9a602-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="9a602-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="9a602-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
);
```



## <a name="parameters"></a><span data-ttu-id="9a602-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a602-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a602-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="9a602-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9a602-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="9a602-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="9a602-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="9a602-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9a602-113">\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI.</span><span class="sxs-lookup"><span data-stu-id="9a602-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="9a602-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9a602-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a602-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*</span><span class="sxs-lookup"><span data-stu-id="9a602-115"><span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="9a602-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="9a602-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="9a602-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="9a602-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a602-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9a602-118">Return Value</span></span>

<span data-ttu-id="9a602-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="9a602-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a602-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a602-120">Remarks</span></span>

<span data-ttu-id="9a602-121">O seguinte sinalizador adicional é usado com o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="9a602-121">The following additional flag is used with the **digitalvideo** device type:</span></span>

<span data-ttu-id="9a602-122">\_DGV \_ Rect MCI</span><span class="sxs-lookup"><span data-stu-id="9a602-122">MCI\_DGV\_RECT</span></span>

<span data-ttu-id="9a602-123">O membro **RC** da estrutura identificada por *lpUnfreeze* contém um retângulo de exibição válido.</span><span class="sxs-lookup"><span data-stu-id="9a602-123">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="9a602-124">O retângulo especifica uma região dentro do buffer de quadro cujos pixels devem ter seu bit de máscara de bloqueio desativado.</span><span class="sxs-lookup"><span data-stu-id="9a602-124">The rectangle specifies a region within the frame buffer whose pixels should have their lock mask bit turned off.</span></span> <span data-ttu-id="9a602-125">Regiões retangulares são especificadas conforme descrito para o comando [MCI \_ Put](mci-put.md) .</span><span class="sxs-lookup"><span data-stu-id="9a602-125">Rectangular regions are specified as described for the [MCI\_PUT](mci-put.md) command.</span></span> <span data-ttu-id="9a602-126">Se omitido, o retângulo assume como padrão o buffer de quadro inteiro.</span><span class="sxs-lookup"><span data-stu-id="9a602-126">If omitted, the rectangle defaults to the entire frame buffer.</span></span> <span data-ttu-id="9a602-127">Usando uma sequência de comandos congelar e descongelar com retângulos diferentes, os padrões arbitrários de bits de máscara de bloqueio podem ser descritos.</span><span class="sxs-lookup"><span data-stu-id="9a602-127">By using a sequence of freeze and unfreeze commands with different rectangles, arbitrary patterns of lock mask bits can be described.</span></span>

<span data-ttu-id="9a602-128">Para dispositivos de vídeo digital, o parâmetro *lpUnfreeze* aponta para uma estrutura **MCI \_ DGV \_ descongelar \_ parâmetros** .</span><span class="sxs-lookup"><span data-stu-id="9a602-128">For digital-video devices, the *lpUnfreeze* parameter points to an **MCI\_DGV\_UNFREEZE\_PARMS** structure.</span></span> <span data-ttu-id="9a602-129">Para obter mais informações, consulte os comentários para a estrutura de [**parâmetros do MCI \_ DGV \_ Rect \_**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="9a602-129">For more information, see the comments for the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="9a602-130">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :</span><span class="sxs-lookup"><span data-stu-id="9a602-130">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="9a602-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>\_entrada de \_ descongelar do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="9a602-131"><span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>MCI\_VCR\_UNFREEZE\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="9a602-132">Descongele a entrada.</span><span class="sxs-lookup"><span data-stu-id="9a602-132">Unfreeze the input.</span></span>

</dd> <dt>

<span data-ttu-id="9a602-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>\_saída de \_ descongelar do VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="9a602-133"><span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>MCI\_VCR\_UNFREEZE\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="9a602-134">Descongele a saída.</span><span class="sxs-lookup"><span data-stu-id="9a602-134">Unfreeze the output.</span></span>

</dd> </dl>

<span data-ttu-id="9a602-135">O seguinte sinalizador adicional é usado com o tipo de dispositivo de **sobreposição** :</span><span class="sxs-lookup"><span data-stu-id="9a602-135">The following additional flag is used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="9a602-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect MCI</span><span class="sxs-lookup"><span data-stu-id="9a602-136"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="9a602-137">O membro **RC** da estrutura identificada por *lpUnfreeze* contém um retângulo de exibição válido.</span><span class="sxs-lookup"><span data-stu-id="9a602-137">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="9a602-138">Esse é um parâmetro necessário.</span><span class="sxs-lookup"><span data-stu-id="9a602-138">This is a required parameter.</span></span>

</dd> </dl>

<span data-ttu-id="9a602-139">Para dispositivos de sobreposição de vídeo, o parâmetro *lpUnfreeze* aponta para uma estrutura de [**parâmetros MCI do \_ OVLY \_ Rect \_**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="9a602-139">For video-overlay devices, the *lpUnfreeze* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a602-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a602-140">Requirements</span></span>



| <span data-ttu-id="9a602-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a602-141">Requirement</span></span> | <span data-ttu-id="9a602-142">Valor</span><span class="sxs-lookup"><span data-stu-id="9a602-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a602-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a602-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9a602-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a602-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9a602-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a602-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9a602-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a602-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9a602-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9a602-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a602-148"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a602-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a602-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a602-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a602-150">MCI</span><span class="sxs-lookup"><span data-stu-id="9a602-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9a602-151">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="9a602-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


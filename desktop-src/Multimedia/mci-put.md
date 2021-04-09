---
title: MCI_PUT comando (mmsystem. h)
description: O \_ comando MCI Put define os retângulos de origem, destino e quadro. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- Multimídia do Windows de comando MCI_PUT
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fa4af30aa2b3aa6f7cdd50f453bc8edca83334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086508"
---
# <a name="mci_put-command"></a><span data-ttu-id="40454-105">Comando de put do MCI \_</span><span class="sxs-lookup"><span data-stu-id="40454-105">MCI\_PUT command</span></span>

<span data-ttu-id="40454-106">O \_ comando MCI Put define os retângulos de origem, destino e quadro.</span><span class="sxs-lookup"><span data-stu-id="40454-106">The MCI\_PUT command sets the source, destination, and frame rectangles.</span></span> <span data-ttu-id="40454-107">Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="40454-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="40454-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="40454-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="40454-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40454-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40454-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="40454-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="40454-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="40454-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="40454-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="40454-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="40454-113">\_Notificação MCI, \_ espera MCI ou, para dispositivos de vídeo digital, teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="40454-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="40454-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="40454-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="40454-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span><span class="sxs-lookup"><span data-stu-id="40454-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="40454-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="40454-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="40454-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="40454-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40454-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="40454-118">Return Value</span></span>

<span data-ttu-id="40454-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="40454-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="40454-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="40454-120">Remarks</span></span>

<span data-ttu-id="40454-121">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="40454-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="40454-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>\_cliente DGV \_ put do MCI \_</span><span class="sxs-lookup"><span data-stu-id="40454-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI\_DGV\_PUT\_CLIENT</span></span>
</dt> <dd>

<span data-ttu-id="40454-123">O retângulo definido para MCI \_ DGV \_ Rect aplica-se à posição da janela do cliente.</span><span class="sxs-lookup"><span data-stu-id="40454-123">The rectangle defined for MCI\_DGV\_RECT applies to the position of the client window.</span></span> <span data-ttu-id="40454-124">O retângulo especificado é relativo à janela pai da janela de exibição.</span><span class="sxs-lookup"><span data-stu-id="40454-124">The rectangle specified is relative to the parent window of the display window.</span></span> <span data-ttu-id="40454-125">\_A janela do MCI DGV \_ Put \_ deve ser definida simultaneamente com esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="40454-125">MCI\_DGV\_PUT\_WINDOW must be set concurrently with this flag.</span></span>

</dd> <dt>

<span data-ttu-id="40454-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>\_destino de \_ Put \_ DGV do MCI</span><span class="sxs-lookup"><span data-stu-id="40454-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>MCI\_DGV\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="40454-127">O retângulo definido para \_ o MCI DGV \_ Rect especifica um retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="40454-127">The rectangle defined for MCI\_DGV\_RECT specifies a destination rectangle.</span></span> <span data-ttu-id="40454-128">O retângulo de destino especifica a parte da janela do cliente associada a essa instância de driver de dispositivo que mostra a imagem ou o vídeo.</span><span class="sxs-lookup"><span data-stu-id="40454-128">The destination rectangle specifies the portion of the client window associated with this device driver instance that shows the image or video.</span></span>

</dd> <dt>

<span data-ttu-id="40454-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>\_quadro de \_ Put \_ DGV do MCI</span><span class="sxs-lookup"><span data-stu-id="40454-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI\_DGV\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="40454-130">O retângulo definido para \_ o MCI DGV \_ Rect aplica-se ao retângulo do quadro.</span><span class="sxs-lookup"><span data-stu-id="40454-130">The rectangle defined for MCI\_DGV\_RECT applies to the frame rectangle.</span></span> <span data-ttu-id="40454-131">O retângulo do quadro especifica a parte do buffer do quadro usado como o destino das imagens de vídeo obtidas do retângulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="40454-131">The frame rectangle specifies the portion of the frame buffer used as the destination of the video images obtained from the video rectangle.</span></span> <span data-ttu-id="40454-132">O vídeo deve ser dimensionado para caber no retângulo do buffer do quadro.</span><span class="sxs-lookup"><span data-stu-id="40454-132">The video should be scaled to fit within the frame buffer rectangle.</span></span>

<span data-ttu-id="40454-133">O retângulo é especificado em coordenadas de buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="40454-133">The rectangle is specified in frame buffer coordinates.</span></span> <span data-ttu-id="40454-134">O retângulo padrão é o buffer de quadro completo.</span><span class="sxs-lookup"><span data-stu-id="40454-134">The default rectangle is the full frame buffer.</span></span> <span data-ttu-id="40454-135">A especificação desse retângulo permite que o dispositivo dimensione a imagem à medida que digitaliza os dados.</span><span class="sxs-lookup"><span data-stu-id="40454-135">Specifying this rectangle lets the device scale the image as it digitizes the data.</span></span> <span data-ttu-id="40454-136">Os dispositivos que não podem dimensionar a imagem rejeitam esse comando com a \_ função sem suporte do MCIERR \_ .</span><span class="sxs-lookup"><span data-stu-id="40454-136">Devices that cannot scale the image reject this command with MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="40454-137">Você pode usar o \_ sinalizador MCI GETDEVCAPS \_ pode \_ ampliar com o [comando \_ GETDEVCAPS do MCI](mci-getdevcaps.md) para determinar se um dispositivo dimensiona a imagem.</span><span class="sxs-lookup"><span data-stu-id="40454-137">You can use the MCI\_GETDEVCAPS\_CAN\_STRETCH flag with the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command to determine if a device scales the image.</span></span> <span data-ttu-id="40454-138">Um dispositivo retornará **falso** se não for possível dimensionar a imagem.</span><span class="sxs-lookup"><span data-stu-id="40454-138">A device returns **FALSE** if it cannot scale the image.</span></span>

</dd> <dt>

<span data-ttu-id="40454-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>\_fonte de \_ Put \_ DGV MCI</span><span class="sxs-lookup"><span data-stu-id="40454-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>MCI\_DGV\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="40454-140">O retângulo definido para \_ o MCI DGV \_ Rect especifica um retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="40454-140">The rectangle defined for MCI\_DGV\_RECT specifies a source rectangle.</span></span> <span data-ttu-id="40454-141">O retângulo de origem especifica qual parte do buffer de quadro deve ser dimensionada para caber no retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="40454-141">The source rectangle specifies which portion of the frame buffer is to be scaled to fit into the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="40454-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>vídeo do MCI \_ DGV \_ Put \_</span><span class="sxs-lookup"><span data-stu-id="40454-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>MCI\_DGV\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="40454-143">O retângulo definido para \_ o MCI DGV \_ Rect aplica-se ao retângulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="40454-143">The rectangle defined for MCI\_DGV\_RECT applies to the video rectangle.</span></span> <span data-ttu-id="40454-144">O retângulo de vídeo especifica qual parte da fonte da apresentação atual é armazenada no buffer do quadro.</span><span class="sxs-lookup"><span data-stu-id="40454-144">The video rectangle specifies which portion of the current presentation source is stored in the frame buffer.</span></span> <span data-ttu-id="40454-145">O retângulo é especificado usando as coordenadas naturais da origem da apresentação.</span><span class="sxs-lookup"><span data-stu-id="40454-145">The rectangle is specified using the natural coordinates of the presentation source.</span></span> <span data-ttu-id="40454-146">Ele permite a especificação de corte que ocorre antes de armazenar imagens e vídeo no buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="40454-146">It allows the specification of cropping that occurs prior to storing images and video in the frame buffer.</span></span> <span data-ttu-id="40454-147">O retângulo padrão é a área de verificação ativa completa ou imagens e vídeos totalmente descompactados.</span><span class="sxs-lookup"><span data-stu-id="40454-147">The default rectangle is the full active scan area or the full decompressed images and video.</span></span>

</dd> <dt>

<span data-ttu-id="40454-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>\_janela do DGV \_ Put \_ do MCI</span><span class="sxs-lookup"><span data-stu-id="40454-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>MCI\_DGV\_PUT\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="40454-149">O retângulo definido para \_ o MCI DGV \_ Rect aplica-se à janela de exibição.</span><span class="sxs-lookup"><span data-stu-id="40454-149">The rectangle defined for MCI\_DGV\_RECT applies to the display window.</span></span> <span data-ttu-id="40454-150">Esse retângulo é relativo à janela pai da janela de exibição (geralmente a área de trabalho).</span><span class="sxs-lookup"><span data-stu-id="40454-150">This rectangle is relative to the parent window of the display window (usually the desktop).</span></span> <span data-ttu-id="40454-151">Se a janela não for especificada, o padrão será o tamanho e a posição da janela inicial.</span><span class="sxs-lookup"><span data-stu-id="40454-151">If the window is not specified, it defaults to the initial window size and position.</span></span>

</dd> <dt>

<span data-ttu-id="40454-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect MCI</span><span class="sxs-lookup"><span data-stu-id="40454-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="40454-153">O membro **RC** da estrutura identificada por *lpDest* contém um retângulo válido.</span><span class="sxs-lookup"><span data-stu-id="40454-153">The **rc** member of the structure identified by *lpDest* contains a valid rectangle.</span></span>

</dd> </dl>

<span data-ttu-id="40454-154">Para dispositivos de vídeo digital, *lpDest* aponta para uma estrutura [**MCI \_ DGV \_ colocar \_ parâmetros**](/previous-versions//dd743397(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="40454-154">For digital-video devices, *lpDest* points to an [**MCI\_DGV\_PUT\_PARMS**](/previous-versions//dd743397(v=vs.85)) structure.</span></span>

<span data-ttu-id="40454-155">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo de **sobreposição** :</span><span class="sxs-lookup"><span data-stu-id="40454-155">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="40454-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>\_destino de \_ Put \_ OVLY do MCI</span><span class="sxs-lookup"><span data-stu-id="40454-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>MCI\_OVLY\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="40454-157">O retângulo definido para \_ o MCI OVLY \_ Rect especifica a área da janela do cliente usada para exibir uma imagem.</span><span class="sxs-lookup"><span data-stu-id="40454-157">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the client window used to display an image.</span></span> <span data-ttu-id="40454-158">O retângulo contém o deslocamento e a extensão visível da imagem em relação à origem da janela.</span><span class="sxs-lookup"><span data-stu-id="40454-158">The rectangle contains the offset and visible extent of the image relative to the window origin.</span></span> <span data-ttu-id="40454-159">Se o quadro estiver sendo ampliado, a origem será ampliada para o retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="40454-159">If the frame is being stretched, the source is stretched to the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="40454-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>\_quadro de \_ Put \_ OVLY do MCI</span><span class="sxs-lookup"><span data-stu-id="40454-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI\_OVLY\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="40454-161">O retângulo definido para o MCI \_ OVLY \_ Rect especifica a área do buffer de vídeo usado para receber a imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="40454-161">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used to receive the video image.</span></span> <span data-ttu-id="40454-162">O retângulo contém o deslocamento e a extensão da área do buffer em relação à origem do buffer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="40454-162">The rectangle contains the offset and extent of the buffer area relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="40454-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>\_fonte de \_ Put \_ OVLY MCI</span><span class="sxs-lookup"><span data-stu-id="40454-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>MCI\_OVLY\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="40454-164">O retângulo definido para \_ o MCI OVLY \_ Rect especifica a área do buffer de vídeo usada como a origem da imagem digital.</span><span class="sxs-lookup"><span data-stu-id="40454-164">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used as the source of the digital image.</span></span> <span data-ttu-id="40454-165">O retângulo contém o deslocamento e a extensão do retângulo de recorte para o buffer de vídeo em relação à sua origem.</span><span class="sxs-lookup"><span data-stu-id="40454-165">The rectangle contains the offset and extent of the clipping rectangle for the video buffer relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="40454-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>vídeo do MCI \_ OVLY \_ Put \_</span><span class="sxs-lookup"><span data-stu-id="40454-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>MCI\_OVLY\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="40454-167">O retângulo definido para o MCI \_ OVLY \_ Rect especifica a área da captura de fonte de vídeo pelo buffer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="40454-167">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video source capture by the video buffer.</span></span> <span data-ttu-id="40454-168">O retângulo contém o deslocamento e a extensão do retângulo de recorte da fonte de vídeo em relação à sua origem.</span><span class="sxs-lookup"><span data-stu-id="40454-168">The rectangle contains the offset and extent of the clipping rectangle for the video source relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="40454-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect MCI</span><span class="sxs-lookup"><span data-stu-id="40454-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="40454-170">O membro **RC** da estrutura identificada por *lpDest* contém um retângulo de exibição válido.</span><span class="sxs-lookup"><span data-stu-id="40454-170">The **rc** member of the structure identified by *lpDest* contains a valid display rectangle.</span></span> <span data-ttu-id="40454-171">Se esse sinalizador não for especificado, o retângulo padrão corresponderá às coordenadas do buffer de vídeo ou da janela que está sendo recortada.</span><span class="sxs-lookup"><span data-stu-id="40454-171">If this flag is not specified, the default rectangle matches the coordinates of the video buffer or window being clipped.</span></span>

</dd> </dl>

<span data-ttu-id="40454-172">Para dispositivos de sobreposição de vídeo, *lpDest* aponta para uma estrutura [**MCI \_ OVLY \_ Rect \_ parms**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="40454-172">For video-overlay devices, *lpDest* points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="40454-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40454-173">Requirements</span></span>



| <span data-ttu-id="40454-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="40454-174">Requirement</span></span> | <span data-ttu-id="40454-175">Valor</span><span class="sxs-lookup"><span data-stu-id="40454-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40454-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40454-176">Minimum supported client</span></span><br/> | <span data-ttu-id="40454-177">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="40454-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="40454-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40454-178">Minimum supported server</span></span><br/> | <span data-ttu-id="40454-179">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="40454-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="40454-180">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="40454-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="40454-181"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40454-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40454-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="40454-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40454-183">MCI</span><span class="sxs-lookup"><span data-stu-id="40454-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="40454-184">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="40454-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


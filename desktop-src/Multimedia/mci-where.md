---
title: MCI_WHERE comando (mmsystem. h)
description: O MCI \_ em que o comando obtém o retângulo de recorte para o dispositivo de vídeo.
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- Multimídia do Windows de comando MCI_WHERE
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918507"
---
# <a name="mci_where-command"></a><span data-ttu-id="75a53-104">MCI, \_ em que comando</span><span class="sxs-lookup"><span data-stu-id="75a53-104">MCI\_WHERE command</span></span>

<span data-ttu-id="75a53-105">O MCI \_ em que o comando obtém o retângulo de recorte para o dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="75a53-105">The MCI\_WHERE command obtains the clipping rectangle for the video device.</span></span> <span data-ttu-id="75a53-106">Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="75a53-106">Digital-video, and video-overlay devices recognize this command.</span></span> <span data-ttu-id="75a53-107">Os membros **superior** e **esquerdo** do [Rect](/previous-versions//ms536136(v=vs.85)) retornado contêm a origem do retângulo de recorte e os membros **direito** e **inferior** contêm a largura e a altura do retângulo de recorte.</span><span class="sxs-lookup"><span data-stu-id="75a53-107">The **top** and **left** members of the returned [RECT](/previous-versions//ms536136(v=vs.85)) contain the origin of the clipping rectangle, and the **right** and **bottom** members contain the width and height of the clipping rectangle.</span></span> <span data-ttu-id="75a53-108">(Esse não é o uso padrão dos membros **direito** e **inferior** .)</span><span class="sxs-lookup"><span data-stu-id="75a53-108">(This is not the standard use of the **right** and **bottom** members.)</span></span>

<span data-ttu-id="75a53-109">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="75a53-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
);
```



## <a name="parameters"></a><span data-ttu-id="75a53-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75a53-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75a53-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="75a53-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="75a53-112">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="75a53-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="75a53-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="75a53-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="75a53-114">\_Notificação MCI, \_ espera MCI ou, para dispositivos de vídeo digital, teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="75a53-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="75a53-115">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="75a53-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="75a53-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*</span><span class="sxs-lookup"><span data-stu-id="75a53-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*</span></span>
</dt> <dd>

<span data-ttu-id="75a53-117">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="75a53-117">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="75a53-118">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="75a53-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75a53-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="75a53-119">Return Value</span></span>

<span data-ttu-id="75a53-120">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="75a53-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="75a53-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="75a53-121">Remarks</span></span>

<span data-ttu-id="75a53-122">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :</span><span class="sxs-lookup"><span data-stu-id="75a53-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="75a53-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI \_ DGV \_ em que \_ destino</span><span class="sxs-lookup"><span data-stu-id="75a53-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI\_DGV\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="75a53-124">Obtém uma descrição da região retangular usada para exibir vídeo e imagens na área do cliente da janela atual.</span><span class="sxs-lookup"><span data-stu-id="75a53-124">Obtains a description of the rectangular region used to display video and images in the client area of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="75a53-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>DGV MCI, \_ \_ em que \_ frame</span><span class="sxs-lookup"><span data-stu-id="75a53-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI\_DGV\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="75a53-126">Obtém uma descrição da região retangular do buffer de quadro no qual as imagens do retângulo de vídeo são dimensionadas.</span><span class="sxs-lookup"><span data-stu-id="75a53-126">Obtains a description of the rectangular region of the frame buffer into which images from the video rectangle are scaled.</span></span> <span data-ttu-id="75a53-127">As coordenadas de retângulo são colocadas no membro **RC** da estrutura identificada por *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="75a53-127">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="75a53-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI \_ DGV \_ em que \_ Max</span><span class="sxs-lookup"><span data-stu-id="75a53-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI\_DGV\_WHERE\_MAX</span></span>
</dt> <dd>

<span data-ttu-id="75a53-129">Quando usado com o MCI \_ DGV \_ onde \_ o destino ou o MCI \_ DGV \_ em que \_ a origem, o retângulo retornado indica a largura máxima e a altura da região especificada.</span><span class="sxs-lookup"><span data-stu-id="75a53-129">When used with MCI\_DGV\_WHERE\_DESTINATION or MCI\_DGV\_WHERE\_SOURCE, the rectangle returned indicates the maximum width and height of the specified region.</span></span> <span data-ttu-id="75a53-130">Quando usado com o MCI \_ DGV \_ em que \_ Window, o retângulo retornado indica o tamanho da tela inteira.</span><span class="sxs-lookup"><span data-stu-id="75a53-130">When used with MCI\_DGV\_WHERE\_WINDOW, the rectangle returned indicates the size of the entire display.</span></span>

</dd> <dt>

<span data-ttu-id="75a53-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI \_ DGV \_ onde a \_ origem</span><span class="sxs-lookup"><span data-stu-id="75a53-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI\_DGV\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="75a53-132">Obtém uma descrição da região retangular (cortada do buffer de quadro) que é ampliada para se ajustar ao retângulo de destino na exibição.</span><span class="sxs-lookup"><span data-stu-id="75a53-132">Obtains a description of the rectangular region (cropped from the frame buffer) that is stretched to fit the destination rectangle on the display.</span></span>

</dd> <dt>

<span data-ttu-id="75a53-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>\_DGV MCI \_ em que \_ vídeo</span><span class="sxs-lookup"><span data-stu-id="75a53-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI\_DGV\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="75a53-134">Obtém uma descrição da região retangular recortada da fonte da apresentação para preencher o retângulo do quadro no buffer do quadro.</span><span class="sxs-lookup"><span data-stu-id="75a53-134">Obtains a description of the rectangular region cropped from the presentation source to fill the frame rectangle in the frame buffer.</span></span> <span data-ttu-id="75a53-135">As coordenadas de retângulo são colocadas no membro **RC** da estrutura identificada por *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="75a53-135">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="75a53-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>DGV MCI, \_ \_ em que \_ janela</span><span class="sxs-lookup"><span data-stu-id="75a53-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI\_DGV\_WHERE\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="75a53-137">Obtém uma descrição do quadro da janela de exibição.</span><span class="sxs-lookup"><span data-stu-id="75a53-137">Obtains a description of the display-window frame.</span></span>

</dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="75a53-138">Para dispositivos de vídeo digital, o parâmetro *lpQuery* aponta para um **\_ DGV MCI \_ em \_ que** a estrutura de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="75a53-138">For digital-video devices, the *lpQuery* parameter points to an **MCI\_DGV\_WHERE\_PARMS** structure.</span></span> <span data-ttu-id="75a53-139">O **DGV MCI em que a estrutura de \_ \_ \_ parms** é idêntica à estrutura de [**parâmetros do MCI \_ DGV \_ Rect \_**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="75a53-139">The **MCI\_DGV\_WHERE\_PARMS** structure is identical to the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="75a53-140">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo de **sobreposição** :</span><span class="sxs-lookup"><span data-stu-id="75a53-140">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="75a53-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI \_ OVLY \_ em que \_ destino</span><span class="sxs-lookup"><span data-stu-id="75a53-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI\_OVLY\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="75a53-142">Obtém o retângulo de exibição de destino.</span><span class="sxs-lookup"><span data-stu-id="75a53-142">Obtains the destination display rectangle.</span></span> <span data-ttu-id="75a53-143">As coordenadas de retângulo são colocadas no membro **RC** da estrutura identificada por *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="75a53-143">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="75a53-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>OVLY MCI, \_ \_ em que \_ frame</span><span class="sxs-lookup"><span data-stu-id="75a53-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI\_OVLY\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="75a53-145">Obtém o retângulo de quadro sobreposto.</span><span class="sxs-lookup"><span data-stu-id="75a53-145">Obtains the overlay frame rectangle.</span></span> <span data-ttu-id="75a53-146">As coordenadas de retângulo são colocadas no membro **RC** da estrutura identificada por *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="75a53-146">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="75a53-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI \_ OVLY \_ onde a \_ origem</span><span class="sxs-lookup"><span data-stu-id="75a53-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI\_OVLY\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="75a53-148">Obtém o retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="75a53-148">Obtains the source rectangle.</span></span> <span data-ttu-id="75a53-149">As coordenadas de retângulo são colocadas no membro **RC** da estrutura identificada por *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="75a53-149">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="75a53-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>\_OVLY MCI \_ em que \_ vídeo</span><span class="sxs-lookup"><span data-stu-id="75a53-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI\_OVLY\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="75a53-151">Obtém o retângulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="75a53-151">Obtains the video rectangle.</span></span> <span data-ttu-id="75a53-152">As coordenadas de retângulo são colocadas no membro **RC** da estrutura identificada por *lpQuery*.</span><span class="sxs-lookup"><span data-stu-id="75a53-152">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> </dl>

<span data-ttu-id="75a53-153">Para dispositivos de sobreposição de vídeo, o parâmetro *lpQuery* aponta para uma estrutura de [**parâmetros MCI do \_ OVLY \_ Rect \_**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="75a53-153">For video-overlay devices, the *lpQuery* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="75a53-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75a53-154">Requirements</span></span>



| <span data-ttu-id="75a53-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="75a53-155">Requirement</span></span> | <span data-ttu-id="75a53-156">Valor</span><span class="sxs-lookup"><span data-stu-id="75a53-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75a53-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75a53-157">Minimum supported client</span></span><br/> | <span data-ttu-id="75a53-158">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="75a53-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="75a53-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75a53-159">Minimum supported server</span></span><br/> | <span data-ttu-id="75a53-160">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="75a53-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="75a53-161">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="75a53-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="75a53-162"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75a53-162"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75a53-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="75a53-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75a53-164">MCI</span><span class="sxs-lookup"><span data-stu-id="75a53-164">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="75a53-165">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="75a53-165">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


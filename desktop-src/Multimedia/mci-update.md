---
title: MCI_UPDATE comando (mmsystem. h)
description: O comando de atualização do MCI \_ atualiza o retângulo de exibição. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- Multimídia do Windows de comando MCI_UPDATE
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423186096c88a8f1ff74987ff57c6b49dc6c3131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086299"
---
# <a name="mci_update-command"></a><span data-ttu-id="4958d-105">Comando de atualização do MCI \_</span><span class="sxs-lookup"><span data-stu-id="4958d-105">MCI\_UPDATE command</span></span>

<span data-ttu-id="4958d-106">O comando de atualização do MCI \_ atualiza o retângulo de exibição.</span><span class="sxs-lookup"><span data-stu-id="4958d-106">The MCI\_UPDATE command updates the display rectangle.</span></span> <span data-ttu-id="4958d-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="4958d-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="4958d-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="4958d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="4958d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4958d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4958d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="4958d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4958d-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="4958d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="4958d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="4958d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4958d-113">**MCI \_ NOTIFICAr**, **\_ espera de MCI** ou, para dispositivos de vídeo digital **, \_ teste MCI**.</span><span class="sxs-lookup"><span data-stu-id="4958d-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="4958d-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4958d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="4958d-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span><span class="sxs-lookup"><span data-stu-id="4958d-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="4958d-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="4958d-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="4958d-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="4958d-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4958d-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="4958d-118">Return Value</span></span>

<span data-ttu-id="4958d-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="4958d-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4958d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4958d-120">Remarks</span></span>

<span data-ttu-id="4958d-121">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo "DigitalVideo":</span><span class="sxs-lookup"><span data-stu-id="4958d-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="4958d-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>DGV de atualização do MCI ( \_ \_ \_ HDC)</span><span class="sxs-lookup"><span data-stu-id="4958d-122"><span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>MCI\_DGV\_UPDATE\_HDC</span></span>
</dt> <dd>

<span data-ttu-id="4958d-123">O membro **HDC** da estrutura identificada por *lpDest* contém uma janela válida do DC a ser pintada.</span><span class="sxs-lookup"><span data-stu-id="4958d-123">The **hDC** member of the structure identified by *lpDest* contains a valid window of the DC to paint.</span></span> <span data-ttu-id="4958d-124">Esse sinalizador é necessário.</span><span class="sxs-lookup"><span data-stu-id="4958d-124">This flag is required.</span></span>

</dd> <dt>

<span data-ttu-id="4958d-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect MCI</span><span class="sxs-lookup"><span data-stu-id="4958d-125"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="4958d-126">O membro **RC** da estrutura identificada por *lpUnfreeze* contém um retângulo de exibição válido.</span><span class="sxs-lookup"><span data-stu-id="4958d-126">The **rc** member of the structure identified by *lpUnfreeze* contains a valid display rectangle.</span></span> <span data-ttu-id="4958d-127">O retângulo especifica o retângulo de recorte relativo ao retângulo do cliente.</span><span class="sxs-lookup"><span data-stu-id="4958d-127">The rectangle specifies the clipping rectangle relative to the client rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="4958d-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>pintura de atualização do MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="4958d-128"><span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>MCI\_DGV\_UPDATE\_PAINT</span></span>
</dt> <dd>

<span data-ttu-id="4958d-129">Um aplicativo usa esse sinalizador quando recebe uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) que é destinada a um controlador de domínio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4958d-129">An application uses this flag when it receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message that is intended for a display DC.</span></span> <span data-ttu-id="4958d-130">Um dispositivo de buffer de quadro geralmente pinta a cor da chave.</span><span class="sxs-lookup"><span data-stu-id="4958d-130">A frame-buffer device usually paints the key color.</span></span> <span data-ttu-id="4958d-131">Se o dispositivo de vídeo não tiver um buffer de quadros, ele poderá ignorar o \_ comando de atualização do MCI quando o sinalizador de **pintura de atualização do MCI \_ \_ \_ DGV** for usado porque a exibição será repintada durante a operação de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4958d-131">If the display device does not have a frame buffer, it might ignore the MCI\_UPDATE command when the **MCI\_DGV\_UPDATE\_PAINT** flag is used because the display will be repainted during the playback operation.</span></span>

</dd> </dl>

<span data-ttu-id="4958d-132">Para dispositivos de vídeo digital, o parâmetro *lpDest* aponta para uma estrutura de parâmetros de [**atualização de \_ DGV \_ \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) .</span><span class="sxs-lookup"><span data-stu-id="4958d-132">For digital-video devices, the *lpDest* parameter points to an [**MCI\_DGV\_UPDATE\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4958d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4958d-133">Requirements</span></span>



| <span data-ttu-id="4958d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4958d-134">Requirement</span></span> | <span data-ttu-id="4958d-135">Valor</span><span class="sxs-lookup"><span data-stu-id="4958d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4958d-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4958d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4958d-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4958d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4958d-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4958d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4958d-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4958d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4958d-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4958d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4958d-141"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4958d-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4958d-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="4958d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4958d-143">MCI</span><span class="sxs-lookup"><span data-stu-id="4958d-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4958d-144">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="4958d-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


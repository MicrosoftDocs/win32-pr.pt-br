---
title: MCI_SIGNAL comando (mmsystem. h)
description: O \_ comando de sinal MCI define uma posição especificada no espaço de trabalho. Dispositivos de vídeo digital reconhecem este comando. O MCIAVI dá suporte a apenas um sinal ativo por vez.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- Multimídia do Windows de comando MCI_SIGNAL
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369525"
---
# <a name="mci_signal-command"></a><span data-ttu-id="2183d-106">\_Comando de sinal MCI</span><span class="sxs-lookup"><span data-stu-id="2183d-106">MCI\_SIGNAL command</span></span>

<span data-ttu-id="2183d-107">O \_ comando de sinal MCI define uma posição especificada no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2183d-107">The MCI\_SIGNAL command sets a specified position in the workspace.</span></span> <span data-ttu-id="2183d-108">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="2183d-108">Digital-video devices recognize this command.</span></span> <span data-ttu-id="2183d-109">O MCIAVI dá suporte a apenas um sinal ativo por vez.</span><span class="sxs-lookup"><span data-stu-id="2183d-109">MCIAVI supports only one active signal at a time.</span></span>

<span data-ttu-id="2183d-110">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="2183d-110">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
);
```



## <a name="parameters"></a><span data-ttu-id="2183d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2183d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2183d-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="2183d-112"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="2183d-113">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="2183d-113">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="2183d-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="2183d-114"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="2183d-115">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="2183d-115">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="2183d-116">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="2183d-116">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="2183d-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*</span><span class="sxs-lookup"><span data-stu-id="2183d-117"><span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*</span></span>
</dt> <dd>

<span data-ttu-id="2183d-118">Ponteiro para uma estrutura de [**\_ parâmetros de \_ sinal \_ de DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) .</span><span class="sxs-lookup"><span data-stu-id="2183d-118">Pointer to an [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2183d-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2183d-119">Return Value</span></span>

<span data-ttu-id="2183d-120">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="2183d-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2183d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2183d-121">Remarks</span></span>

<span data-ttu-id="2183d-122">A janela cujo identificador você especificar no membro **dwCallback** da estrutura de [**\_ parâmetros do \_ sinal \_ DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) recebe a mensagem mm \_ MCISIGNAL.</span><span class="sxs-lookup"><span data-stu-id="2183d-122">The window whose handle you specify in the **dwCallback** member of the [**MCI\_DGV\_SIGNAL\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) structure receives the MM\_MCISIGNAL message.</span></span>

<span data-ttu-id="2183d-123">Os seguintes sinalizadores se aplicam a dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="2183d-123">The following flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="2183d-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>\_ \_ sinal de DGV MCI \_ em</span><span class="sxs-lookup"><span data-stu-id="2183d-124"><span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>MCI\_DGV\_SIGNAL\_AT</span></span>
</dt> <dd>

<span data-ttu-id="2183d-125">Uma posição de sinal é incluída no membro **dwPosition** da estrutura identificada por *lpSignal*.</span><span class="sxs-lookup"><span data-stu-id="2183d-125">A signal position is included in the **dwPosition** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="2183d-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>cancelamento de sinal MCI \_ DGV \_ \_</span><span class="sxs-lookup"><span data-stu-id="2183d-126"><span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>MCI\_DGV\_SIGNAL\_CANCEL</span></span>
</dt> <dd>

<span data-ttu-id="2183d-127">Remove a posição do sinal especificada pelo valor associado ao \_ USERVAL do \_ sinal MCI DGV \_ .</span><span class="sxs-lookup"><span data-stu-id="2183d-127">Removes the signal position specified by the value associated with MCI\_DGV\_SIGNAL\_USERVAL.</span></span>

</dd> <dt>

<span data-ttu-id="2183d-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>\_sinal MCI DGV a \_ \_ cada</span><span class="sxs-lookup"><span data-stu-id="2183d-128"><span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>MCI\_DGV\_SIGNAL\_EVERY</span></span>
</dt> <dd>

<span data-ttu-id="2183d-129">Um valor de período de sinal é incluído no membro **dwPeriod** da estrutura identificada por *lpSignal*.</span><span class="sxs-lookup"><span data-stu-id="2183d-129">A signal-period value is included in the **dwPeriod** member of the structure identified by *lpSignal*.</span></span>

</dd> <dt>

<span data-ttu-id="2183d-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>\_posição do \_ sinal MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="2183d-130"><span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>MCI\_DGV\_SIGNAL\_POSITION</span></span>
</dt> <dd>

<span data-ttu-id="2183d-131">O dispositivo enviará o valor da posição com a mensagem do Windows em vez do valor especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2183d-131">The device will send the position value with the Windows message instead of the user-specified value.</span></span>

</dd> <dt>

<span data-ttu-id="2183d-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>\_USERVAL do \_ sinal MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="2183d-132"><span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>MCI\_DGV\_SIGNAL\_USERVAL</span></span>
</dt> <dd>

<span data-ttu-id="2183d-133">Um valor de dados é incluído no membro **dwUserParm** da estrutura identificada por *lpSignal*.</span><span class="sxs-lookup"><span data-stu-id="2183d-133">A data value is included in the **dwUserParm** member of the structure identified by *lpSignal*.</span></span> <span data-ttu-id="2183d-134">O valor de dados associado a essa solicitação é relatado de volta com a mensagem do Windows.</span><span class="sxs-lookup"><span data-stu-id="2183d-134">The data value associated with this request is reported back with the Windows message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2183d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2183d-135">Requirements</span></span>



| <span data-ttu-id="2183d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="2183d-136">Requirement</span></span> | <span data-ttu-id="2183d-137">Valor</span><span class="sxs-lookup"><span data-stu-id="2183d-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2183d-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2183d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2183d-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2183d-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2183d-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2183d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2183d-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2183d-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2183d-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2183d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="2183d-143"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2183d-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2183d-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="2183d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2183d-145">MCI</span><span class="sxs-lookup"><span data-stu-id="2183d-145">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2183d-146">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="2183d-146">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


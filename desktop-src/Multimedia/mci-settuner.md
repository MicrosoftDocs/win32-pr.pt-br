---
title: MCI_SETTUNER comando (mmsystem. h)
description: O \_ comando de SETAJUSTE MCI define o canal atual no sintonizador. Os dispositivos VCR reconhecem este comando.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- Multimídia do Windows de comando MCI_SETTUNER
topic_type:
- apiref
api_name:
- MCI_SETTUNER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5774a927e1f41cf5d3bf42d6e93e532e0c2961a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009745"
---
# <a name="mci_settuner-command"></a><span data-ttu-id="f8269-105">Comando do MCI \_ SETajuster</span><span class="sxs-lookup"><span data-stu-id="f8269-105">MCI\_SETTUNER command</span></span>

<span data-ttu-id="f8269-106">O \_ comando de SETAJUSTE MCI define o canal atual no sintonizador.</span><span class="sxs-lookup"><span data-stu-id="f8269-106">The MCI\_SETTUNER command sets the current channel on the tuner.</span></span> <span data-ttu-id="f8269-107">Os dispositivos VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="f8269-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="f8269-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="f8269-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTUNER, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTuner
);
```



## <a name="parameters"></a><span data-ttu-id="f8269-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8269-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8269-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f8269-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f8269-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="f8269-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f8269-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f8269-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f8269-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="f8269-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="f8269-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f8269-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8269-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*</span><span class="sxs-lookup"><span data-stu-id="f8269-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*</span></span>
</dt> <dd>

<span data-ttu-id="f8269-116">Ponteiro para uma estrutura de [**\_ \_ \_ parâmetros de setajuster de videocassete MCI**](mci-vcr-settuner-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f8269-116">Pointer to an [**MCI\_VCR\_SETTUNER\_PARMS**](mci-vcr-settuner-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8269-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f8269-117">Return Value</span></span>

<span data-ttu-id="f8269-118">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f8269-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8269-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8269-119">Remarks</span></span>

<span data-ttu-id="f8269-120">Os seguintes sinalizadores adicionais se aplicam a dispositivos VCR:</span><span class="sxs-lookup"><span data-stu-id="f8269-120">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="f8269-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>\_canal do \_ setajuster \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="f8269-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>MCI\_VCR\_SETTUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="f8269-122">O membro **dwChannel** da estrutura identificada por *lpSetTuner* contém o novo número de canal.</span><span class="sxs-lookup"><span data-stu-id="f8269-122">The **dwChannel** member of the structure identified by *lpSetTuner* contains the new channel number.</span></span>

</dd> <dt>

<span data-ttu-id="f8269-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>\_canal do \_ setajuster VCR MCI \_ \_ inoperante</span><span class="sxs-lookup"><span data-stu-id="f8269-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="f8269-124">Decrementa o canal do sintonizador.</span><span class="sxs-lookup"><span data-stu-id="f8269-124">Decrements the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="f8269-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>\_ \_ \_ \_ busca inativa do canal do MCI VCR setajuster \_</span><span class="sxs-lookup"><span data-stu-id="f8269-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="f8269-126">Procura um canal válido na direção inversa.</span><span class="sxs-lookup"><span data-stu-id="f8269-126">Searches for a valid channel in the reverse direction.</span></span>

</dd> <dt>

<span data-ttu-id="f8269-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>\_ \_ \_ \_ busca ativa do canal \_ de videocassete do MCI</span><span class="sxs-lookup"><span data-stu-id="f8269-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_UP</span></span>
</dt> <dd>

<span data-ttu-id="f8269-128">Procura um canal válido na direção de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="f8269-128">Searches for a valid channel in the forward direction.</span></span>

</dd> <dt>

<span data-ttu-id="f8269-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>\_canal do \_ setajuster \_ VCR \_ MCI</span><span class="sxs-lookup"><span data-stu-id="f8269-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_UP</span></span>
</dt> <dd>

<span data-ttu-id="f8269-130">Incrementa o canal do sintonizador.</span><span class="sxs-lookup"><span data-stu-id="f8269-130">Increments the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="f8269-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>\_número do \_ sintonizador de \_ VCR MCI</span><span class="sxs-lookup"><span data-stu-id="f8269-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>MCI\_VCR\_SETTUNER\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="f8269-132">O membro **dwNumber** da estrutura identificada por *lpSetTuner* especifica qual sintonizador lógico deve afetar com esse comando.</span><span class="sxs-lookup"><span data-stu-id="f8269-132">The **dwNumber** member of the structure identified by *lpSetTuner* specifies which logical tuner to affect with this command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8269-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8269-133">Requirements</span></span>



| <span data-ttu-id="f8269-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8269-134">Requirement</span></span> | <span data-ttu-id="f8269-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f8269-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8269-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8269-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f8269-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f8269-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8269-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8269-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f8269-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f8269-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8269-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f8269-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8269-141"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8269-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8269-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8269-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8269-143">MCI</span><span class="sxs-lookup"><span data-stu-id="f8269-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f8269-144">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="f8269-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


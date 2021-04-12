---
title: MCI_SPIN comando (mmsystem. h)
description: O comando de rotação do MCI \_ inicia o dispositivo girando ou reduzindo. Os dispositivos VIDEODISC reconhecem este comando.
ms.assetid: 9e491455-d06d-44c6-8aca-6360384ec266
keywords:
- Multimídia do Windows de comando MCI_SPIN
topic_type:
- apiref
api_name:
- MCI_SPIN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0b154d9a2f54248ac6174e71a24d4afe74918d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369524"
---
# <a name="mci_spin-command"></a><span data-ttu-id="f0a6f-105">Comando de rotação do MCI \_</span><span class="sxs-lookup"><span data-stu-id="f0a6f-105">MCI\_SPIN command</span></span>

<span data-ttu-id="f0a6f-106">O comando de rotação do MCI \_ inicia o dispositivo girando ou reduzindo.</span><span class="sxs-lookup"><span data-stu-id="f0a6f-106">The MCI\_SPIN command starts the device spinning up or down.</span></span> <span data-ttu-id="f0a6f-107">Os dispositivos VIDEODISC reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="f0a6f-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="f0a6f-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="f0a6f-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SPIN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSpin
);
```



## <a name="parameters"></a><span data-ttu-id="f0a6f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0a6f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0a6f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="f0a6f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="f0a6f-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="f0a6f-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="f0a6f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f0a6f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="f0a6f-113">\_Notificação MCI ou \_ espera MCI.</span><span class="sxs-lookup"><span data-stu-id="f0a6f-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="f0a6f-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f0a6f-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0a6f-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*</span><span class="sxs-lookup"><span data-stu-id="f0a6f-115"><span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*</span></span>
</dt> <dd>

<span data-ttu-id="f0a6f-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a6f-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="f0a6f-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="f0a6f-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0a6f-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f0a6f-118">Return Value</span></span>

<span data-ttu-id="f0a6f-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f0a6f-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0a6f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0a6f-120">Remarks</span></span>

<span data-ttu-id="f0a6f-121">Os seguintes sinalizadores adicionais se aplicam a dispositivos VIDEODISC:</span><span class="sxs-lookup"><span data-stu-id="f0a6f-121">The following additional flags apply to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="f0a6f-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>\_rotação de VD MCI \_ \_ para baixo</span><span class="sxs-lookup"><span data-stu-id="f0a6f-122"><span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>MCI\_VD\_SPIN\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="f0a6f-123">Interrompe o disco girando.</span><span class="sxs-lookup"><span data-stu-id="f0a6f-123">Stops the disc spinning.</span></span>

</dd> <dt>

<span data-ttu-id="f0a6f-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>\_ \_ rotação de VD \_ do MCI</span><span class="sxs-lookup"><span data-stu-id="f0a6f-124"><span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>MCI\_VD\_SPIN\_UP</span></span>
</dt> <dd>

<span data-ttu-id="f0a6f-125">Inicia o disco girando.</span><span class="sxs-lookup"><span data-stu-id="f0a6f-125">Starts the disc spinning.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0a6f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0a6f-126">Requirements</span></span>



| <span data-ttu-id="f0a6f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0a6f-127">Requirement</span></span> | <span data-ttu-id="f0a6f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f0a6f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a6f-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0a6f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a6f-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f0a6f-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f0a6f-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0a6f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a6f-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f0a6f-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f0a6f-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f0a6f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0a6f-134"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0a6f-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0a6f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0a6f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a6f-136">MCI</span><span class="sxs-lookup"><span data-stu-id="f0a6f-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f0a6f-137">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="f0a6f-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


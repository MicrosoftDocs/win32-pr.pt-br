---
title: MCI_SETTIMECODE comando (mmsystem. h)
description: O \_ comando MCI SetCode habilita ou desabilita a gravação do código de paficação de um videocassete. Os dispositivos VCR reconhecem este comando.
ms.assetid: b014fbe0-de97-4540-a5fe-b22d157361f7
keywords:
- Multimídia do Windows de comando MCI_SETTIMECODE
topic_type:
- apiref
api_name:
- MCI_SETTIMECODE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df0727f4386bad46b3fde7f2d816ce951850b8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759365"
---
# <a name="mci_settimecode-command"></a><span data-ttu-id="71aab-105">Comando do MCI \_ SETcode</span><span class="sxs-lookup"><span data-stu-id="71aab-105">MCI\_SETTIMECODE command</span></span>

<span data-ttu-id="71aab-106">O \_ comando MCI SetCode habilita ou desabilita a gravação do código de paficação de um videocassete.</span><span class="sxs-lookup"><span data-stu-id="71aab-106">The MCI\_SETTIMECODE command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="71aab-107">Os dispositivos VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="71aab-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="71aab-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="71aab-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTIMECODE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTimeCode
);
```



## <a name="parameters"></a><span data-ttu-id="71aab-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71aab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71aab-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="71aab-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="71aab-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="71aab-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="71aab-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="71aab-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="71aab-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="71aab-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="71aab-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="71aab-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="71aab-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*</span><span class="sxs-lookup"><span data-stu-id="71aab-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="71aab-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="71aab-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="71aab-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="71aab-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71aab-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="71aab-118">Return Value</span></span>

<span data-ttu-id="71aab-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="71aab-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="71aab-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="71aab-120">Remarks</span></span>

<span data-ttu-id="71aab-121">O seguinte sinalizador adicional se aplica a dispositivos VCR:</span><span class="sxs-lookup"><span data-stu-id="71aab-121">The following additional flag applies to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="71aab-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>\_registro SETcode-of-código de VCR MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="71aab-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>MCI\_VCR\_SETTIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="71aab-123">Define a gravação de controle de código de Code como on ou off.</span><span class="sxs-lookup"><span data-stu-id="71aab-123">Sets the timecode track recording to on or off.</span></span> <span data-ttu-id="71aab-124">Esse sinalizador é usado em combinação com um dos seguintes sinalizadores adicionais:</span><span class="sxs-lookup"><span data-stu-id="71aab-124">This flag is used in combination with one of the following additional flags:</span></span>

</dd> <dt>

<span data-ttu-id="71aab-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em</span><span class="sxs-lookup"><span data-stu-id="71aab-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="71aab-126">Gravação de código de ponto em.</span><span class="sxs-lookup"><span data-stu-id="71aab-126">Timecode recording on.</span></span>

</dd> <dt>

<span data-ttu-id="71aab-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado</span><span class="sxs-lookup"><span data-stu-id="71aab-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="71aab-128">Gravação de código de ponto desativada.</span><span class="sxs-lookup"><span data-stu-id="71aab-128">Timecode recording off.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71aab-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71aab-129">Requirements</span></span>



| <span data-ttu-id="71aab-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="71aab-130">Requirement</span></span> | <span data-ttu-id="71aab-131">Valor</span><span class="sxs-lookup"><span data-stu-id="71aab-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71aab-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71aab-132">Minimum supported client</span></span><br/> | <span data-ttu-id="71aab-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="71aab-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="71aab-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71aab-134">Minimum supported server</span></span><br/> | <span data-ttu-id="71aab-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="71aab-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="71aab-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="71aab-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="71aab-137"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71aab-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71aab-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="71aab-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71aab-139">MCI</span><span class="sxs-lookup"><span data-stu-id="71aab-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="71aab-140">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="71aab-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


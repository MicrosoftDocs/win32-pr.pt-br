---
title: MCI_INDEX comando (mmsystem. h)
description: O \_ comando de índice MCI ativa ou desativa a exibição na tela. Os dispositivos VCR reconhecem este comando.
ms.assetid: c0f18f28-3578-4648-9b75-2d3ede68b3df
keywords:
- Multimídia do Windows de comando MCI_INDEX
topic_type:
- apiref
api_name:
- MCI_INDEX
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e93890b8c3db1150bc7224b0fd8b6ee7475ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086397"
---
# <a name="mci_index-command"></a><span data-ttu-id="ff216-105">\_Comando de índice MCI</span><span class="sxs-lookup"><span data-stu-id="ff216-105">MCI\_INDEX command</span></span>

<span data-ttu-id="ff216-106">O \_ comando de índice MCI ativa ou desativa a exibição na tela.</span><span class="sxs-lookup"><span data-stu-id="ff216-106">The MCI\_INDEX command turns the on-screen display on or off.</span></span> <span data-ttu-id="ff216-107">Os dispositivos VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="ff216-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="ff216-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff216-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INDEX, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpIndex
);
```



## <a name="parameters"></a><span data-ttu-id="ff216-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff216-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff216-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="ff216-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ff216-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="ff216-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ff216-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ff216-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ff216-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="ff216-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="ff216-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ff216-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff216-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*</span><span class="sxs-lookup"><span data-stu-id="ff216-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*</span></span>
</dt> <dd>

<span data-ttu-id="ff216-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="ff216-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="ff216-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="ff216-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff216-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ff216-118">Return Value</span></span>

<span data-ttu-id="ff216-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="ff216-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff216-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff216-120">Remarks</span></span>

<span data-ttu-id="ff216-121">As informações apresentadas na exibição na tela são controladas pelo \_ sinalizador de índice do conjunto de VCR MCI \_ \_ no [comando \_ set do MCI](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="ff216-121">The information presented in the on-screen display is controlled by the MCI\_VCR\_SET\_INDEX flag in the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="ff216-122">Os seguintes sinalizadores adicionais se aplicam a dispositivos VCR:</span><span class="sxs-lookup"><span data-stu-id="ff216-122">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="ff216-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado</span><span class="sxs-lookup"><span data-stu-id="ff216-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="ff216-124">Ativa a exibição da tela.</span><span class="sxs-lookup"><span data-stu-id="ff216-124">Turns on-screen display off.</span></span>

</dd> <dt>

<span data-ttu-id="ff216-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em</span><span class="sxs-lookup"><span data-stu-id="ff216-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="ff216-126">Ativa a exibição na tela no.</span><span class="sxs-lookup"><span data-stu-id="ff216-126">Turns on-screen display on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff216-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff216-127">Requirements</span></span>



| <span data-ttu-id="ff216-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff216-128">Requirement</span></span> | <span data-ttu-id="ff216-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ff216-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff216-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff216-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ff216-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ff216-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ff216-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff216-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ff216-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ff216-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ff216-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ff216-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff216-135"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff216-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff216-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff216-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff216-137">MCI</span><span class="sxs-lookup"><span data-stu-id="ff216-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ff216-138">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="ff216-138">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


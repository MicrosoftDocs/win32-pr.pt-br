---
title: MCI_UNDO comando (mmsystem. h)
description: O \_ comando MCI desfazer reverte o \_ comando de colar, cópia MCI, exclusão de MCI ou de colagem MCI bem-sucedido mais recente \_ \_ \_ . Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 1593457a-e680-4732-a89e-00f4eff7605a
keywords:
- Multimídia do Windows de comando MCI_UNDO
topic_type:
- apiref
api_name:
- MCI_UNDO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d099d95159afee8d91acb77eb64e8e80bee5425d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008981"
---
# <a name="mci_undo-command"></a><span data-ttu-id="8498f-105">\_Comando de desfazer MCI</span><span class="sxs-lookup"><span data-stu-id="8498f-105">MCI\_UNDO command</span></span>

<span data-ttu-id="8498f-106">O \_ comando MCI desfazer reverte o comando de colar, [ \_ cópia MCI](mci-copy.md), [ \_ exclusão](mci-delete.md)de MCI ou de [ \_ colagem](mci-paste.md) MCI bem-sucedido mais recente. [ \_ ](mci-cut.md)</span><span class="sxs-lookup"><span data-stu-id="8498f-106">The MCI\_UNDO command reverses the most recent successful [MCI\_CUT](mci-cut.md), [MCI\_COPY](mci-copy.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="8498f-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="8498f-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="8498f-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="8498f-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNDO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUndo
);
```



## <a name="parameters"></a><span data-ttu-id="8498f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8498f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8498f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="8498f-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="8498f-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="8498f-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="8498f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8498f-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="8498f-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="8498f-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="8498f-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="8498f-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="8498f-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpUndo*</span><span class="sxs-lookup"><span data-stu-id="8498f-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpUndo*</span></span>
</dt> <dd>

<span data-ttu-id="8498f-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="8498f-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="8498f-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="8498f-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8498f-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8498f-118">Return Value</span></span>

<span data-ttu-id="8498f-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="8498f-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8498f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8498f-120">Requirements</span></span>



| <span data-ttu-id="8498f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8498f-121">Requirement</span></span> | <span data-ttu-id="8498f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8498f-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8498f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8498f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8498f-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8498f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8498f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8498f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8498f-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8498f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8498f-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8498f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8498f-128"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8498f-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8498f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8498f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8498f-130">MCI</span><span class="sxs-lookup"><span data-stu-id="8498f-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8498f-131">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="8498f-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


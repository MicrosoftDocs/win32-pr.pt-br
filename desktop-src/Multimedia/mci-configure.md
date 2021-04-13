---
title: MCI_CONFIGURE comando (mmsystem. h)
description: O \_ comando configurar MCI exibe uma caixa de diálogo para definir as opções operacionais. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 92683579-e6af-42a7-8a0f-6b88b04441f2
keywords:
- Multimídia do Windows de comando MCI_CONFIGURE
topic_type:
- apiref
api_name:
- MCI_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f752f17ac0d0a5c04edf628edfb6c04a339783f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369278"
---
# <a name="mci_configure-command"></a><span data-ttu-id="c05eb-105">Comando de configuração do MCI \_</span><span class="sxs-lookup"><span data-stu-id="c05eb-105">MCI\_CONFIGURE command</span></span>

<span data-ttu-id="c05eb-106">O \_ comando configurar MCI exibe uma caixa de diálogo para definir as opções operacionais.</span><span class="sxs-lookup"><span data-stu-id="c05eb-106">The MCI\_CONFIGURE command displays a dialog box for setting the operating options.</span></span> <span data-ttu-id="c05eb-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="c05eb-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="c05eb-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="c05eb-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CONFIGURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpConfigure
);
```



## <a name="parameters"></a><span data-ttu-id="c05eb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c05eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c05eb-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="c05eb-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="c05eb-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="c05eb-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="c05eb-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="c05eb-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c05eb-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="c05eb-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="c05eb-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c05eb-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c05eb-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpConfigure*</span><span class="sxs-lookup"><span data-stu-id="c05eb-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpConfigure*</span></span>
</dt> <dd>

<span data-ttu-id="c05eb-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="c05eb-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="c05eb-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="c05eb-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c05eb-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c05eb-118">Return Value</span></span>

<span data-ttu-id="c05eb-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="c05eb-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c05eb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c05eb-120">Requirements</span></span>



| <span data-ttu-id="c05eb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c05eb-121">Requirement</span></span> | <span data-ttu-id="c05eb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c05eb-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c05eb-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c05eb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c05eb-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c05eb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c05eb-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c05eb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c05eb-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c05eb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c05eb-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c05eb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c05eb-128"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c05eb-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c05eb-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c05eb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c05eb-130">MCI</span><span class="sxs-lookup"><span data-stu-id="c05eb-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c05eb-131">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="c05eb-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


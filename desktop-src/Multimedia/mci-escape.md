---
title: MCI_ESCAPE comando (mmsystem. h)
description: O \_ comando de escape MCI envia uma cadeia de caracteres diretamente para o dispositivo. Os dispositivos VIDEODISC reconhecem este comando.
ms.assetid: 56ebc717-f0f7-4612-8e51-57b13ff9d42b
keywords:
- Multimídia do Windows de comando MCI_ESCAPE
topic_type:
- apiref
api_name:
- MCI_ESCAPE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4bcd55590cb1b2cab5482eeb921118531002c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760819"
---
# <a name="mci_escape-command"></a><span data-ttu-id="370f6-105">\_Comando de escape MCI</span><span class="sxs-lookup"><span data-stu-id="370f6-105">MCI\_ESCAPE command</span></span>

<span data-ttu-id="370f6-106">O \_ comando de escape MCI envia uma cadeia de caracteres diretamente para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="370f6-106">The MCI\_ESCAPE command sends a string directly to the device.</span></span> <span data-ttu-id="370f6-107">Os dispositivos VIDEODISC reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="370f6-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="370f6-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="370f6-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_ESCAPE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_VD_ESCAPE_PARMS) lpEscape
);
```



## <a name="parameters"></a><span data-ttu-id="370f6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="370f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="370f6-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="370f6-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="370f6-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="370f6-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="370f6-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="370f6-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="370f6-113">\_Notificação MCI ou \_ espera MCI.</span><span class="sxs-lookup"><span data-stu-id="370f6-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="370f6-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="370f6-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="370f6-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*</span><span class="sxs-lookup"><span data-stu-id="370f6-115"><span id="lpEscape"></span><span id="lpescape"></span><span id="LPESCAPE"></span>*lpEscape*</span></span>
</dt> <dd>

<span data-ttu-id="370f6-116">Ponteiro para uma estrutura de [**parâmetros de escape de VD do MCI \_ \_ \_**](mci-vd-escape-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="370f6-116">Pointer to an [**MCI\_VD\_ESCAPE\_PARMS**](mci-vd-escape-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="370f6-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="370f6-117">Return Value</span></span>

<span data-ttu-id="370f6-118">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="370f6-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="370f6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="370f6-119">Remarks</span></span>

<span data-ttu-id="370f6-120">Os dados enviados com o \_ escape MCI são dependentes do dispositivo e geralmente são passados diretamente para o hardware associado ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="370f6-120">The data sent with MCI\_ESCAPE is device-dependent and is usually passed directly to the hardware associated with the device.</span></span>

<span data-ttu-id="370f6-121">O sinalizador adicional a seguir se aplica a dispositivos VIDEODISC:</span><span class="sxs-lookup"><span data-stu-id="370f6-121">The following additional flag applies to videodisc devices:</span></span>

<dl> <dt>

<span data-ttu-id="370f6-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>\_cadeia de \_ caracteres de escape de VD MCI \_</span><span class="sxs-lookup"><span data-stu-id="370f6-122"><span id="MCI_VD_ESCAPE_STRING"></span><span id="mci_vd_escape_string"></span>MCI\_VD\_ESCAPE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="370f6-123">Uma cadeia de caracteres de comando é especificada no membro **lpstrCommand** da estrutura identificada por *lpEscape*.</span><span class="sxs-lookup"><span data-stu-id="370f6-123">A command string is specified in the **lpstrCommand** member of the structure identified by *lpEscape*.</span></span> <span data-ttu-id="370f6-124">Esse sinalizador é necessário.</span><span class="sxs-lookup"><span data-stu-id="370f6-124">This flag is required.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="370f6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="370f6-125">Requirements</span></span>



| <span data-ttu-id="370f6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="370f6-126">Requirement</span></span> | <span data-ttu-id="370f6-127">Valor</span><span class="sxs-lookup"><span data-stu-id="370f6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="370f6-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="370f6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="370f6-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="370f6-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="370f6-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="370f6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="370f6-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="370f6-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="370f6-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="370f6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="370f6-133"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="370f6-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="370f6-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="370f6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="370f6-135">MCI</span><span class="sxs-lookup"><span data-stu-id="370f6-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="370f6-136">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="370f6-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


---
title: MCI_REALIZE comando (mmsystem. h)
description: O \_ comando de concretização do MCI faz com que um dispositivo gráfico perceba sua paleta em um DC (contexto de dispositivo). Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- Multimídia do Windows de comando MCI_REALIZE
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f2e59bfe9bbe1443f55ae0fbcf8819b932bb1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751174"
---
# <a name="mci_realize-command"></a><span data-ttu-id="b1fd9-105">\_Comando de concretização do MCI</span><span class="sxs-lookup"><span data-stu-id="b1fd9-105">MCI\_REALIZE command</span></span>

<span data-ttu-id="b1fd9-106">O \_ comando de concretização do MCI faz com que um dispositivo gráfico perceba sua paleta em um DC (contexto de dispositivo).</span><span class="sxs-lookup"><span data-stu-id="b1fd9-106">The MCI\_REALIZE command causes a graphic device to realize its palette into a device context (DC).</span></span> <span data-ttu-id="b1fd9-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="b1fd9-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="b1fd9-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1fd9-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
);
```



## <a name="parameters"></a><span data-ttu-id="b1fd9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1fd9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1fd9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b1fd9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b1fd9-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="b1fd9-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b1fd9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b1fd9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b1fd9-113">**MCI \_ NOTIFICAr**, **\_ espera de MCI** ou, para dispositivos de vídeo digital **, \_ teste MCI**.</span><span class="sxs-lookup"><span data-stu-id="b1fd9-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or, for digital-video devices, **MCI\_TEST**.</span></span> <span data-ttu-id="b1fd9-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b1fd9-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1fd9-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*</span><span class="sxs-lookup"><span data-stu-id="b1fd9-115"><span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*</span></span>
</dt> <dd>

<span data-ttu-id="b1fd9-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="b1fd9-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="b1fd9-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="b1fd9-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1fd9-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b1fd9-118">Return Value</span></span>

<span data-ttu-id="b1fd9-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="b1fd9-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1fd9-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1fd9-120">Remarks</span></span>

<span data-ttu-id="b1fd9-121">Você deve usar esse comando quando seu aplicativo receber a [**mensagem \_ QUERYNEWPALETTE do WM**](/windows/desktop/gdi/wm-querynewpalette) .</span><span class="sxs-lookup"><span data-stu-id="b1fd9-121">You should use this command when your application receives the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) message.</span></span>

<span data-ttu-id="b1fd9-122">Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo "DigitalVideo":</span><span class="sxs-lookup"><span data-stu-id="b1fd9-122">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="b1fd9-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ perceber \_ BKGD</span><span class="sxs-lookup"><span data-stu-id="b1fd9-123"><span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI\_DGV\_REALIZE\_BKGD</span></span>
</dt> <dd>

<span data-ttu-id="b1fd9-124">Percebe a paleta como uma paleta de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="b1fd9-124">Realizes the palette as a background palette.</span></span>

</dd> <dt>

<span data-ttu-id="b1fd9-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>DGV de MCI \_ \_ perceba \_ normal</span><span class="sxs-lookup"><span data-stu-id="b1fd9-125"><span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>MCI\_DGV\_REALIZE\_NORM</span></span>
</dt> <dd>

<span data-ttu-id="b1fd9-126">O percebe normalmente a paleta.</span><span class="sxs-lookup"><span data-stu-id="b1fd9-126">Realizes the palette normally.</span></span> <span data-ttu-id="b1fd9-127">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="b1fd9-127">This is the default.</span></span>

</dd> </dl>

<span data-ttu-id="b1fd9-128">Para dispositivos de vídeo digital, o parâmetro *lpRealize* aponta para uma estrutura de **\_ \_ parâmetros de reprovação MCI** .</span><span class="sxs-lookup"><span data-stu-id="b1fd9-128">For digital-video devices, the *lpRealize* parameter points to an **MCI\_REALIZE\_PARMS** structure.</span></span> <span data-ttu-id="b1fd9-129">Para obter mais informações, consulte comentários na estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="b1fd9-129">For more information, see comments in the [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1fd9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1fd9-130">Requirements</span></span>



| <span data-ttu-id="b1fd9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1fd9-131">Requirement</span></span> | <span data-ttu-id="b1fd9-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b1fd9-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1fd9-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1fd9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b1fd9-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b1fd9-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b1fd9-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1fd9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b1fd9-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b1fd9-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b1fd9-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b1fd9-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1fd9-138"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1fd9-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1fd9-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1fd9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1fd9-140">MCI</span><span class="sxs-lookup"><span data-stu-id="b1fd9-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b1fd9-141">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="b1fd9-141">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


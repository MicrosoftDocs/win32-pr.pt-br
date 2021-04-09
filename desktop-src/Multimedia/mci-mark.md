---
title: MCI_MARK comando (mmsystem. h)
description: O \_ comando de marca MCI registra ou apaga marcas que podem ser usadas com o \_ comando MCI Seek para pesquisas de alta velocidade. Os dispositivos VCR reconhecem este comando.
ms.assetid: 69b17e5b-99a1-4fb9-bc0e-30e772c1f11f
keywords:
- Multimídia do Windows de comando MCI_MARK
topic_type:
- apiref
api_name:
- MCI_MARK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddc80decb4559659efb29132f17f18459c334fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009059"
---
# <a name="mci_mark-command"></a><span data-ttu-id="a77b0-105">\_Comando de marca MCI</span><span class="sxs-lookup"><span data-stu-id="a77b0-105">MCI\_MARK command</span></span>

<span data-ttu-id="a77b0-106">O \_ comando de marca MCI registra ou apaga marcas que podem ser usadas com o comando [MCI \_ Seek](mci-seek.md) para pesquisas de alta velocidade.</span><span class="sxs-lookup"><span data-stu-id="a77b0-106">The MCI\_MARK command records or erases marks that can be used with the [MCI\_SEEK](mci-seek.md) command for high-speed searches.</span></span> <span data-ttu-id="a77b0-107">Os dispositivos VCR reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="a77b0-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="a77b0-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="a77b0-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MARK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpMark
);
```



## <a name="parameters"></a><span data-ttu-id="a77b0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a77b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a77b0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a77b0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a77b0-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="a77b0-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a77b0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a77b0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a77b0-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="a77b0-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="a77b0-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a77b0-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a77b0-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*</span><span class="sxs-lookup"><span data-stu-id="a77b0-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*</span></span>
</dt> <dd>

<span data-ttu-id="a77b0-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a77b0-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="a77b0-117">(Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)</span><span class="sxs-lookup"><span data-stu-id="a77b0-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a77b0-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a77b0-118">Return Value</span></span>

<span data-ttu-id="a77b0-119">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="a77b0-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a77b0-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a77b0-120">Remarks</span></span>

<span data-ttu-id="a77b0-121">Os seguintes sinalizadores adicionais se aplicam a dispositivos VCR:</span><span class="sxs-lookup"><span data-stu-id="a77b0-121">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="a77b0-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>\_sinalização de videocassete MCI \_ \_ apagar</span><span class="sxs-lookup"><span data-stu-id="a77b0-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>MCI\_VCR\_MARK\_ERASE</span></span>
</dt> <dd>

<span data-ttu-id="a77b0-123">Apaga uma marca na posição atual, se houver uma.</span><span class="sxs-lookup"><span data-stu-id="a77b0-123">Erases a mark at the current position if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="a77b0-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>\_gravação de \_ marca de VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="a77b0-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>MCI\_VCR\_MARK\_WRITE</span></span>
</dt> <dd>

<span data-ttu-id="a77b0-125">Grava uma marca na posição atual.</span><span class="sxs-lookup"><span data-stu-id="a77b0-125">Writes a mark at the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a77b0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a77b0-126">Requirements</span></span>



| <span data-ttu-id="a77b0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a77b0-127">Requirement</span></span> | <span data-ttu-id="a77b0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a77b0-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a77b0-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a77b0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a77b0-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a77b0-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a77b0-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a77b0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a77b0-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a77b0-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a77b0-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a77b0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a77b0-134"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a77b0-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a77b0-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a77b0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a77b0-136">MCI</span><span class="sxs-lookup"><span data-stu-id="a77b0-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a77b0-137">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="a77b0-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


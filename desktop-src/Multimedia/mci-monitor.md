---
title: MCI_MONITOR comando (mmsystem. h)
description: O \_ comando monitor MCI especifica a origem da apresentação. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- Multimídia do Windows de comando MCI_MONITOR
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918757"
---
# <a name="mci_monitor-command"></a><span data-ttu-id="b243a-105">\_Comando do monitor MCI</span><span class="sxs-lookup"><span data-stu-id="b243a-105">MCI\_MONITOR command</span></span>

<span data-ttu-id="b243a-106">O \_ comando monitor MCI especifica a origem da apresentação.</span><span class="sxs-lookup"><span data-stu-id="b243a-106">The MCI\_MONITOR command specifies the presentation source.</span></span> <span data-ttu-id="b243a-107">Dispositivos de vídeo digital reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="b243a-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="b243a-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="b243a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="b243a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b243a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b243a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="b243a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="b243a-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="b243a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="b243a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b243a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b243a-113">\_Notificação MCI, \_ espera MCI ou teste MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="b243a-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="b243a-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b243a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b243a-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*</span><span class="sxs-lookup"><span data-stu-id="b243a-115"><span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*</span></span>
</dt> <dd>

<span data-ttu-id="b243a-116">Ponteiro para uma estrutura de [**\_ parâmetros de \_ Monitor \_ de DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) .</span><span class="sxs-lookup"><span data-stu-id="b243a-116">Pointer to an [**MCI\_DGV\_MONITOR\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b243a-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b243a-117">Return Value</span></span>

<span data-ttu-id="b243a-118">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="b243a-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b243a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b243a-119">Remarks</span></span>

<span data-ttu-id="b243a-120">Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="b243a-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="b243a-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>\_método de \_ Monitor de DGV MCI \_</span><span class="sxs-lookup"><span data-stu-id="b243a-121"><span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>MCI\_DGV\_MONITOR\_METHOD</span></span>
</dt> <dd>

<span data-ttu-id="b243a-122">Uma constante indicando que o método de monitoramento está incluído no membro **dwMethod** da estrutura identificada por *lpMonitor*.</span><span class="sxs-lookup"><span data-stu-id="b243a-122">A constant indicating the method of monitoring is included in the **dwMethod** member of the structure identified by *lpMonitor*.</span></span>

<span data-ttu-id="b243a-123">Quando o \_ sinalizador de entrada do monitor MCI DGV \_ \_ é usado no membro **dwSource** , isso seleciona o método de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="b243a-123">When the MCI\_DGV\_MONITOR\_INPUT flag is used in the **dwSource** member, this selects the method of monitoring.</span></span> <span data-ttu-id="b243a-124">Normalmente, diferentes métodos de monitoramento têm diferentes implicações sobre como o hardware é usado.</span><span class="sxs-lookup"><span data-stu-id="b243a-124">Typically, different monitoring methods have different implications on how the hardware is used.</span></span> <span data-ttu-id="b243a-125">O método de monitoramento padrão é selecionado pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b243a-125">The default monitoring method is selected by the device.</span></span>

</dd> <dt>

<span data-ttu-id="b243a-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>\_origem do \_ Monitor MCI DGV \_</span><span class="sxs-lookup"><span data-stu-id="b243a-126"><span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>MCI\_DGV\_MONITOR\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="b243a-127">Uma constante indicando que a origem do monitor está incluída no membro **dwSource** da estrutura identificada por *lpMonitor*.</span><span class="sxs-lookup"><span data-stu-id="b243a-127">A constant indicating the monitor source is included in the **dwSource** member of the structure identified by *lpMonitor*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b243a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b243a-128">Requirements</span></span>



| <span data-ttu-id="b243a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b243a-129">Requirement</span></span> | <span data-ttu-id="b243a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b243a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b243a-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b243a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b243a-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b243a-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b243a-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b243a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b243a-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b243a-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b243a-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b243a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b243a-136"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b243a-136"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b243a-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b243a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b243a-138">MCI</span><span class="sxs-lookup"><span data-stu-id="b243a-138">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b243a-139">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="b243a-139">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


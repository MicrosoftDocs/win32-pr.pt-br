---
title: MCI_CLOSE comando (mmsystem. h)
description: O \_ comando MCI Close libera o acesso a um dispositivo ou arquivo. Todos os dispositivos reconhecem este comando.
ms.assetid: 62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f
keywords:
- Multimídia do Windows de comando MCI_CLOSE
topic_type:
- apiref
api_name:
- MCI_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 417129595405aeb6c9a2345eb9c3f03f1e2731e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085445"
---
# <a name="mci_close-command"></a><span data-ttu-id="6750a-105">\_Comando de fechamento MCI</span><span class="sxs-lookup"><span data-stu-id="6750a-105">MCI\_CLOSE command</span></span>

<span data-ttu-id="6750a-106">O \_ comando MCI Close libera o acesso a um dispositivo ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="6750a-106">The MCI\_CLOSE command releases access to a device or file.</span></span> <span data-ttu-id="6750a-107">Todos os dispositivos reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="6750a-107">All devices recognize this command.</span></span>

<span data-ttu-id="6750a-108">Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="6750a-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CLOSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpClose
);
```



## <a name="parameters"></a><span data-ttu-id="6750a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6750a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6750a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="6750a-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6750a-111">Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.</span><span class="sxs-lookup"><span data-stu-id="6750a-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="6750a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6750a-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6750a-113">\_Notificação MCI ou \_ espera MCI.</span><span class="sxs-lookup"><span data-stu-id="6750a-113">MCI\_NOTIFY or MCI\_WAIT.</span></span> <span data-ttu-id="6750a-114">Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6750a-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6750a-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*</span><span class="sxs-lookup"><span data-stu-id="6750a-115"><span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*lpClose*</span></span>
</dt> <dd>

<span data-ttu-id="6750a-116">Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="6750a-116">Pointer to an [**MCI\_ GENERIC\_ PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="6750a-117">(Você também pode usar uma estrutura de **\_ \_ parâmetros de fechamento MCI** .</span><span class="sxs-lookup"><span data-stu-id="6750a-117">(You can also use an **MCI\_CLOSE\_PARMS** structure.</span></span> <span data-ttu-id="6750a-118">Para obter mais informações, consulte os comentários **para \_ \_ parâmetros genéricos MCI**.)</span><span class="sxs-lookup"><span data-stu-id="6750a-118">For more information, see the comments for **MCI\_GENERIC\_PARMS**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6750a-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6750a-119">Return Value</span></span>

<span data-ttu-id="6750a-120">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="6750a-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6750a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="6750a-121">Remarks</span></span>

<span data-ttu-id="6750a-122">Sair de um aplicativo sem fechar os dispositivos MCI que ele abriu pode deixar o dispositivo inacessível.</span><span class="sxs-lookup"><span data-stu-id="6750a-122">Exiting an application without closing any MCI devices it has opened can leave the device inaccessible.</span></span> <span data-ttu-id="6750a-123">Seu aplicativo deve fechar explicitamente cada dispositivo ou arquivo quando ele for concluído com ele.</span><span class="sxs-lookup"><span data-stu-id="6750a-123">Your application should explicitly close each device or file when it is finished with it.</span></span> <span data-ttu-id="6750a-124">O MCI descarrega o dispositivo quando todas as instâncias do dispositivo ou todos os arquivos associados são fechados.</span><span class="sxs-lookup"><span data-stu-id="6750a-124">MCI unloads the device when all instances of the device or all associated files are closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6750a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6750a-125">Requirements</span></span>



| <span data-ttu-id="6750a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6750a-126">Requirement</span></span> | <span data-ttu-id="6750a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6750a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6750a-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6750a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6750a-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6750a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6750a-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6750a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6750a-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6750a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6750a-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6750a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6750a-133"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6750a-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6750a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6750a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6750a-135">MCI</span><span class="sxs-lookup"><span data-stu-id="6750a-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6750a-136">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="6750a-136">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 


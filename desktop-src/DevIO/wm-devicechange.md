---
description: Notifica um aplicativo sobre uma alteração na configuração de hardware de um dispositivo ou computador.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Mensagem de WM_DEVICECHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370405"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="fa633-103">Mensagem do WM \_ DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="fa633-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="fa633-104">Notifica um aplicativo sobre uma alteração na configuração de hardware de um dispositivo ou computador.</span><span class="sxs-lookup"><span data-stu-id="fa633-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="fa633-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fa633-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="fa633-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa633-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa633-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="fa633-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="fa633-108">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="fa633-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="fa633-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="fa633-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="fa633-110">O **identificador \_ DEVICECHANGE do WM** .</span><span class="sxs-lookup"><span data-stu-id="fa633-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="fa633-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa633-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa633-112">O evento que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="fa633-112">The event that has occurred.</span></span> <span data-ttu-id="fa633-113">Esse parâmetro pode ser um dos seguintes valores do arquivo de cabeçalho DBT. h.</span><span class="sxs-lookup"><span data-stu-id="fa633-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>



| <span data-ttu-id="fa633-114">Valor</span><span class="sxs-lookup"><span data-stu-id="fa633-114">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="fa633-115">Significado</span><span class="sxs-lookup"><span data-stu-id="fa633-115">Meaning</span></span>                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <span data-ttu-id="fa633-116"><dt>**[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span><span class="sxs-lookup"><span data-stu-id="fa633-116"><dt>**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt></span></span> </dl>             | <span data-ttu-id="fa633-117">Uma solicitação para alterar a configuração atual (Dock ou Dock) foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="fa633-117">A request to change the current configuration (dock or undock) has been canceled.</span></span><br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <span data-ttu-id="fa633-118"><dt>**[DBT \_ CONFIGchanged](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span><span class="sxs-lookup"><span data-stu-id="fa633-118"><dt>**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</dt> <dt>0x0018</dt></span></span> </dl>                                         | <span data-ttu-id="fa633-119">A configuração atual foi alterada devido a um encaixe ou desencaixe.</span><span class="sxs-lookup"><span data-stu-id="fa633-119">The current configuration has changed, due to a dock or undock.</span></span><br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <span data-ttu-id="fa633-120"><dt>**[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt></span><span class="sxs-lookup"><span data-stu-id="fa633-120"><dt>**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt></span></span> </dl>                                                 | <span data-ttu-id="fa633-121">Ocorreu um evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="fa633-121">A custom event has occurred.</span></span><br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <span data-ttu-id="fa633-122"><dt>**[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="fa633-122"><dt>**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt></span></span> </dl>                                         | <span data-ttu-id="fa633-123">Um dispositivo ou parte da mídia foi inserido e agora está disponível.</span><span class="sxs-lookup"><span data-stu-id="fa633-123">A device or piece of media has been inserted and is now available.</span></span><br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <span data-ttu-id="fa633-124"><dt>**[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span><span class="sxs-lookup"><span data-stu-id="fa633-124"><dt>**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt></span></span> </dl>                         | <span data-ttu-id="fa633-125">A permissão é solicitada para remover um dispositivo ou parte da mídia.</span><span class="sxs-lookup"><span data-stu-id="fa633-125">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="fa633-126">Qualquer aplicativo pode negar essa solicitação e cancelar a remoção.</span><span class="sxs-lookup"><span data-stu-id="fa633-126">Any application can deny this request and cancel the removal.</span></span><br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <span data-ttu-id="fa633-127"><dt>**[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span><span class="sxs-lookup"><span data-stu-id="fa633-127"><dt>**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt></span></span> </dl> | <span data-ttu-id="fa633-128">Uma solicitação para remover um dispositivo ou parte da mídia foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="fa633-128">A request to remove a device or piece of media has been canceled.</span></span><br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <span data-ttu-id="fa633-129"><dt>**[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span><span class="sxs-lookup"><span data-stu-id="fa633-129"><dt>**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt></span></span> </dl>             | <span data-ttu-id="fa633-130">Um dispositivo ou parte da mídia foi removida.</span><span class="sxs-lookup"><span data-stu-id="fa633-130">A device or piece of media has been removed.</span></span><br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <span data-ttu-id="fa633-131"><dt>**[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span><span class="sxs-lookup"><span data-stu-id="fa633-131"><dt>**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt></span></span> </dl>                 | <span data-ttu-id="fa633-132">Um dispositivo ou parte da mídia está prestes a ser removida.</span><span class="sxs-lookup"><span data-stu-id="fa633-132">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="fa633-133">Não pode ser negado.</span><span class="sxs-lookup"><span data-stu-id="fa633-133">Cannot be denied.</span></span><br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <span data-ttu-id="fa633-134"><dt>**[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span><span class="sxs-lookup"><span data-stu-id="fa633-134"><dt>**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt></span></span> </dl>                     | <span data-ttu-id="fa633-135">Ocorreu um evento específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa633-135">A device-specific event has occurred.</span></span><br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <span data-ttu-id="fa633-136"><dt>**[DBT \_ DEVNODES \_ alterou](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span><span class="sxs-lookup"><span data-stu-id="fa633-136"><dt>**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt></span></span> </dl>                            | <span data-ttu-id="fa633-137">Um dispositivo foi adicionado ou removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="fa633-137">A device has been added to or removed from the system.</span></span><br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <span data-ttu-id="fa633-138"><dt>**[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span><span class="sxs-lookup"><span data-stu-id="fa633-138"><dt>**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt></span></span> </dl>                         | <span data-ttu-id="fa633-139">A permissão é solicitada para alterar a configuração atual (Dock ou desencaixar).</span><span class="sxs-lookup"><span data-stu-id="fa633-139">Permission is requested to change the current configuration (dock or undock).</span></span><br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <span data-ttu-id="fa633-140"><dt>**[DBT \_ 0xFFFF definido pelo UserDefined](dbt-userdefined.md)**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fa633-140"><dt>**[DBT\_USERDEFINED](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt></span></span> </dl>                                                 | <span data-ttu-id="fa633-141">O significado dessa mensagem é definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fa633-141">The meaning of this message is user-defined.</span></span><br/>                                                                                |



 

</dd> <dt>

<span data-ttu-id="fa633-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa633-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa633-143">Um ponteiro para uma estrutura que contém dados específicos do evento.</span><span class="sxs-lookup"><span data-stu-id="fa633-143">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="fa633-144">Seu formato depende do valor do parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="fa633-144">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="fa633-145">Para obter mais informações, consulte a documentação de cada evento.</span><span class="sxs-lookup"><span data-stu-id="fa633-145">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa633-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa633-146">Return value</span></span>

<span data-ttu-id="fa633-147">Retornar **true** para conceder a solicitação.</span><span class="sxs-lookup"><span data-stu-id="fa633-147">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="fa633-148">Retornar **consulta de difusão \_ \_ negar** para negar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="fa633-148">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa633-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa633-149">Remarks</span></span>

<span data-ttu-id="fa633-150">Para dispositivos que oferecem recursos controlávels por software, como ejeção e bloqueio, o sistema normalmente envia uma mensagem [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) para permitir que aplicativos e drivers de dispositivo terminem o uso do dispositivo normalmente.</span><span class="sxs-lookup"><span data-stu-id="fa633-150">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="fa633-151">Se o sistema forçar a remoção de um dispositivo, ele não poderá enviar uma mensagem [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) antes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="fa633-151">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa633-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa633-152">Requirements</span></span>



| <span data-ttu-id="fa633-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa633-153">Requirement</span></span> | <span data-ttu-id="fa633-154">Valor</span><span class="sxs-lookup"><span data-stu-id="fa633-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa633-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa633-155">Minimum supported client</span></span><br/> | <span data-ttu-id="fa633-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fa633-156">Windows XP</span></span><br/>                                                                                             |
| <span data-ttu-id="fa633-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa633-157">Minimum supported server</span></span><br/> | <span data-ttu-id="fa633-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fa633-158">Windows Server 2003</span></span><br/>                                                                                    |
| <span data-ttu-id="fa633-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa633-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa633-160"><dt>WinUser. h (incluir Windows. h ou DBT. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa633-160"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa633-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa633-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa633-162">DBT \_ CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="fa633-162">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="fa633-163">DBT \_ ConfigChanged</span><span class="sxs-lookup"><span data-stu-id="fa633-163">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="fa633-164">DBT \_ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="fa633-164">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="fa633-165">DBT \_ DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="fa633-165">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="fa633-166">DBT \_ DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="fa633-166">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="fa633-167">DBT \_ DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="fa633-167">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="fa633-168">DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="fa633-168">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="fa633-169">DBT \_ DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="fa633-169">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="fa633-170">DBT \_ DEVICETYPESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="fa633-170">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="fa633-171">DBT \_ DEVNODES \_ alterado</span><span class="sxs-lookup"><span data-stu-id="fa633-171">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="fa633-172">DBT \_ QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="fa633-172">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="fa633-173">DBT \_ USERdefined</span><span class="sxs-lookup"><span data-stu-id="fa633-173">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>

 


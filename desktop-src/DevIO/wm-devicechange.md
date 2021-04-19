---
description: Notifica um aplicativo sobre uma alteração na configuração de hardware de um dispositivo ou computador.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Mensagem de WM_DEVICECHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cc45d7a7978d5501e51cc1355c43afcf12b956
ms.sourcegitcommit: 8c1942ac6731488abbeae46a7dbe3da166fee2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2021
ms.locfileid: "107581498"
---
# <a name="wm_devicechange-message"></a><span data-ttu-id="bf5bb-103">Mensagem do WM \_ DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="bf5bb-103">WM\_DEVICECHANGE message</span></span>

<span data-ttu-id="bf5bb-104">Notifica um aplicativo sobre uma alteração na configuração de hardware de um dispositivo ou computador.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-104">Notifies an application of a change to the hardware configuration of a device or the computer.</span></span>

<span data-ttu-id="bf5bb-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bf5bb-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```

## <a name="parameters"></a><span data-ttu-id="bf5bb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf5bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf5bb-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="bf5bb-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bf5bb-108">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-108">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="bf5bb-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="bf5bb-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="bf5bb-110">O **identificador \_ DEVICECHANGE do WM** .</span><span class="sxs-lookup"><span data-stu-id="bf5bb-110">The **WM\_DEVICECHANGE** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bf5bb-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf5bb-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf5bb-112">O evento que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-112">The event that has occurred.</span></span> <span data-ttu-id="bf5bb-113">Esse parâmetro pode ser um dos seguintes valores do arquivo de cabeçalho DBT. h.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-113">This parameter can be one of the following values from the Dbt.h header file.</span></span>

| <span data-ttu-id="bf5bb-114">Valor</span><span class="sxs-lookup"><span data-stu-id="bf5bb-114">Value</span></span> | <span data-ttu-id="bf5bb-115">Significado</span><span class="sxs-lookup"><span data-stu-id="bf5bb-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="bf5bb-116">**[DBT \_ DEVNODES \_ alterado](dbt-devnodes-changed.md)**</span><span class="sxs-lookup"><span data-stu-id="bf5bb-116">**[DBT\_DEVNODES\_CHANGED](dbt-devnodes-changed.md)**</span></span></br><span data-ttu-id="bf5bb-117">0x0007</span><span class="sxs-lookup"><span data-stu-id="bf5bb-117">0x0007</span></span> | <span data-ttu-id="bf5bb-118">Um dispositivo foi adicionado ou removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-118">A device has been added to or removed from the system.</span></span> |
| <span data-ttu-id="bf5bb-119">**[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span><span class="sxs-lookup"><span data-stu-id="bf5bb-119">**[DBT\_QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</span></span></br><span data-ttu-id="bf5bb-120">0x0017</span><span class="sxs-lookup"><span data-stu-id="bf5bb-120">0x0017</span></span> | <span data-ttu-id="bf5bb-121">A permissão é solicitada para alterar a configuração atual (Dock ou desencaixar).</span><span class="sxs-lookup"><span data-stu-id="bf5bb-121">Permission is requested to change the current configuration (dock or undock).</span></span> |
| <span data-ttu-id="bf5bb-122">**[DBT \_ ConfigChanged](dbt-configchanged.md)**</span><span class="sxs-lookup"><span data-stu-id="bf5bb-122">**[DBT\_CONFIGCHANGED](dbt-configchanged.md)**</span></span></br><span data-ttu-id="bf5bb-123">0x0018</span><span class="sxs-lookup"><span data-stu-id="bf5bb-123">0x0018</span></span> | <span data-ttu-id="bf5bb-124">A configuração atual foi alterada devido a um encaixe ou desencaixe.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-124">The current configuration has changed, due to a dock or undock.</span></span> |
| <span data-ttu-id="bf5bb-125">**[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span><span class="sxs-lookup"><span data-stu-id="bf5bb-125">**[DBT\_CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</span></span></br><span data-ttu-id="bf5bb-126">0x0019</span><span class="sxs-lookup"><span data-stu-id="bf5bb-126">0x0019</span></span> | <span data-ttu-id="bf5bb-127">Uma solicitação para alterar a configuração atual (Dock ou Dock) foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-127">A request to change the current configuration (dock or undock) has been canceled.</span></span> |
| <span data-ttu-id="bf5bb-128">**[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</span><span class="sxs-lookup"><span data-stu-id="bf5bb-128">**[DBT\_DEVICEARRIVAL](dbt-devicearrival.md)**</span></span></br><span data-ttu-id="bf5bb-129">0x8000</span><span class="sxs-lookup"><span data-stu-id="bf5bb-129">0x8000</span></span> | <span data-ttu-id="bf5bb-130">Um dispositivo ou parte da mídia foi inserido e agora está disponível.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-130">A device or piece of media has been inserted and is now available.</span></span> |
| <span data-ttu-id="bf5bb-131">**[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span><span class="sxs-lookup"><span data-stu-id="bf5bb-131">**[DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</span></span></br><span data-ttu-id="bf5bb-132">0x8001</span><span class="sxs-lookup"><span data-stu-id="bf5bb-132">0x8001</span></span> | <span data-ttu-id="bf5bb-133">A permissão é solicitada para remover um dispositivo ou parte da mídia.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-133">Permission is requested to remove a device or piece of media.</span></span> <span data-ttu-id="bf5bb-134">Qualquer aplicativo pode negar essa solicitação e cancelar a remoção.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-134">Any application can deny this request and cancel the removal.</span></span> |
| <span data-ttu-id="bf5bb-135">**[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span><span class="sxs-lookup"><span data-stu-id="bf5bb-135">**[DBT\_DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</span></span></br><span data-ttu-id="bf5bb-136">0x8002</span><span class="sxs-lookup"><span data-stu-id="bf5bb-136">0x8002</span></span> | <span data-ttu-id="bf5bb-137">Uma solicitação para remover um dispositivo ou parte da mídia foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-137">A request to remove a device or piece of media has been canceled.</span></span> |
| <span data-ttu-id="bf5bb-138">**[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span><span class="sxs-lookup"><span data-stu-id="bf5bb-138">**[DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</span></span></br><span data-ttu-id="bf5bb-139">0x8003</span><span class="sxs-lookup"><span data-stu-id="bf5bb-139">0x8003</span></span> | <span data-ttu-id="bf5bb-140">Um dispositivo ou parte da mídia está prestes a ser removida.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-140">A device or piece of media is about to be removed.</span></span> <span data-ttu-id="bf5bb-141">Não pode ser negado.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-141">Cannot be denied.</span></span> |
| <span data-ttu-id="bf5bb-142">**[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span><span class="sxs-lookup"><span data-stu-id="bf5bb-142">**[DBT\_DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</span></span></br><span data-ttu-id="bf5bb-143">0x8004</span><span class="sxs-lookup"><span data-stu-id="bf5bb-143">0x8004</span></span> | <span data-ttu-id="bf5bb-144">Um dispositivo ou parte da mídia foi removida.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-144">A device or piece of media has been removed.</span></span> |
| <span data-ttu-id="bf5bb-145">**[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span><span class="sxs-lookup"><span data-stu-id="bf5bb-145">**[DBT\_DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</span></span></br><span data-ttu-id="bf5bb-146">0x8005</span><span class="sxs-lookup"><span data-stu-id="bf5bb-146">0x8005</span></span> | <span data-ttu-id="bf5bb-147">Ocorreu um evento específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-147">A device-specific event has occurred.</span></span> |
| <span data-ttu-id="bf5bb-148">**[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</span><span class="sxs-lookup"><span data-stu-id="bf5bb-148">**[DBT\_CUSTOMEVENT](dbt-customevent.md)**</span></span></br><span data-ttu-id="bf5bb-149">0x8006</span><span class="sxs-lookup"><span data-stu-id="bf5bb-149">0x8006</span></span> | <span data-ttu-id="bf5bb-150">Ocorreu um evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-150">A custom event has occurred.</span></span> |
| <span data-ttu-id="bf5bb-151">**[DBT \_ USERdefined](dbt-userdefined.md)**</span><span class="sxs-lookup"><span data-stu-id="bf5bb-151">**[DBT\_USERDEFINED](dbt-userdefined.md)**</span></span></br><span data-ttu-id="bf5bb-152">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="bf5bb-152">0xFFFF</span></span> | <span data-ttu-id="bf5bb-153">O significado dessa mensagem é definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-153">The meaning of this message is user-defined.</span></span> |

</dd> <dt>

<span data-ttu-id="bf5bb-154">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf5bb-154">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf5bb-155">Um ponteiro para uma estrutura que contém dados específicos do evento.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-155">A pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="bf5bb-156">Seu formato depende do valor do parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="bf5bb-156">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="bf5bb-157">Para obter mais informações, consulte a documentação de cada evento.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-157">For more information, refer to the documentation for each event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf5bb-158">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf5bb-158">Return value</span></span>

<span data-ttu-id="bf5bb-159">Retornar **true** para conceder a solicitação.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-159">Return **TRUE** to grant the request.</span></span>

<span data-ttu-id="bf5bb-160">Retornar **consulta de difusão \_ \_ negar** para negar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-160">Return **BROADCAST\_QUERY\_DENY** to deny the request.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf5bb-161">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf5bb-161">Remarks</span></span>

<span data-ttu-id="bf5bb-162">Para dispositivos que oferecem recursos controlávels por software, como ejeção e bloqueio, o sistema normalmente envia uma mensagem [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) para permitir que aplicativos e drivers de dispositivo terminem o uso do dispositivo normalmente.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-162">For devices that offer software-controllable features, such as ejection and locking, the system typically sends a [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) message to let applications and device drivers end their use of the device gracefully.</span></span> <span data-ttu-id="bf5bb-163">Se o sistema forçar a remoção de um dispositivo, ele não poderá enviar uma mensagem [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) antes de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="bf5bb-163">If the system forcibly removes a device, it may not send a [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message before doing so.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf5bb-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf5bb-164">Requirements</span></span>

| <span data-ttu-id="bf5bb-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf5bb-165">Requirement</span></span> | <span data-ttu-id="bf5bb-166">Valor</span><span class="sxs-lookup"><span data-stu-id="bf5bb-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf5bb-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf5bb-167">Minimum supported client</span></span> | <span data-ttu-id="bf5bb-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf5bb-168">Windows XP</span></span> |
| <span data-ttu-id="bf5bb-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf5bb-169">Minimum supported server</span></span> | <span data-ttu-id="bf5bb-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf5bb-170">Windows Server 2003</span></span>|
| <span data-ttu-id="bf5bb-171">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf5bb-171">Header</span></span> | <dl> <span data-ttu-id="bf5bb-172"><dt>WinUser. h (incluir Windows. h ou DBT. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf5bb-172"><dt>Winuser.h (include Windows.h or Dbt.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="bf5bb-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf5bb-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf5bb-174">DBT \_ CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="bf5bb-174">DBT\_CONFIGCHANGECANCELED</span></span>](dbt-configchangecanceled.md)
</dt> <dt>

[<span data-ttu-id="bf5bb-175">DBT \_ ConfigChanged</span><span class="sxs-lookup"><span data-stu-id="bf5bb-175">DBT\_CONFIGCHANGED</span></span>](dbt-configchanged.md)
</dt> <dt>

[<span data-ttu-id="bf5bb-176">DBT \_ CUSTOMEVENT</span><span class="sxs-lookup"><span data-stu-id="bf5bb-176">DBT\_CUSTOMEVENT</span></span>](dbt-customevent.md)
</dt> <dt>

[<span data-ttu-id="bf5bb-177">DBT \_ DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="bf5bb-177">DBT\_DEVICEARRIVAL</span></span>](dbt-devicearrival.md)
</dt> <dt>

[<span data-ttu-id="bf5bb-178">DBT \_ DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="bf5bb-178">DBT\_DEVICEQUERYREMOVE</span></span>](dbt-devicequeryremove.md)
</dt> <dt>

[<span data-ttu-id="bf5bb-179">DBT \_ DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="bf5bb-179">DBT\_DEVICEQUERYREMOVEFAILED</span></span>](dbt-devicequeryremovefailed.md)
</dt> <dt>

[<span data-ttu-id="bf5bb-180">DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="bf5bb-180">DBT\_DEVICEREMOVECOMPLETE</span></span>](dbt-deviceremovecomplete.md)
</dt> <dt>

[<span data-ttu-id="bf5bb-181">DBT \_ DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="bf5bb-181">DBT\_DEVICEREMOVEPENDING</span></span>](dbt-deviceremovepending.md)
</dt> <dt>

[<span data-ttu-id="bf5bb-182">DBT \_ DEVICETYPESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="bf5bb-182">DBT\_DEVICETYPESPECIFIC</span></span>](dbt-devicetypespecific.md)
</dt> <dt>

[<span data-ttu-id="bf5bb-183">DBT \_ DEVNODES \_ alterado</span><span class="sxs-lookup"><span data-stu-id="bf5bb-183">DBT\_DEVNODES\_CHANGED</span></span>](dbt-devnodes-changed.md)
</dt> <dt>

[<span data-ttu-id="bf5bb-184">DBT \_ QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="bf5bb-184">DBT\_QUERYCHANGECONFIG</span></span>](dbt-querychangeconfig.md)
</dt> <dt>

[<span data-ttu-id="bf5bb-185">DBT \_ USERdefined</span><span class="sxs-lookup"><span data-stu-id="bf5bb-185">DBT\_USERDEFINED</span></span>](dbt-userdefined.md)
</dt> </dl>

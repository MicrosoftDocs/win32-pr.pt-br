---
description: Uma mensagem que é enviada para todas as janelas de nível superior quando a função SystemParametersInfo altera uma configuração de todo o sistema ou quando as configurações de política são alteradas.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: Mensagem de WM_SETTINGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c3d1360b5e4cc5de2dbd23b09b8f2ad034948f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171699"
---
# <a name="wm_settingchange-message"></a><span data-ttu-id="ed4cb-103">Mensagem do WM \_ SETTINGCHANGE</span><span class="sxs-lookup"><span data-stu-id="ed4cb-103">WM\_SETTINGCHANGE message</span></span>

<span data-ttu-id="ed4cb-104">Uma mensagem que é enviada para todas as janelas de nível superior quando a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) altera uma configuração de todo o sistema ou quando as configurações de política são alteradas.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-104">A message that is sent to all top-level windows when the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function changes a system-wide setting or when policy settings have changed.</span></span>

<span data-ttu-id="ed4cb-105">Os aplicativos devem enviar o **WM \_ SETTINGCHANGE** para todas as janelas de nível superior quando fizerem alterações nos parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-105">Applications should send **WM\_SETTINGCHANGE** to all top-level windows when they make changes to system parameters.</span></span> <span data-ttu-id="ed4cb-106">(Esta mensagem não pode ser enviada diretamente a uma janela.) Para enviar a mensagem do **WM \_ SETTINGCHANGE** para todas as janelas de nível superior, use a função [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) com o parâmetro *HWND* definido como a **\_ difusão HWND**.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-106">(This message cannot be sent directly to a window.) To send the **WM\_SETTINGCHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hwnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="ed4cb-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ed4cb-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a><span data-ttu-id="ed4cb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed4cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed4cb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed4cb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed4cb-110">Quando o sistema envia essa mensagem como resultado de uma chamada [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , o parâmetro *wParam* é o valor do parâmetro *UiAction* passado para a função **SystemParametersInfo** .</span><span class="sxs-lookup"><span data-stu-id="ed4cb-110">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, the *wParam* parameter is the value of the *uiAction* parameter passed to the **SystemParametersInfo** function.</span></span> <span data-ttu-id="ed4cb-111">Para obter uma lista de valores, consulte **SystemParametersInfo**.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-111">For a list of values, see **SystemParametersInfo**.</span></span>

<span data-ttu-id="ed4cb-112">Quando o sistema envia essa mensagem como resultado de uma alteração nas configurações de política, esse parâmetro indica o tipo de política que foi aplicada.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-112">When the system sends this message as a result of a change in policy settings, this parameter indicates the type of policy that was applied.</span></span> <span data-ttu-id="ed4cb-113">Esse valor será 1 se a política do computador tiver sido aplicada ou zero se a política do usuário tiver sido aplicada.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-113">This value is 1 if computer policy was applied or zero if user policy was applied.</span></span>

<span data-ttu-id="ed4cb-114">Quando o sistema envia essa mensagem como resultado de uma alteração nas configurações de localidade, esse parâmetro é zero.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-114">When the system sends this message as a result of a change in locale settings, this parameter is zero.</span></span>

<span data-ttu-id="ed4cb-115">Quando um aplicativo envia essa mensagem, esse parâmetro deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-115">When an application sends this message, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ed4cb-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed4cb-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed4cb-117">Quando o sistema envia essa mensagem como resultado de uma chamada [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , *lParam* é um ponteiro para uma cadeia de caracteres que indica a área que contém o parâmetro do sistema que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-117">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, *lParam* is a pointer to a string that indicates the area containing the system parameter that was changed.</span></span> <span data-ttu-id="ed4cb-118">Esse parâmetro geralmente não indica qual parâmetro de sistema específico foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-118">This parameter does not usually indicate which specific system parameter changed.</span></span> <span data-ttu-id="ed4cb-119">(Observe que alguns aplicativos enviam essa mensagem com *lParam* definido como **NULL**.) Em geral, ao receber essa mensagem, você deve verificar e recarregar as configurações de parâmetro do sistema que são usadas pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-119">(Note that some applications send this message with *lParam* set to **NULL**.) In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

<span data-ttu-id="ed4cb-120">Essa cadeia de caracteres pode ser o nome de uma chave do registro ou o nome de uma seção no arquivo Win.ini.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-120">This string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="ed4cb-121">Quando a cadeia de caracteres é um nome de registro, ela normalmente indica apenas o nó folha no registro, não o caminho completo.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-121">When the string is a registry name, it typically indicates only the leaf node in the registry, not the full path.</span></span>

<span data-ttu-id="ed4cb-122">Quando o sistema envia essa mensagem como resultado de uma alteração nas configurações de política, esse parâmetro aponta para a cadeia de caracteres "Policy".</span><span class="sxs-lookup"><span data-stu-id="ed4cb-122">When the system sends this message as a result of a change in policy settings, this parameter points to the string "Policy".</span></span>

<span data-ttu-id="ed4cb-123">Quando o sistema envia essa mensagem como resultado de uma alteração nas configurações de localidade, esse parâmetro aponta para a cadeia de caracteres "intl".</span><span class="sxs-lookup"><span data-stu-id="ed4cb-123">When the system sends this message as a result of a change in locale settings, this parameter points to the string "intl".</span></span>

<span data-ttu-id="ed4cb-124">Para afetar uma alteração nas variáveis de ambiente do sistema ou do usuário, transmita essa mensagem com *lParam* definido para a cadeia de caracteres "Environment".</span><span class="sxs-lookup"><span data-stu-id="ed4cb-124">To effect a change in the environment variables for the system or the user, broadcast this message with *lParam* set to the string "Environment".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed4cb-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed4cb-125">Return value</span></span>

<span data-ttu-id="ed4cb-126">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="ed4cb-126">Type: **LRESULT**</span></span>

<span data-ttu-id="ed4cb-127">Se você processar essa mensagem, retornará zero.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-127">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed4cb-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed4cb-128">Remarks</span></span>

<span data-ttu-id="ed4cb-129">O parâmetro *lParam* indica qual métrica do sistema foi alterada, por exemplo, "ConvertibleSlateMode" se o indicador ConvertibleSlateMode foi alternado ou "SystemDockMode" se o indicador encaixado foi alternado.</span><span class="sxs-lookup"><span data-stu-id="ed4cb-129">The *lParam* parameter indicates which system metric has changed, for example, "ConvertibleSlateMode" if the CONVERTIBLESLATEMODE indicator was toggled or "SystemDockMode" if the DOCKED indicator was toggled.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed4cb-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed4cb-130">Requirements</span></span>



| <span data-ttu-id="ed4cb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed4cb-131">Requirement</span></span> | <span data-ttu-id="ed4cb-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ed4cb-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed4cb-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed4cb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ed4cb-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed4cb-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ed4cb-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed4cb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ed4cb-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed4cb-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ed4cb-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ed4cb-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed4cb-138"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed4cb-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed4cb-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed4cb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed4cb-140">Eventos de política</span><span class="sxs-lookup"><span data-stu-id="ed4cb-140">Policy Events</span></span>](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[<span data-ttu-id="ed4cb-141">**SendMessageTimeout**</span><span class="sxs-lookup"><span data-stu-id="ed4cb-141">**SendMessageTimeout**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[<span data-ttu-id="ed4cb-142">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="ed4cb-142">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 

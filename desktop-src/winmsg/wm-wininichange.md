---
description: Um aplicativo envia a mensagem do WM \_ WININICHANGE para todas as janelas de nível superior depois de fazer uma alteração no arquivo de WIN.INI. A função SystemParametersInfo envia essa mensagem depois que um aplicativo usa a função para alterar uma configuração em WIN.INI.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: Mensagem de WM_WININICHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b8db6c4794a8c1a572f61028d32eaeaf578d0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920874"
---
# <a name="wm_wininichange-message"></a><span data-ttu-id="9d5a7-104">Mensagem do WM \_ WININICHANGE</span><span class="sxs-lookup"><span data-stu-id="9d5a7-104">WM\_WININICHANGE message</span></span>

<span data-ttu-id="9d5a7-105">Um aplicativo envia a mensagem do **WM \_ WININICHANGE** para todas as janelas de nível superior depois de fazer uma alteração no arquivo de WIN.INI.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-105">An application sends the **WM\_WININICHANGE** message to all top-level windows after making a change to the WIN.INI file.</span></span> <span data-ttu-id="9d5a7-106">A função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) envia essa mensagem depois que um aplicativo usa a função para alterar uma configuração em WIN.INI.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-106">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function sends this message after an application uses the function to change a setting in WIN.INI.</span></span>

> [!Note]  
> <span data-ttu-id="9d5a7-107">A mensagem do **WM \_ WININICHANGE** é fornecida apenas para compatibilidade com versões anteriores do sistema.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-107">The **WM\_WININICHANGE** message is provided only for compatibility with earlier versions of the system.</span></span> <span data-ttu-id="9d5a7-108">Os aplicativos devem usar a mensagem [**\_ SETTINGCHANGE do WM**](wm-settingchange.md) .</span><span class="sxs-lookup"><span data-stu-id="9d5a7-108">Applications should use the [**WM\_SETTINGCHANGE**](wm-settingchange.md) message.</span></span>

 

<span data-ttu-id="9d5a7-109">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9d5a7-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a><span data-ttu-id="9d5a7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d5a7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d5a7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d5a7-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d5a7-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d5a7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d5a7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d5a7-114">Um ponteiro para uma cadeia de caracteres que contém o nome do parâmetro do sistema que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-114">A pointer to a string containing the name of the system parameter that was changed.</span></span> <span data-ttu-id="9d5a7-115">Por exemplo, essa cadeia de caracteres pode ser o nome de uma chave do registro ou o nome de uma seção no arquivo de Win.ini.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-115">For example, this string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="9d5a7-116">Esse parâmetro não é particularmente útil para determinar qual parâmetro do sistema foi alterado.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-116">This parameter is not particularly useful in determining which system parameter changed.</span></span> <span data-ttu-id="9d5a7-117">Por exemplo, quando a cadeia de caracteres é um nome de registro, ela normalmente indica apenas o nó folha no registro, não o caminho inteiro.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-117">For example, when the string is a registry name, it typically indicates only the leaf node in the registry, not the whole path.</span></span> <span data-ttu-id="9d5a7-118">Além disso, alguns aplicativos enviam essa mensagem com *lParam* definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-118">In addition, some applications send this message with *lParam* set to **NULL**.</span></span> <span data-ttu-id="9d5a7-119">Em geral, ao receber essa mensagem, você deve verificar e recarregar as configurações de parâmetro do sistema que são usadas pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-119">In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d5a7-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d5a7-120">Return value</span></span>

<span data-ttu-id="9d5a7-121">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9d5a7-121">Type: **LRESULT**</span></span>

<span data-ttu-id="9d5a7-122">Se você processar essa mensagem, retornará zero.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-122">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d5a7-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d5a7-123">Remarks</span></span>

<span data-ttu-id="9d5a7-124">Para enviar a mensagem do **WM \_ WININICHANGE** para todas as janelas de nível superior, use a função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) com o parâmetro *HWND* definido como **\_ transmissão de HWND**.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-124">To send the **WM\_WININICHANGE** message to all top-level windows, use the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the *hWnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="9d5a7-125">Chamadas para funções que mudam WIN.INI podem ser mapeadas para o registro em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-125">Calls to functions that change WIN.INI may be mapped to the registry instead.</span></span> <span data-ttu-id="9d5a7-126">Esse mapeamento ocorre quando WIN.INI e a seção que está sendo alterada são especificados no registro na seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="9d5a7-126">This mapping occurs when WIN.INI and the section being changed are specified in the registry under the following key:</span></span>

<span data-ttu-id="9d5a7-127">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**</span><span class="sxs-lookup"><span data-stu-id="9d5a7-127">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\IniFileMapping**</span></span>

<span data-ttu-id="9d5a7-128">A alteração no local de armazenamento não tem nenhum efeito sobre o comportamento dessa mensagem.</span><span class="sxs-lookup"><span data-stu-id="9d5a7-128">The change in the storage location has no effect on the behavior of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d5a7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d5a7-129">Requirements</span></span>



| <span data-ttu-id="9d5a7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d5a7-130">Requirement</span></span> | <span data-ttu-id="9d5a7-131">Valor</span><span class="sxs-lookup"><span data-stu-id="9d5a7-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5a7-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d5a7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5a7-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9d5a7-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9d5a7-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d5a7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5a7-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9d5a7-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9d5a7-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9d5a7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d5a7-137"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d5a7-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d5a7-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d5a7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d5a7-139">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="9d5a7-139">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 

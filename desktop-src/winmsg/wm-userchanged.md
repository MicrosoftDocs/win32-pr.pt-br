---
description: Enviado a todas as janelas após o logon ou logoff do usuário. Quando o usuário faz logon ou logoff, o sistema atualiza as configurações específicas do usuário. O sistema envia essa mensagem imediatamente após a atualização das configurações.
title: Mensagem de WM_USERCHANGED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14458bdafa0bbf4421c67db8102491db4e1fe6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922637"
---
# <a name="wm_userchanged-message"></a><span data-ttu-id="0e308-105">Mensagem do WM \_ USERchanged</span><span class="sxs-lookup"><span data-stu-id="0e308-105">WM\_USERCHANGED message</span></span>

<span data-ttu-id="0e308-106">Enviado a todas as janelas após o logon ou logoff do usuário.</span><span class="sxs-lookup"><span data-stu-id="0e308-106">Sent to all windows after the user has logged on or off.</span></span> <span data-ttu-id="0e308-107">Quando o usuário faz logon ou logoff, o sistema atualiza as configurações específicas do usuário.</span><span class="sxs-lookup"><span data-stu-id="0e308-107">When the user logs on or off, the system updates the user-specific settings.</span></span> <span data-ttu-id="0e308-108">O sistema envia essa mensagem imediatamente após a atualização das configurações.</span><span class="sxs-lookup"><span data-stu-id="0e308-108">The system sends this message immediately after updating the settings.</span></span>

<span data-ttu-id="0e308-109">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0e308-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="0e308-110">Não há suporte para essa mensagem no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0e308-110">This message is not supported as of Windows Vista.</span></span>

 


```C++
#define WM_USERCHANGED                  0x0054
```



## <a name="parameters"></a><span data-ttu-id="0e308-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e308-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e308-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e308-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e308-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="0e308-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0e308-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e308-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e308-115">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="0e308-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e308-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e308-116">Return value</span></span>

<span data-ttu-id="0e308-117">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="0e308-117">Type: **LRESULT**</span></span>

<span data-ttu-id="0e308-118">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="0e308-118">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e308-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e308-119">Requirements</span></span>



| <span data-ttu-id="0e308-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e308-120">Requirement</span></span> | <span data-ttu-id="0e308-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0e308-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e308-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e308-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0e308-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0e308-123">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0e308-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e308-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0e308-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0e308-125">None supported</span></span><br/>                                                                                |
| <span data-ttu-id="0e308-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e308-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e308-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e308-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e308-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e308-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e308-129">Visão geral do Windows</span><span class="sxs-lookup"><span data-stu-id="0e308-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 

---
description: Enviado a um aplicativo quando o sistema operacional está prestes a alterar o IME atual. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: Mensagem de WM_IME_SELECT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758133"
---
# <a name="wm_ime_select-message"></a><span data-ttu-id="72075-104">\_Selecionar mensagem do IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="72075-104">WM\_IME\_SELECT message</span></span>

<span data-ttu-id="72075-105">Enviado a um aplicativo quando o sistema operacional está prestes a alterar o IME atual.</span><span class="sxs-lookup"><span data-stu-id="72075-105">Sent to an application when the operating system is about to change the current IME.</span></span> <span data-ttu-id="72075-106">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="72075-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="72075-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72075-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72075-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="72075-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="72075-109">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="72075-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="72075-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72075-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72075-111">Indicador de seleção.</span><span class="sxs-lookup"><span data-stu-id="72075-111">Selection indicator.</span></span> <span data-ttu-id="72075-112">Esse parâmetro especifica **true** se o IME indicado for selecionado.</span><span class="sxs-lookup"><span data-stu-id="72075-112">This parameter specifies **TRUE** if the indicated IME is selected.</span></span> <span data-ttu-id="72075-113">O parâmetro será definido como **false** se o IME especificado não estiver mais selecionado.</span><span class="sxs-lookup"><span data-stu-id="72075-113">The parameter is set to **FALSE** if the specified IME is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="72075-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72075-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="72075-115">Identificador de localidade de entrada associado ao IME.</span><span class="sxs-lookup"><span data-stu-id="72075-115">Input locale identifier associated with the IME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72075-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72075-116">Return value</span></span>

<span data-ttu-id="72075-117">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="72075-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72075-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="72075-118">Remarks</span></span>

<span data-ttu-id="72075-119">Um aplicativo que criou uma janela IME deve passar essa mensagem para essa janela para que ela possa recuperar o identificador de layout do teclado para o IME selecionado recentemente.</span><span class="sxs-lookup"><span data-stu-id="72075-119">An application that has created an IME window should pass this message to that window so that it can retrieve the keyboard layout handle to the newly selected IME.</span></span>

<span data-ttu-id="72075-120">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  processa essa mensagem passando as informações para a janela padrão do IME.</span><span class="sxs-lookup"><span data-stu-id="72075-120">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing the information to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="72075-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72075-121">Requirements</span></span>



| <span data-ttu-id="72075-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="72075-122">Requirement</span></span> | <span data-ttu-id="72075-123">Valor</span><span class="sxs-lookup"><span data-stu-id="72075-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72075-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72075-124">Minimum supported client</span></span><br/> | <span data-ttu-id="72075-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="72075-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="72075-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72075-126">Minimum supported server</span></span><br/> | <span data-ttu-id="72075-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="72075-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="72075-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="72075-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="72075-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72075-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72075-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="72075-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72075-131">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="72075-131">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="72075-132">Mensagens do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="72075-132">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 

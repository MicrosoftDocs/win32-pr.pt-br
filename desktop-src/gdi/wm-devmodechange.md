---
description: A mensagem do WM \_ DEVMODECHANGE é enviada para todas as janelas de nível superior sempre que o usuário altera as configurações do modo de dispositivo.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: Mensagem de WM_DEVMODECHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968085"
---
# <a name="wm_devmodechange-message"></a><span data-ttu-id="8adff-103">Mensagem do WM \_ DEVMODECHANGE</span><span class="sxs-lookup"><span data-stu-id="8adff-103">WM\_DEVMODECHANGE message</span></span>

<span data-ttu-id="8adff-104">A mensagem do **WM \_ DEVMODECHANGE** é enviada para todas as janelas de nível superior sempre que o usuário altera as configurações do modo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8adff-104">The **WM\_DEVMODECHANGE** message is sent to all top-level windows whenever the user changes device-mode settings.</span></span>

<span data-ttu-id="8adff-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8adff-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="8adff-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8adff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8adff-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8adff-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8adff-108">Um identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="8adff-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="8adff-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="8adff-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="8adff-110">DEVMODECHANGE do WM \_</span><span class="sxs-lookup"><span data-stu-id="8adff-110">WM\_DEVMODECHANGE</span></span>

</dd> <dt>

<span data-ttu-id="8adff-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8adff-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8adff-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="8adff-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8adff-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8adff-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8adff-114">Um ponteiro para uma cadeia de caracteres que especifica o nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8adff-114">A pointer to a string that specifies the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8adff-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8adff-115">Return value</span></span>

<span data-ttu-id="8adff-116">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="8adff-116">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="8adff-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8adff-117">Remarks</span></span>

<span data-ttu-id="8adff-118">Esta mensagem não pode ser enviada diretamente a uma janela.</span><span class="sxs-lookup"><span data-stu-id="8adff-118">This message cannot be sent directly to a window.</span></span> <span data-ttu-id="8adff-119">Para enviar a mensagem do **WM \_ DEVMODECHANGE** para todas as janelas de nível superior, use a função [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) com o parâmetro *HWND* definido como a \_ difusão HWND.</span><span class="sxs-lookup"><span data-stu-id="8adff-119">To send the **WM\_DEVMODECHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hWnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="8adff-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8adff-120">Requirements</span></span>



| <span data-ttu-id="8adff-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8adff-121">Requirement</span></span> | <span data-ttu-id="8adff-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8adff-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8adff-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8adff-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8adff-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8adff-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8adff-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8adff-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8adff-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8adff-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8adff-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8adff-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8adff-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8adff-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8adff-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8adff-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8adff-130">Visão geral de contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="8adff-130">Device Contexts Overview</span></span>](device-contexts.md)
</dt> <dt>

[<span data-ttu-id="8adff-131">Mensagens de contexto do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8adff-131">Device Context Messages</span></span>](device-context-messages.md)
</dt> </dl>

 

 

---
description: Um aplicativo envia a mensagem do WM \_ FONTCHANGE para todas as janelas de nível superior no sistema após a alteração do pool de recursos de fonte.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: Mensagem de WM_FONTCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b40650f0077ed854b87a6fd10e1dae610f0c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968084"
---
# <a name="wm_fontchange-message"></a><span data-ttu-id="535bc-103">Mensagem do WM \_ FONTCHANGE</span><span class="sxs-lookup"><span data-stu-id="535bc-103">WM\_FONTCHANGE message</span></span>

<span data-ttu-id="535bc-104">Um aplicativo envia a mensagem do **WM \_ FONTCHANGE** para todas as janelas de nível superior no sistema após a alteração do pool de recursos de fonte.</span><span class="sxs-lookup"><span data-stu-id="535bc-104">An application sends the **WM\_FONTCHANGE** message to all top-level windows in the system after changing the pool of font resources.</span></span>

<span data-ttu-id="535bc-105">Para enviar essa mensagem, chame a função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="535bc-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
```



## <a name="parameters"></a><span data-ttu-id="535bc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="535bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="535bc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="535bc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="535bc-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="535bc-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="535bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="535bc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="535bc-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="535bc-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="535bc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="535bc-111">Remarks</span></span>

<span data-ttu-id="535bc-112">Um aplicativo que adiciona ou remove fontes do sistema (por exemplo, usando a função [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) ou [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) ) deve enviar essa mensagem para todas as janelas de nível superior.</span><span class="sxs-lookup"><span data-stu-id="535bc-112">An application that adds or removes fonts from the system (for example, by using the [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) or [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) function) should send this message to all top-level windows.</span></span>

<span data-ttu-id="535bc-113">Para enviar a mensagem do **WM \_ FONTCHANGE** para todas as janelas de nível superior, um aplicativo pode chamar a função **SendMessage** com o parâmetro *HWND* definido como broadcast de HWND \_ .</span><span class="sxs-lookup"><span data-stu-id="535bc-113">To send the **WM\_FONTCHANGE** message to all top-level windows, an application can call the **SendMessage** function with the *hwnd* parameter set to HWND\_BROADCAST.</span></span>

## <a name="requirements"></a><span data-ttu-id="535bc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="535bc-114">Requirements</span></span>



| <span data-ttu-id="535bc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="535bc-115">Requirement</span></span> | <span data-ttu-id="535bc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="535bc-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="535bc-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="535bc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="535bc-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="535bc-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="535bc-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="535bc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="535bc-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="535bc-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="535bc-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="535bc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="535bc-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="535bc-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="535bc-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="535bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="535bc-124">Visão geral de fontes e texto</span><span class="sxs-lookup"><span data-stu-id="535bc-124">Fonts and Text Overview</span></span>](fonts-and-text.md)
</dt> <dt>

[<span data-ttu-id="535bc-125">Mensagens de fonte e texto</span><span class="sxs-lookup"><span data-stu-id="535bc-125">Font and Text Messages</span></span>](font-and-text-messages.md)
</dt> <dt>

[<span data-ttu-id="535bc-126">**AddFontResource**</span><span class="sxs-lookup"><span data-stu-id="535bc-126">**AddFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[<span data-ttu-id="535bc-127">**RemoveFontResource**</span><span class="sxs-lookup"><span data-stu-id="535bc-127">**RemoveFontResource**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 

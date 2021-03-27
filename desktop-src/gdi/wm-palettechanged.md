---
description: A \_ mensagem da paletachanged do WM é enviada a todas as janelas de nível superior e sobrepostas após a janela com o foco do teclado ter percebido sua paleta lógica, alterando assim a paleta do sistema.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: Mensagem de WM_PALETTECHANGED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661962"
---
# <a name="wm_palettechanged-message"></a><span data-ttu-id="13d72-103">\_Mensagem da paletachanged do WM</span><span class="sxs-lookup"><span data-stu-id="13d72-103">WM\_PALETTECHANGED message</span></span>

<span data-ttu-id="13d72-104">A mensagem da **\_ Paletachanged do WM** é enviada a todas as janelas de nível superior e sobrepostas após a janela com o foco do teclado ter percebido sua paleta lógica, alterando assim a paleta do sistema.</span><span class="sxs-lookup"><span data-stu-id="13d72-104">The **WM\_PALETTECHANGED** message is sent to all top-level and overlapped windows after the window with the keyboard focus has realized its logical palette, thereby changing the system palette.</span></span> <span data-ttu-id="13d72-105">Essa mensagem habilita uma janela que usa uma paleta de cores, mas não tem o foco do teclado para compreender sua paleta lógica e atualizar sua área do cliente.</span><span class="sxs-lookup"><span data-stu-id="13d72-105">This message enables a window that uses a color palette but does not have the keyboard focus to realize its logical palette and update its client area.</span></span>

<span data-ttu-id="13d72-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="13d72-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="13d72-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13d72-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13d72-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13d72-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13d72-109">Um identificador para a janela que fez com que a paleta do sistema fosse alterada.</span><span class="sxs-lookup"><span data-stu-id="13d72-109">A handle to the window that caused the system palette to change.</span></span>

</dd> <dt>

<span data-ttu-id="13d72-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13d72-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13d72-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="13d72-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13d72-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="13d72-112">Remarks</span></span>

<span data-ttu-id="13d72-113">Essa mensagem deve ser enviada a todas as janelas de nível superior e sobrepostas, incluindo aquela que alterou a paleta do sistema.</span><span class="sxs-lookup"><span data-stu-id="13d72-113">This message must be sent to all top-level and overlapped windows, including the one that changed the system palette.</span></span> <span data-ttu-id="13d72-114">Se qualquer janela filho usar uma paleta de cores, essa mensagem também deverá ser passada para elas.</span><span class="sxs-lookup"><span data-stu-id="13d72-114">If any child windows use a color palette, this message must be passed on to them as well.</span></span>

<span data-ttu-id="13d72-115">Para evitar a criação de um loop infinito, uma janela que recebe essa mensagem não deve perceber sua paleta, a menos que ela determine que *wParam* não contém seu próprio identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="13d72-115">To avoid creating an infinite loop, a window that receives this message must not realize its palette, unless it determines that *wParam* does not contain its own window handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d72-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13d72-116">Requirements</span></span>



| <span data-ttu-id="13d72-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="13d72-117">Requirement</span></span> | <span data-ttu-id="13d72-118">Valor</span><span class="sxs-lookup"><span data-stu-id="13d72-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13d72-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13d72-119">Minimum supported client</span></span><br/> | <span data-ttu-id="13d72-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="13d72-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="13d72-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13d72-121">Minimum supported server</span></span><br/> | <span data-ttu-id="13d72-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="13d72-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="13d72-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="13d72-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="13d72-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13d72-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d72-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="13d72-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d72-126">Visão geral das cores</span><span class="sxs-lookup"><span data-stu-id="13d72-126">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="13d72-127">Mensagens de cores</span><span class="sxs-lookup"><span data-stu-id="13d72-127">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="13d72-128">**PALETTEISCHANGING do WM \_**</span><span class="sxs-lookup"><span data-stu-id="13d72-128">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> <dt>

[<span data-ttu-id="13d72-129">**QUERYNEWPALETTE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="13d72-129">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 

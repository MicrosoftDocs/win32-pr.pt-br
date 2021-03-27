---
description: A mensagem do WM \_ QUERYNEWPALETTE informa uma janela de que está prestes a receber o foco do teclado, dando à janela a oportunidade de perceber sua paleta lógica quando recebe o foco.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: Mensagem de WM_QUERYNEWPALETTE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967851"
---
# <a name="wm_querynewpalette-message"></a><span data-ttu-id="a1d84-103">Mensagem do WM \_ QUERYNEWPALETTE</span><span class="sxs-lookup"><span data-stu-id="a1d84-103">WM\_QUERYNEWPALETTE message</span></span>

<span data-ttu-id="a1d84-104">A mensagem do **WM \_ QUERYNEWPALETTE** informa uma janela de que está prestes a receber o foco do teclado, dando à janela a oportunidade de perceber sua paleta lógica quando recebe o foco.</span><span class="sxs-lookup"><span data-stu-id="a1d84-104">The **WM\_QUERYNEWPALETTE** message informs a window that it is about to receive the keyboard focus, giving the window the opportunity to realize its logical palette when it receives the focus.</span></span>

<span data-ttu-id="a1d84-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a1d84-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="a1d84-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1d84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1d84-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1d84-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1d84-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="a1d84-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a1d84-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1d84-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1d84-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="a1d84-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1d84-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1d84-111">Return value</span></span>

<span data-ttu-id="a1d84-112">Se a janela perceber sua paleta lógica, ela deverá retornar **true**; caso contrário, ele deve retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="a1d84-112">If the window realizes its logical palette, it must return **TRUE**; otherwise, it must return **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d84-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1d84-113">Requirements</span></span>



| <span data-ttu-id="a1d84-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1d84-114">Requirement</span></span> | <span data-ttu-id="a1d84-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a1d84-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d84-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1d84-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a1d84-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a1d84-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a1d84-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1d84-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a1d84-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a1d84-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a1d84-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a1d84-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1d84-121"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1d84-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1d84-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1d84-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d84-123">Visão geral das cores</span><span class="sxs-lookup"><span data-stu-id="a1d84-123">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="a1d84-124">Mensagens de cores</span><span class="sxs-lookup"><span data-stu-id="a1d84-124">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="a1d84-125">**paleta do WMchanged \_**</span><span class="sxs-lookup"><span data-stu-id="a1d84-125">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="a1d84-126">**PALETTEISCHANGING do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a1d84-126">**WM\_PALETTEISCHANGING**</span></span>](wm-paletteischanging.md)
</dt> </dl>

 

 

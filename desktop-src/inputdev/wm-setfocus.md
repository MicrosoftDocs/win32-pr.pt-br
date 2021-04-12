---
title: Mensagem de WM_SETFOCUS (WinUser. h)
description: Enviado a uma janela depois de ter obtido o foco do teclado.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- Entrada de mouse e teclado de mensagem WM_SETFOCUS
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b304d7f7739ce551c1efc6a1d33a934c48dc8b4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455827"
---
# <a name="wm_setfocus-message"></a><span data-ttu-id="363d8-104">Mensagem do WM \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="363d8-104">WM\_SETFOCUS message</span></span>

<span data-ttu-id="363d8-105">Enviado a uma janela depois de ter obtido o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="363d8-105">Sent to a window after it has gained the keyboard focus.</span></span>


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a><span data-ttu-id="363d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="363d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="363d8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="363d8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="363d8-108">Um identificador para a janela que perdeu o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="363d8-108">A handle to the window that has lost the keyboard focus.</span></span> <span data-ttu-id="363d8-109">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="363d8-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="363d8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="363d8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="363d8-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="363d8-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="363d8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="363d8-112">Return value</span></span>

<span data-ttu-id="363d8-113">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="363d8-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="363d8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="363d8-114">Remarks</span></span>

<span data-ttu-id="363d8-115">Para exibir um cursor, um aplicativo deve chamar as funções de cursor apropriadas quando receber a mensagem do **WM \_ SETFOCUS** .</span><span class="sxs-lookup"><span data-stu-id="363d8-115">To display a caret, an application should call the appropriate caret functions when it receives the **WM\_SETFOCUS** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="363d8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="363d8-116">Requirements</span></span>



| <span data-ttu-id="363d8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="363d8-117">Requirement</span></span> | <span data-ttu-id="363d8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="363d8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="363d8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="363d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="363d8-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="363d8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="363d8-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="363d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="363d8-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="363d8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="363d8-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="363d8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="363d8-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="363d8-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="363d8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="363d8-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="363d8-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="363d8-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="363d8-127">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="363d8-127">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="363d8-128">**KILLFOCUS do WM \_**</span><span class="sxs-lookup"><span data-stu-id="363d8-128">**WM\_KILLFOCUS**</span></span>](wm-killfocus.md)
</dt> <dt>

<span data-ttu-id="363d8-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="363d8-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="363d8-130">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="363d8-130">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 


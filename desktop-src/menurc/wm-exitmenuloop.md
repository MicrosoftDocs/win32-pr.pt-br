---
title: Mensagem de WM_EXITMENULOOP (WinUser. h)
description: Notifica o procedimento de janela principal de um aplicativo que um loop modal de menu foi encerrado.
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- WM_EXITMENULOOP menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8440e1a255968eb3e1607b5d54375900f7b5de16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644701"
---
# <a name="wm_exitmenuloop-message"></a><span data-ttu-id="2711d-104">Mensagem do WM \_ EXITMENULOOP</span><span class="sxs-lookup"><span data-stu-id="2711d-104">WM\_EXITMENULOOP message</span></span>

<span data-ttu-id="2711d-105">Notifica o procedimento de janela principal de um aplicativo que um loop modal de menu foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="2711d-105">Notifies an application's main window procedure that a menu modal loop has been exited.</span></span>


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a><span data-ttu-id="2711d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2711d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2711d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2711d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2711d-108">Especifica se o menu é um menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="2711d-108">Specifies whether the menu is a shortcut menu.</span></span> <span data-ttu-id="2711d-109">Esse parâmetro tem um valor de **true** se for um menu de atalho, **false** se não for.</span><span class="sxs-lookup"><span data-stu-id="2711d-109">This parameter has a value of **TRUE** if it is a shortcut menu, **FALSE** if it is not.</span></span>

</dd> <dt>

<span data-ttu-id="2711d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2711d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2711d-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="2711d-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2711d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2711d-112">Return value</span></span>

<span data-ttu-id="2711d-113">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="2711d-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="2711d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2711d-114">Remarks</span></span>

<span data-ttu-id="2711d-115">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna zero.</span><span class="sxs-lookup"><span data-stu-id="2711d-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2711d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2711d-116">Requirements</span></span>



| <span data-ttu-id="2711d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2711d-117">Requirement</span></span> | <span data-ttu-id="2711d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2711d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2711d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2711d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2711d-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2711d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2711d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2711d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2711d-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2711d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2711d-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2711d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2711d-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2711d-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2711d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2711d-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="2711d-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2711d-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2711d-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2711d-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2711d-128">**ENTERMENULOOP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2711d-128">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
</dt> <dt>

<span data-ttu-id="2711d-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="2711d-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2711d-130">Menus</span><span class="sxs-lookup"><span data-stu-id="2711d-130">Menus</span></span>](menus.md)
</dt> </dl>

 


---
title: Mensagem de WM_MENUCOMMAND (WinUser. h)
description: Enviado quando o usuário faz uma seleção de um menu.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369926"
---
# <a name="wm_menucommand-message"></a><span data-ttu-id="6e7ac-104">Mensagem do WM \_ MENUCOMMAND</span><span class="sxs-lookup"><span data-stu-id="6e7ac-104">WM\_MENUCOMMAND message</span></span>

<span data-ttu-id="6e7ac-105">Enviado quando o usuário faz uma seleção de um menu.</span><span class="sxs-lookup"><span data-stu-id="6e7ac-105">Sent when the user makes a selection from a menu.</span></span>


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a><span data-ttu-id="6e7ac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e7ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e7ac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e7ac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e7ac-108">O índice de base zero do item selecionado.</span><span class="sxs-lookup"><span data-stu-id="6e7ac-108">The zero-based index of the item selected.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ac-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e7ac-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e7ac-110">Um identificador para o menu do item selecionado.</span><span class="sxs-lookup"><span data-stu-id="6e7ac-110">A handle to the menu for the item selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e7ac-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e7ac-111">Remarks</span></span>

<span data-ttu-id="6e7ac-112">A mensagem do **WM \_ MENUCOMMAND** fornece um identificador para o menu para que você possa acessar os dados do menu na estrutura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) e também fornece o índice do item selecionado, que normalmente é o que os aplicativos precisam.</span><span class="sxs-lookup"><span data-stu-id="6e7ac-112">The **WM\_MENUCOMMAND** message gives you a handle to the menu so you can access the menu data in the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure and also gives you the index of the selected item, which is typically what applications need.</span></span> <span data-ttu-id="6e7ac-113">Por outro lado, a mensagem de [**\_ comando do WM**](wm-command.md) fornece o identificador do item de menu.</span><span class="sxs-lookup"><span data-stu-id="6e7ac-113">In contrast, the [**WM\_COMMAND**](wm-command.md) message gives you the menu item identifier.</span></span>

<span data-ttu-id="6e7ac-114">A mensagem do **WM \_ MENUCOMMAND** é enviada somente para menus que são definidos com o sinalizador de **MNS \_ NOTIFYBYPOS** definido no membro **dwStyle** da estrutura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) .</span><span class="sxs-lookup"><span data-stu-id="6e7ac-114">The **WM\_MENUCOMMAND** message is sent only for menus that are defined with the **MNS\_NOTIFYBYPOS** flag set in the **dwStyle** member of the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e7ac-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e7ac-115">Requirements</span></span>



| <span data-ttu-id="6e7ac-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e7ac-116">Requirement</span></span> | <span data-ttu-id="6e7ac-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6e7ac-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e7ac-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e7ac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6e7ac-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e7ac-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6e7ac-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e7ac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6e7ac-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e7ac-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6e7ac-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6e7ac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e7ac-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e7ac-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e7ac-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e7ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e7ac-125">Visão geral dos menus</span><span class="sxs-lookup"><span data-stu-id="6e7ac-125">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 






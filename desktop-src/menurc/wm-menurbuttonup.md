---
title: Mensagem de WM_MENURBUTTONUP (WinUser. h)
description: Enviado quando o usuário libera o botão direito do mouse enquanto o cursor está em um item de menu.
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- WM_MENURBUTTONUP menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295918"
---
# <a name="wm_menurbuttonup-message"></a><span data-ttu-id="3844e-104">Mensagem do WM \_ MENURBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="3844e-104">WM\_MENURBUTTONUP message</span></span>

<span data-ttu-id="3844e-105">Enviado quando o usuário libera o botão direito do mouse enquanto o cursor está em um item de menu.</span><span class="sxs-lookup"><span data-stu-id="3844e-105">Sent when the user releases the right mouse button while the cursor is on a menu item.</span></span>


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a><span data-ttu-id="3844e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3844e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3844e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3844e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3844e-108">O índice de base zero do item de menu no qual o botão direito do mouse foi liberado.</span><span class="sxs-lookup"><span data-stu-id="3844e-108">The zero-based index of the menu item on which the right mouse button was released.</span></span>

</dd> <dt>

<span data-ttu-id="3844e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3844e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3844e-110">Um identificador para o menu que contém o item.</span><span class="sxs-lookup"><span data-stu-id="3844e-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3844e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3844e-111">Remarks</span></span>

<span data-ttu-id="3844e-112">A mensagem do **WM \_ MENURBUTTONUP** permite que os aplicativos forneçam um menu contextual também conhecido como menu de atalho para o item de menu especificado nesta mensagem.</span><span class="sxs-lookup"><span data-stu-id="3844e-112">The **WM\_MENURBUTTONUP** message allows applications to provide a context-sensitive menu also known as a shortcut menu for the menu item specified in this message.</span></span> <span data-ttu-id="3844e-113">Para exibir um menu sensível ao contexto para um item de menu, chame a função [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) com o **TPM \_ recurse**.</span><span class="sxs-lookup"><span data-stu-id="3844e-113">To display a context-sensitive menu for a menu item, call the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function with **TPM\_RECURSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3844e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3844e-114">Requirements</span></span>



| <span data-ttu-id="3844e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3844e-115">Requirement</span></span> | <span data-ttu-id="3844e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3844e-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3844e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3844e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3844e-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3844e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3844e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3844e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3844e-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3844e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3844e-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3844e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3844e-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3844e-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3844e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3844e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3844e-124">Visão geral dos menus</span><span class="sxs-lookup"><span data-stu-id="3844e-124">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 






---
title: Mensagem de WM_ENTERMENULOOP (WinUser. h)
description: Notifica o procedimento de janela principal de um aplicativo que um loop modal de menu foi inserido.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b325719c428dc7310503320b53f3a5f96182e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787709"
---
# <a name="wm_entermenuloop-message"></a><span data-ttu-id="9e98c-104">Mensagem do WM \_ ENTERMENULOOP</span><span class="sxs-lookup"><span data-stu-id="9e98c-104">WM\_ENTERMENULOOP message</span></span>

<span data-ttu-id="9e98c-105">Notifica o procedimento de janela principal de um aplicativo que um loop modal de menu foi inserido.</span><span class="sxs-lookup"><span data-stu-id="9e98c-105">Notifies an application's main window procedure that a menu modal loop has been entered.</span></span>


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a><span data-ttu-id="9e98c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e98c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e98c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e98c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e98c-108">Especifica se o menu de janela foi inserido usando a função [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) .</span><span class="sxs-lookup"><span data-stu-id="9e98c-108">Specifies whether the window menu was entered using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function.</span></span> <span data-ttu-id="9e98c-109">Esse parâmetro terá um valor **true** se o menu Window tiver sido inserido usando **TrackPopupMenu** e **false** se não tiver sido.</span><span class="sxs-lookup"><span data-stu-id="9e98c-109">This parameter has a value of **TRUE** if the window menu was entered using **TrackPopupMenu**, and **FALSE** if it was not.</span></span>

</dd> <dt>

<span data-ttu-id="9e98c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e98c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e98c-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="9e98c-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e98c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e98c-112">Return value</span></span>

<span data-ttu-id="9e98c-113">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="9e98c-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e98c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e98c-114">Remarks</span></span>

<span data-ttu-id="9e98c-115">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna zero.</span><span class="sxs-lookup"><span data-stu-id="9e98c-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e98c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e98c-116">Requirements</span></span>



| <span data-ttu-id="9e98c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e98c-117">Requirement</span></span> | <span data-ttu-id="9e98c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9e98c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e98c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e98c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e98c-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e98c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9e98c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e98c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9e98c-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e98c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9e98c-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9e98c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e98c-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e98c-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e98c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e98c-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e98c-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="9e98c-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9e98c-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9e98c-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="9e98c-128">**EXITMENULOOP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="9e98c-128">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
</dt> <dt>

<span data-ttu-id="9e98c-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="9e98c-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9e98c-130">Menus</span><span class="sxs-lookup"><span data-stu-id="9e98c-130">Menus</span></span>](menus.md)
</dt> </dl>

 


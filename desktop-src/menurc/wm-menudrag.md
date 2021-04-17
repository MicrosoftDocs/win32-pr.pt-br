---
title: Mensagem de WM_MENUDRAG (WinUser. h)
description: Enviado ao proprietário de um menu de arrastar e soltar quando o usuário arrasta um item de menu.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67e83c41576a716d292187df4cb08fa803271c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761670"
---
# <a name="wm_menudrag-message"></a><span data-ttu-id="c1cc5-104">Mensagem do WM \_ MENUDRAG</span><span class="sxs-lookup"><span data-stu-id="c1cc5-104">WM\_MENUDRAG message</span></span>

<span data-ttu-id="c1cc5-105">Enviado ao proprietário de um menu de arrastar e soltar quando o usuário arrasta um item de menu.</span><span class="sxs-lookup"><span data-stu-id="c1cc5-105">Sent to the owner of a drag-and-drop menu when the user drags a menu item.</span></span>


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a><span data-ttu-id="c1cc5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1cc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1cc5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1cc5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1cc5-108">A posição do item no qual a operação de arrastar começou.</span><span class="sxs-lookup"><span data-stu-id="c1cc5-108">The position of the item where the drag operation began.</span></span>

</dd> <dt>

<span data-ttu-id="c1cc5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1cc5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1cc5-110">Um identificador para o menu que contém o item.</span><span class="sxs-lookup"><span data-stu-id="c1cc5-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1cc5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1cc5-111">Return value</span></span>

<span data-ttu-id="c1cc5-112">O aplicativo deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1cc5-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="c1cc5-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c1cc5-113">Return code/value</span></span>                                                                                                                                   | <span data-ttu-id="c1cc5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1cc5-114">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1cc5-115"><dt>**MND \_ CONTINUAR**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c1cc5-115"><dt>**MND\_CONTINUE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="c1cc5-116">O menu deve permanecer ativo.</span><span class="sxs-lookup"><span data-stu-id="c1cc5-116">Menu should remain active.</span></span> <span data-ttu-id="c1cc5-117">Se o mouse for liberado, ele deverá ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="c1cc5-117">If the mouse is released, it should be ignored.</span></span><br/> |
| <dl> <span data-ttu-id="c1cc5-118"><dt>**MND \_ Endmenu**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c1cc5-118"><dt>**MND\_ENDMENU**</dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="c1cc5-119">O menu deve ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="c1cc5-119">Menu should be ended.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="c1cc5-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1cc5-120">Remarks</span></span>

<span data-ttu-id="c1cc5-121">O aplicativo pode chamar a função [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) em resposta a esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="c1cc5-121">The application can call the [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) function in response to this message.</span></span>

<span data-ttu-id="c1cc5-122">Para criar um menu do tipo "arrastar e soltar", chame [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) com **MNS \_ DRAGDROP**.</span><span class="sxs-lookup"><span data-stu-id="c1cc5-122">To create a drag-and-drop menu, call [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) with **MNS\_DRAGDROP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1cc5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1cc5-123">Requirements</span></span>



| <span data-ttu-id="c1cc5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1cc5-124">Requirement</span></span> | <span data-ttu-id="c1cc5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c1cc5-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cc5-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1cc5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c1cc5-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c1cc5-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c1cc5-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1cc5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c1cc5-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c1cc5-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c1cc5-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c1cc5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1cc5-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1cc5-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1cc5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1cc5-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1cc5-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c1cc5-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c1cc5-134">**SetMenuInfo**</span><span class="sxs-lookup"><span data-stu-id="c1cc5-134">**SetMenuInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

<span data-ttu-id="c1cc5-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c1cc5-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c1cc5-136">Menus</span><span class="sxs-lookup"><span data-stu-id="c1cc5-136">Menus</span></span>](menus.md)
</dt> </dl>

 


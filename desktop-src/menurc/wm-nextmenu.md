---
title: Mensagem de WM_NEXTMENU (WinUser. h)
description: Enviado a um aplicativo quando a tecla de seta para a direita ou para a esquerda é usada para alternar entre a barra de menus e o menu do sistema.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919199"
---
# <a name="wm_nextmenu-message"></a><span data-ttu-id="679f5-104">Mensagem do WM \_ NEXTMENU</span><span class="sxs-lookup"><span data-stu-id="679f5-104">WM\_NEXTMENU message</span></span>

<span data-ttu-id="679f5-105">Enviado a um aplicativo quando a tecla de seta para a direita ou para a esquerda é usada para alternar entre a barra de menus e o menu do sistema.</span><span class="sxs-lookup"><span data-stu-id="679f5-105">Sent to an application when the right or left arrow key is used to switch between the menu bar and the system menu.</span></span>


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a><span data-ttu-id="679f5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="679f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="679f5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="679f5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="679f5-108">O código de chave virtual da chave.</span><span class="sxs-lookup"><span data-stu-id="679f5-108">The virtual-key code of the key.</span></span> <span data-ttu-id="679f5-109">Consulte [**códigos de chave virtual**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="679f5-109">See [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="679f5-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="679f5-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="679f5-111">Um ponteiro para uma estrutura [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) que contém informações sobre o menu a ser ativado.</span><span class="sxs-lookup"><span data-stu-id="679f5-111">A pointer to a [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) structure that contains information about the menu to be activated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="679f5-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="679f5-112">Remarks</span></span>

<span data-ttu-id="679f5-113">Ao responder a essa mensagem, o aplicativo pode especificar o menu para alternar para o membro **hmenuNext** de [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) e a janela para receber as mensagens de notificação de menu no membro **hWndNext** da estrutura **MDINEXTMENU** .</span><span class="sxs-lookup"><span data-stu-id="679f5-113">In responding to this message, the application can specify the menu to switch to in the **hmenuNext** member of [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) and the window to receive the menu notification messages in the **hwndNext** member of the **MDINEXTMENU** structure.</span></span> <span data-ttu-id="679f5-114">Você deve definir ambos os membros para que as alterações entrem em vigor (elas são inicialmente **nulas**).</span><span class="sxs-lookup"><span data-stu-id="679f5-114">You must set both members for the changes to take effect (they are initially **NULL**).</span></span>

## <a name="requirements"></a><span data-ttu-id="679f5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="679f5-115">Requirements</span></span>



| <span data-ttu-id="679f5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="679f5-116">Requirement</span></span> | <span data-ttu-id="679f5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="679f5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="679f5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="679f5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="679f5-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="679f5-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="679f5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="679f5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="679f5-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="679f5-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="679f5-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="679f5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="679f5-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="679f5-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="679f5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="679f5-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="679f5-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="679f5-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="679f5-126">**MDINEXTMENU**</span><span class="sxs-lookup"><span data-stu-id="679f5-126">**MDINEXTMENU**</span></span>](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

<span data-ttu-id="679f5-127">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="679f5-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="679f5-128">Menus</span><span class="sxs-lookup"><span data-stu-id="679f5-128">Menus</span></span>](menus.md)
</dt> </dl>

 


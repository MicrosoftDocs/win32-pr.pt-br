---
description: Um aplicativo envia a mensagem do WM \_ MDIREFRESHMENU para uma janela de cliente MDI (interface de vários documentos) para atualizar o menu janela da janela do quadro MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: Mensagem de WM_MDIREFRESHMENU (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4eafa7b84dc9389e57d379a30019505e85fb602
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759270"
---
# <a name="wm_mdirefreshmenu-message"></a><span data-ttu-id="9a6b8-103">Mensagem do WM \_ MDIREFRESHMENU</span><span class="sxs-lookup"><span data-stu-id="9a6b8-103">WM\_MDIREFRESHMENU message</span></span>

<span data-ttu-id="9a6b8-104">Um aplicativo envia a mensagem do **WM \_ MDIREFRESHMENU** para uma janela de cliente MDI (interface de vários documentos) para atualizar o menu janela da janela do quadro MDI.</span><span class="sxs-lookup"><span data-stu-id="9a6b8-104">An application sends the **WM\_MDIREFRESHMENU** message to a multiple-document interface (MDI) client window to refresh the window menu of the MDI frame window.</span></span>


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a><span data-ttu-id="9a6b8-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a6b8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a6b8-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a6b8-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a6b8-107">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9a6b8-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9a6b8-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a6b8-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a6b8-109">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9a6b8-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a6b8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a6b8-110">Return value</span></span>

<span data-ttu-id="9a6b8-111">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="9a6b8-111">Type: **HMENU**</span></span>

<span data-ttu-id="9a6b8-112">Se a mensagem tiver sucesso, o valor de retorno será o identificador para o menu de janela do quadro.</span><span class="sxs-lookup"><span data-stu-id="9a6b8-112">If the message succeeds, the return value is the handle to the frame window menu.</span></span>

<span data-ttu-id="9a6b8-113">Se a mensagem falhar, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="9a6b8-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a6b8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a6b8-114">Remarks</span></span>

<span data-ttu-id="9a6b8-115">Depois de enviar essa mensagem, um aplicativo deve chamar a função [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) para atualizar a barra de menus.</span><span class="sxs-lookup"><span data-stu-id="9a6b8-115">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a6b8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a6b8-116">Requirements</span></span>



| <span data-ttu-id="9a6b8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a6b8-117">Requirement</span></span> | <span data-ttu-id="9a6b8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9a6b8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6b8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a6b8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9a6b8-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a6b8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9a6b8-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a6b8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9a6b8-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a6b8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9a6b8-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9a6b8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a6b8-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a6b8-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a6b8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a6b8-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="9a6b8-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="9a6b8-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9a6b8-127">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="9a6b8-127">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="9a6b8-128">**MDISETMENU do WM \_**</span><span class="sxs-lookup"><span data-stu-id="9a6b8-128">**WM\_MDISETMENU**</span></span>](wm-mdisetmenu.md)
</dt> <dt>

<span data-ttu-id="9a6b8-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="9a6b8-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9a6b8-130">Interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="9a6b8-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 

---
title: Mensagem de WM_DDE_UNADVISE (DDE. h)
description: Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de aviso de DDE do WM \_ \_ para informar a um aplicativo de servidor DDE que o item especificado ou um formato de área de transferência específico para o item não deve mais ser atualizado.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- Troca de dados de mensagem WM_DDE_UNADVISE
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455676"
---
# <a name="wm_dde_unadvise-message"></a><span data-ttu-id="69d4f-104">Mensagem de aviso de \_ DDE do WM \_</span><span class="sxs-lookup"><span data-stu-id="69d4f-104">WM\_DDE\_UNADVISE message</span></span>

<span data-ttu-id="69d4f-105">Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de **\_ \_ aviso de DDE do WM** para informar a um aplicativo de servidor DDE que o item especificado ou um formato de área de transferência específico para o item não deve mais ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="69d4f-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_UNADVISE** message to inform a DDE server application that the specified item or a particular clipboard format for the item should no longer be updated.</span></span> <span data-ttu-id="69d4f-106">Isso encerra o link de dados quente ou ativo para o item especificado.</span><span class="sxs-lookup"><span data-stu-id="69d4f-106">This terminates the warm or hot data link for the specified item.</span></span>

<span data-ttu-id="69d4f-107">Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="69d4f-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a><span data-ttu-id="69d4f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69d4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69d4f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69d4f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69d4f-110">Um identificador para a janela do cliente que está enviando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="69d4f-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="69d4f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69d4f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69d4f-112">A palavra de ordem inferior Especifica o formato da área de transferência do item para o qual a solicitação de atualização está sendo cancelada.</span><span class="sxs-lookup"><span data-stu-id="69d4f-112">The low-order word specifies the clipboard format of the item for which the update request is being retracted.</span></span> <span data-ttu-id="69d4f-113">Se isso for **nulo**, todas as conversas de [**\_ \_ aviso DDE**](wm-dde-advise.md) ativos do WM para o item serão encerradas.</span><span class="sxs-lookup"><span data-stu-id="69d4f-113">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) conversations for the item are to be terminated.</span></span>

<span data-ttu-id="69d4f-114">A palavra de ordem superior contém um átomo global que identifica o item para o qual a solicitação de atualização está sendo cancelada.</span><span class="sxs-lookup"><span data-stu-id="69d4f-114">The high-order word contains a global atom that identifies the item for which the update request is being retracted.</span></span> <span data-ttu-id="69d4f-115">Se isso for **nulo**, todos os links de [**\_ \_ aviso DDE**](wm-dde-advise.md) ativos do WM associados à conversa serão encerrados.</span><span class="sxs-lookup"><span data-stu-id="69d4f-115">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) links associated with the conversation are to be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69d4f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="69d4f-116">Remarks</span></span>

<span data-ttu-id="69d4f-117">O aplicativo cliente aloca a palavra de ordem superior do *lParam* chamando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="69d4f-117">The client application allocates the high-order word of *lParam* by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="69d4f-118">O aplicativo de servidor posta a mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para responder positiva ou negativamente.</span><span class="sxs-lookup"><span data-stu-id="69d4f-118">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="69d4f-119">Durante o lançamento do **\_ pacote de \_ ACK do WM DDE**, o servidor pode reutilizar o Atom ou pode excluir o Atom e criar um novo.</span><span class="sxs-lookup"><span data-stu-id="69d4f-119">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="69d4f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69d4f-120">Requirements</span></span>



| <span data-ttu-id="69d4f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d4f-121">Requirement</span></span> | <span data-ttu-id="69d4f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="69d4f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69d4f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d4f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="69d4f-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="69d4f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="69d4f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d4f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="69d4f-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="69d4f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69d4f-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="69d4f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="69d4f-128"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69d4f-128"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69d4f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="69d4f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="69d4f-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="69d4f-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="69d4f-131">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="69d4f-131">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="69d4f-132">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="69d4f-132">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="69d4f-133">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="69d4f-133">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="69d4f-134">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="69d4f-134">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="69d4f-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="69d4f-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="69d4f-136">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="69d4f-136">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="69d4f-137">**\_ACK de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="69d4f-137">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="69d4f-138">**\_aviso de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="69d4f-138">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

<span data-ttu-id="69d4f-139">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="69d4f-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="69d4f-140">Sobre troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="69d4f-140">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


---
title: WM_DDE_INITIATE mensagem (Dde.h)
description: Um aplicativo troca dinâmica de dados cliente (DDE) envia uma mensagem WM DDE INITIATE para iniciar uma conversa com um aplicativo de servidor que responde aos nomes de aplicativo e \_ \_ tópico especificados.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE troca de dados de mensagens
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf65e222c7711d429db44e391d4f03c35997e219
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386719"
---
# <a name="wm_dde_initiate-message"></a><span data-ttu-id="96c32-104">Mensagem WM \_ DDE \_ INITIATE</span><span class="sxs-lookup"><span data-stu-id="96c32-104">WM\_DDE\_INITIATE message</span></span>

<span data-ttu-id="96c32-105">Um troca dinâmica de dados cliente (DDE) envia uma mensagem **WM \_ DDE \_ INITIATE** para iniciar uma conversa com um aplicativo de servidor que responde aos nomes de aplicativo e tópico especificados.</span><span class="sxs-lookup"><span data-stu-id="96c32-105">A Dynamic Data Exchange (DDE) client application sends a **WM\_DDE\_INITIATE** message to initiate a conversation with a server application responding to the specified application and topic names.</span></span> <span data-ttu-id="96c32-106">Ao receber essa mensagem, todos os aplicativos de servidor com nomes que corresponderem ao aplicativo especificado e que deem suporte ao tópico especificado devem confirmá-lo.</span><span class="sxs-lookup"><span data-stu-id="96c32-106">Upon receiving this message, all server applications with names that match the specified application and that support the specified topic are expected to acknowledge it.</span></span> <span data-ttu-id="96c32-107">(Para obter mais informações, consulte a [**mensagem WM \_ DDE \_ ACK.)**](wm-dde-ack.md)</span><span class="sxs-lookup"><span data-stu-id="96c32-107">(For more information, see the [**WM\_DDE\_ACK**](wm-dde-ack.md) message.)</span></span>


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a><span data-ttu-id="96c32-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96c32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96c32-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96c32-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96c32-110">Um alça para a janela do cliente que envia a mensagem.</span><span class="sxs-lookup"><span data-stu-id="96c32-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="96c32-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96c32-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96c32-112">A palavra de ordem baixa contém um atom que identifica o aplicativo com o qual uma conversa é solicitada.</span><span class="sxs-lookup"><span data-stu-id="96c32-112">The low-order word contains an atom that identifies the application with which a conversation is requested.</span></span> <span data-ttu-id="96c32-113">O nome do aplicativo não pode conter barras (/) ou barras in backslashes ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="96c32-113">The application name cannot contain slashes (/) or backslashes (\\).</span></span> <span data-ttu-id="96c32-114">Esses caracteres são reservados para implementações de rede.</span><span class="sxs-lookup"><span data-stu-id="96c32-114">These characters are reserved for network implementations.</span></span> <span data-ttu-id="96c32-115">Se esse parâmetro for **NULL,** uma conversa com todos os aplicativos será solicitada.</span><span class="sxs-lookup"><span data-stu-id="96c32-115">If this parameter is **NULL**, a conversation with all applications is requested.</span></span>

<span data-ttu-id="96c32-116">A palavra de ordem alta contém um atom que identifica o tópico para o qual uma conversa é solicitada.</span><span class="sxs-lookup"><span data-stu-id="96c32-116">The high-order word contains an atom that identifies the topic for which a conversation is requested.</span></span> <span data-ttu-id="96c32-117">Se o tópico for **NULL,** serão solicitadas conversas para todos os tópicos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="96c32-117">If the topic is **NULL**, conversations for all available topics are requested.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96c32-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="96c32-118">Remarks</span></span>

<span data-ttu-id="96c32-119">Se a palavra de ordem baixa *de lParam* for **NULL,** qualquer aplicativo de servidor poderá responder.</span><span class="sxs-lookup"><span data-stu-id="96c32-119">If the low-order word of *lParam* is **NULL**, any server application can respond.</span></span> <span data-ttu-id="96c32-120">Se a palavra de ordem alta de *lParam* for **NULL,** qualquer tópico será válido.</span><span class="sxs-lookup"><span data-stu-id="96c32-120">If the high-order word of *lParam* is **NULL**, any topic is valid.</span></span> <span data-ttu-id="96c32-121">Ao receber uma solicitação WM DDE INITIATE com a palavra de ordem alta do parâmetro *lParam* definida como **NULL**, um servidor deve enviar uma mensagem WM **\_ \_ DDE** [**\_ \_ ACK**](wm-dde-ack.md) para cada um dos tópicos aos que ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="96c32-121">Upon receiving a **WM\_DDE\_INITIATE** request with the high-order word of the *lParam* parameter set to **NULL**, a server must send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each of the topics it supports.</span></span>

### <a name="sending"></a><span data-ttu-id="96c32-122">Envio</span><span class="sxs-lookup"><span data-stu-id="96c32-122">Sending</span></span>

<span data-ttu-id="96c32-123">O cliente transmite a mensagem para todas as janelas de nível superior definindo o primeiro parâmetro de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) como **HWND \_ BROADCAST.**</span><span class="sxs-lookup"><span data-stu-id="96c32-123">The client broadcasts the message to all top-level windows by setting the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="96c32-124">Se o aplicativo cliente já tiver obtido o handle de janela do servidor desejado, ele poderá enviar **WM \_ DDE \_ INITIATE** diretamente para a janela do servidor passando o alça de janela do servidor como o primeiro parâmetro [**de SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="96c32-124">If the client application has already obtained the window handle of the desired server, it can send **WM\_DDE\_INITIATE** directly to the server window by passing the server's window handle as the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span>

<span data-ttu-id="96c32-125">O aplicativo cliente aloca átomos chamando a [**função GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)</span><span class="sxs-lookup"><span data-stu-id="96c32-125">The client application allocates atoms by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="96c32-126">Quando [**SendMessage retorna,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o aplicativo cliente deve excluir os átomos.</span><span class="sxs-lookup"><span data-stu-id="96c32-126">When [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application must delete the atoms.</span></span>

### <a name="receiving"></a><span data-ttu-id="96c32-127">Recebimento</span><span class="sxs-lookup"><span data-stu-id="96c32-127">Receiving</span></span>

<span data-ttu-id="96c32-128">Para concluir o início de uma conversa, o aplicativo de servidor deve responder com uma ou mais mensagens [**WM \_ DDE \_ ACK,**](wm-dde-ack.md) em que cada mensagem é para um tópico separado.</span><span class="sxs-lookup"><span data-stu-id="96c32-128">To complete the initiation of a conversation, the server application must respond with one or more [**WM\_DDE\_ACK**](wm-dde-ack.md) messages, where each message is for a separate topic.</span></span> <span data-ttu-id="96c32-129">Ao enviar **a mensagem WM \_ DDE \_ ACK,** o servidor deve criar novos átomos; ele não deve reutilizar os átomos enviados com **WM \_ DDE \_ INITIATE.**</span><span class="sxs-lookup"><span data-stu-id="96c32-129">When sending **WM\_DDE\_ACK** message, the server should create new atoms; it should not reuse the atoms sent with **WM\_DDE\_INITIATE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="96c32-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96c32-130">Requirements</span></span>



| <span data-ttu-id="96c32-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="96c32-131">Requirement</span></span> | <span data-ttu-id="96c32-132">Valor</span><span class="sxs-lookup"><span data-stu-id="96c32-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96c32-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96c32-133">Minimum supported client</span></span><br/> | <span data-ttu-id="96c32-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96c32-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="96c32-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96c32-135">Minimum supported server</span></span><br/> | <span data-ttu-id="96c32-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96c32-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="96c32-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="96c32-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="96c32-138"><dt>Dde.h (inclua Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="96c32-138"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96c32-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="96c32-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="96c32-140">**Referência**</span><span class="sxs-lookup"><span data-stu-id="96c32-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="96c32-141">**Globaladdatom**</span><span class="sxs-lookup"><span data-stu-id="96c32-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="96c32-142">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="96c32-142">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="96c32-143">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="96c32-143">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="96c32-144">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="96c32-144">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="96c32-145">**Conceitual**</span><span class="sxs-lookup"><span data-stu-id="96c32-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="96c32-146">Sobre troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="96c32-146">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


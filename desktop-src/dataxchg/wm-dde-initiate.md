---
title: Mensagem de WM_DDE_INITIATE (DDE. h)
description: Um aplicativo cliente troca dinâmica de dados (DDE) envia uma mensagem de início do WM \_ DDE \_ para iniciar uma conversa com um aplicativo de servidor respondendo aos nomes de aplicativo e de tópico especificados.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- Troca de dados de mensagem WM_DDE_INITIATE
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
ms.openlocfilehash: 36485db262c46d5364ee0ee26e7e6f39ccf0e677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369546"
---
# <a name="wm_dde_initiate-message"></a><span data-ttu-id="0111f-104">Mensagem de inicialização de \_ DDE do WM \_</span><span class="sxs-lookup"><span data-stu-id="0111f-104">WM\_DDE\_INITIATE message</span></span>

<span data-ttu-id="0111f-105">Um aplicativo cliente troca dinâmica de dados (DDE) envia uma mensagem de **\_ \_ início do WM DDE** para iniciar uma conversa com um aplicativo de servidor respondendo aos nomes de aplicativo e de tópico especificados.</span><span class="sxs-lookup"><span data-stu-id="0111f-105">A Dynamic Data Exchange (DDE) client application sends a **WM\_DDE\_INITIATE** message to initiate a conversation with a server application responding to the specified application and topic names.</span></span> <span data-ttu-id="0111f-106">Ao receber essa mensagem, todos os aplicativos de servidor com nomes que correspondem ao aplicativo especificado e que dão suporte ao tópico especificado devem confirmá-lo.</span><span class="sxs-lookup"><span data-stu-id="0111f-106">Upon receiving this message, all server applications with names that match the specified application and that support the specified topic are expected to acknowledge it.</span></span> <span data-ttu-id="0111f-107">(Para obter mais informações, consulte a mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) .)</span><span class="sxs-lookup"><span data-stu-id="0111f-107">(For more information, see the [**WM\_DDE\_ACK**](wm-dde-ack.md) message.)</span></span>


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a><span data-ttu-id="0111f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0111f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0111f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0111f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0111f-110">Um identificador para a janela do cliente que está enviando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="0111f-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="0111f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0111f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0111f-112">A palavra de ordem inferior contém um Atom que identifica o aplicativo com o qual uma conversa é solicitada.</span><span class="sxs-lookup"><span data-stu-id="0111f-112">The low-order word contains an atom that identifies the application with which a conversation is requested.</span></span> <span data-ttu-id="0111f-113">O nome do aplicativo não pode conter barras (/) ou barras invertidas ( \) .</span><span class="sxs-lookup"><span data-stu-id="0111f-113">The application name cannot contain slashes (/) or backslashes (\).</span></span> <span data-ttu-id="0111f-114">Esses caracteres são reservados para implementações de rede.</span><span class="sxs-lookup"><span data-stu-id="0111f-114">These characters are reserved for network implementations.</span></span> <span data-ttu-id="0111f-115">Se esse parâmetro for **NULL**, será solicitada uma conversa com todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0111f-115">If this parameter is **NULL**, a conversation with all applications is requested.</span></span>

<span data-ttu-id="0111f-116">A palavra de ordem superior contém um átomo que identifica o tópico para o qual uma conversa é solicitada.</span><span class="sxs-lookup"><span data-stu-id="0111f-116">The high-order word contains an atom that identifies the topic for which a conversation is requested.</span></span> <span data-ttu-id="0111f-117">Se o tópico for **nulo**, as conversas de todos os tópicos disponíveis serão solicitadas.</span><span class="sxs-lookup"><span data-stu-id="0111f-117">If the topic is **NULL**, conversations for all available topics are requested.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0111f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0111f-118">Remarks</span></span>

<span data-ttu-id="0111f-119">Se a palavra de ordem inferior de *lParam* for **nula**, qualquer aplicativo de servidor poderá responder.</span><span class="sxs-lookup"><span data-stu-id="0111f-119">If the low-order word of *lParam* is **NULL**, any server application can respond.</span></span> <span data-ttu-id="0111f-120">Se a palavra de ordem superior de *lParam* for **nula**, qualquer tópico será válido.</span><span class="sxs-lookup"><span data-stu-id="0111f-120">If the high-order word of *lParam* is **NULL**, any topic is valid.</span></span> <span data-ttu-id="0111f-121">Após receber uma solicitação de **\_ \_ inicialização de DDE do WM** com a palavra de ordem superior do parâmetro *lParam* definido como **NULL**, um servidor deve enviar uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para cada um dos tópicos com suporte.</span><span class="sxs-lookup"><span data-stu-id="0111f-121">Upon receiving a **WM\_DDE\_INITIATE** request with the high-order word of the *lParam* parameter set to **NULL**, a server must send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each of the topics it supports.</span></span>

### <a name="sending"></a><span data-ttu-id="0111f-122">Envio</span><span class="sxs-lookup"><span data-stu-id="0111f-122">Sending</span></span>

<span data-ttu-id="0111f-123">O cliente transmite a mensagem para todas as janelas de nível superior definindo o primeiro parâmetro de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para a **\_ difusão de hWnd**.</span><span class="sxs-lookup"><span data-stu-id="0111f-123">The client broadcasts the message to all top-level windows by setting the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="0111f-124">Se o aplicativo cliente já tiver obtido o identificador de janela do servidor desejado, ele poderá enviar o **WM \_ DDE \_ inicie** diretamente para a janela do servidor passando o identificador de janela do servidor como o primeiro parâmetro de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="0111f-124">If the client application has already obtained the window handle of the desired server, it can send **WM\_DDE\_INITIATE** directly to the server window by passing the server's window handle as the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span>

<span data-ttu-id="0111f-125">O aplicativo cliente aloca Atoms chamando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="0111f-125">The client application allocates atoms by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="0111f-126">Quando [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retorna, o aplicativo cliente deve excluir os átomos.</span><span class="sxs-lookup"><span data-stu-id="0111f-126">When [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application must delete the atoms.</span></span>

### <a name="receiving"></a><span data-ttu-id="0111f-127">Recebimento</span><span class="sxs-lookup"><span data-stu-id="0111f-127">Receiving</span></span>

<span data-ttu-id="0111f-128">Para concluir a inicialização de uma conversa, o aplicativo de servidor deve responder com uma ou mais mensagens de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) , em que cada mensagem é para um tópico separado.</span><span class="sxs-lookup"><span data-stu-id="0111f-128">To complete the initiation of a conversation, the server application must respond with one or more [**WM\_DDE\_ACK**](wm-dde-ack.md) messages, where each message is for a separate topic.</span></span> <span data-ttu-id="0111f-129">Ao enviar a mensagem de **\_ \_ ACK DDE do WM** , o servidor deve criar novos átomos; ele não deve reutilizar os átomos enviados com o **WM \_ DDE \_ Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="0111f-129">When sending **WM\_DDE\_ACK** message, the server should create new atoms; it should not reuse the atoms sent with **WM\_DDE\_INITIATE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0111f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0111f-130">Requirements</span></span>



| <span data-ttu-id="0111f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0111f-131">Requirement</span></span> | <span data-ttu-id="0111f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0111f-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0111f-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0111f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0111f-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0111f-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0111f-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0111f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0111f-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0111f-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0111f-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0111f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0111f-138"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0111f-138"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0111f-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0111f-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="0111f-140">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0111f-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0111f-141">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="0111f-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="0111f-142">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="0111f-142">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="0111f-143">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="0111f-143">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="0111f-144">**\_ACK de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0111f-144">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="0111f-145">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="0111f-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0111f-146">Sobre troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="0111f-146">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


---
title: Mensagem de WM_DDE_DATA (DDE. h)
description: Um aplicativo de servidor troca dinâmica de dados (DDE) posta uma \_ mensagem de dados DDE do WM \_ em um aplicativo cliente DDE para passar um item de dados para o cliente ou notificar o cliente sobre a disponibilidade de um item de dados.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- Troca de dados de mensagem WM_DDE_DATA
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f045ff07e01023e6535eb00dcb78400e4c9519a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812098"
---
# <a name="wm_dde_data-message"></a><span data-ttu-id="eea67-104">\_Mensagem de dados DDE do WM \_</span><span class="sxs-lookup"><span data-stu-id="eea67-104">WM\_DDE\_DATA message</span></span>

<span data-ttu-id="eea67-105">Um aplicativo de servidor troca dinâmica de dados (DDE) posta uma mensagem de **\_ \_ dados DDE do WM** em um aplicativo cliente DDE para passar um item de dados para o cliente ou notificar o cliente sobre a disponibilidade de um item de dados.</span><span class="sxs-lookup"><span data-stu-id="eea67-105">A Dynamic Data Exchange (DDE) server application posts a **WM\_DDE\_DATA** message to a DDE client application to pass a data item to the client or to notify the client of the availability of a data item.</span></span>

<span data-ttu-id="eea67-106">Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="eea67-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a><span data-ttu-id="eea67-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eea67-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eea67-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eea67-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eea67-109">Um identificador para a janela do servidor postando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="eea67-109">A handle to the server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="eea67-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eea67-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eea67-111">A palavra de ordem inferior é um identificador para um objeto de memória global que contém uma estrutura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) com os dados e informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="eea67-111">The low-order word is a handle to a global memory object containing a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure with the data and additional information.</span></span> <span data-ttu-id="eea67-112">O identificador deve ser definido como **nulo** se o servidor estiver notificando o cliente que o valor do item de dados foi alterado durante um link de dados quente.</span><span class="sxs-lookup"><span data-stu-id="eea67-112">The handle should be set to **NULL** if the server is notifying the client that the data-item value has changed during a warm data link.</span></span> <span data-ttu-id="eea67-113">Um link quente é estabelecido pelo cliente que envia uma mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-advise.md) com o conjunto de bits **fDeferUpd** .</span><span class="sxs-lookup"><span data-stu-id="eea67-113">A warm link is established by the client sending a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message with the **fDeferUpd** bit set.</span></span>

<span data-ttu-id="eea67-114">A palavra de ordem superior contém um átomo que identifica o item de dados para o qual os dados ou a notificação são enviados.</span><span class="sxs-lookup"><span data-stu-id="eea67-114">The high-order word contains an atom that identifies the data item for which the data or notification is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eea67-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="eea67-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="eea67-116">Lançamento</span><span class="sxs-lookup"><span data-stu-id="eea67-116">Posting</span></span>

<span data-ttu-id="eea67-117">O aplicativo de servidor aloca o objeto de memória global usando a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="eea67-117">The server application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="eea67-118">Ele aloca o Atom usando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="eea67-118">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="eea67-119">O servidor deve criar ou reutilizar o parâmetro de *lParam* de **\_ \_ dados DDE do WM** chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="eea67-119">The server must create or reuse the **WM\_DDE\_DATA** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="eea67-120">Se o aplicativo receptor (cliente) responder com uma mensagem [**de \_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa, o aplicativo de postagem (servidor) deverá excluir o objeto de memória global; caso contrário, o cliente deverá excluir o objeto depois de extrair seu conteúdo chamando a função [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) .</span><span class="sxs-lookup"><span data-stu-id="eea67-120">If the receiving (client) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting (server) application must delete the global memory object; otherwise, the client must delete the object after extracting its contents by calling the [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) function.</span></span>

<span data-ttu-id="eea67-121">Se o aplicativo de servidor definir o membro **fRelease** da estrutura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) como **false**, o servidor será responsável por excluir o objeto no recebimento de uma confirmação positiva ou negativa.</span><span class="sxs-lookup"><span data-stu-id="eea67-121">If the server application sets the **fRelease** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**, the server is responsible for deleting the object upon receiving either a positive or negative acknowledgment.</span></span>

<span data-ttu-id="eea67-122">O aplicativo de servidor não deve definir os membros **fAckReq** e **FRelease** da estrutura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) como **false**.</span><span class="sxs-lookup"><span data-stu-id="eea67-122">The server application should not set both the **fAckReq** and **fRelease** members of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**.</span></span> <span data-ttu-id="eea67-123">Se ambos os membros forem definidos como **false**, será impossível para o servidor determinar quando excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="eea67-123">If both members are set to **FALSE**, it is impossible for the server to determine when to delete the object.</span></span>

### <a name="receiving"></a><span data-ttu-id="eea67-124">Recebimento</span><span class="sxs-lookup"><span data-stu-id="eea67-124">Receiving</span></span>

<span data-ttu-id="eea67-125">Se **fAckReq** for **true**, o aplicativo cliente deverá postar a mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para responder positiva ou negativamente.</span><span class="sxs-lookup"><span data-stu-id="eea67-125">If **fAckReq** is **TRUE**, the client application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="eea67-126">Ao lançar o **WM \_ DDE \_ ACK**, o cliente pode reutilizar o Atom ou pode excluí-lo e criar um novo.</span><span class="sxs-lookup"><span data-stu-id="eea67-126">When posting **WM\_DDE\_ACK**, the client can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="eea67-127">O cliente deve criar ou reutilizar o parâmetro de *lParam* [**\_ DDE \_ ACK do WM**](wm-dde-ack.md) chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="eea67-127">The client must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="eea67-128">Se **fAckReq** for **false**, o aplicativo cliente deverá excluir o Atom.</span><span class="sxs-lookup"><span data-stu-id="eea67-128">If **fAckReq** is **FALSE**, the client application should delete the atom.</span></span>

<span data-ttu-id="eea67-129">Se o aplicativo de lançamento especificou o objeto de memória global como **nulo**, o aplicativo receptor pode solicitar que o servidor envie os dados postando uma mensagem de [**\_ \_ solicitação DDE do WM**](wm-dde-request.md) .</span><span class="sxs-lookup"><span data-stu-id="eea67-129">If the posting application specified global memory object as **NULL**, the receiving application can request the server to send the data by posting a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message.</span></span>

<span data-ttu-id="eea67-130">Depois de processar uma mensagem de **\_ \_ dados DDE do WM** em que o objeto de memória global não é **nulo**, o cliente deve liberar o objeto, a menos que uma das seguintes condições seja verdadeira:</span><span class="sxs-lookup"><span data-stu-id="eea67-130">After processing a **WM\_DDE\_DATA** message in which the global memory object is not **NULL**, the client should free the object, unless one of the following conditions is true:</span></span>

-   <span data-ttu-id="eea67-131">O membro **fRelease** é **false**.</span><span class="sxs-lookup"><span data-stu-id="eea67-131">The **fRelease** member is **FALSE**.</span></span>
-   <span data-ttu-id="eea67-132">O membro **fRelease** é **true**, mas o aplicativo cliente responde com uma mensagem [**de \_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa.</span><span class="sxs-lookup"><span data-stu-id="eea67-132">The **fRelease** member is **TRUE**, but the client application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea67-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eea67-133">Requirements</span></span>



| <span data-ttu-id="eea67-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="eea67-134">Requirement</span></span> | <span data-ttu-id="eea67-135">Valor</span><span class="sxs-lookup"><span data-stu-id="eea67-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eea67-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eea67-136">Minimum supported client</span></span><br/> | <span data-ttu-id="eea67-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eea67-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eea67-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eea67-138">Minimum supported server</span></span><br/> | <span data-ttu-id="eea67-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eea67-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eea67-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="eea67-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="eea67-141"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eea67-141"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eea67-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="eea67-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="eea67-143">**Referência**</span><span class="sxs-lookup"><span data-stu-id="eea67-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eea67-144">**DDEDATA**</span><span class="sxs-lookup"><span data-stu-id="eea67-144">**DDEDATA**</span></span>](/windows/desktop/api/Dde/ns-dde-ddedata)
</dt> <dt>

[<span data-ttu-id="eea67-145">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="eea67-145">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="eea67-146">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="eea67-146">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="eea67-147">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="eea67-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="eea67-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="eea67-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="eea67-149">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="eea67-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="eea67-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="eea67-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="eea67-151">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="eea67-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="eea67-152">**\_ACK de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="eea67-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="eea67-153">**\_aviso de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="eea67-153">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="eea67-154">**o WM \_ DDE. \_**</span><span class="sxs-lookup"><span data-stu-id="eea67-154">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="eea67-155">**\_solicitação de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="eea67-155">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="eea67-156">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="eea67-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eea67-157">Sobre troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="eea67-157">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


---
title: Mensagem de WM_DDE_ADVISE (DDE. h)
description: Um aplicativo cliente troca dinâmica de dados (DDE) posta a mensagem de aviso de DDE do WM \_ \_ em um aplicativo de servidor DDE para solicitar que o servidor forneça uma atualização para um item de dados sempre que o item for alterado.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- Troca de dados de mensagem WM_DDE_ADVISE
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832c6991169b71955c0ab21b59d2b55b0b54fc9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085482"
---
# <a name="wm_dde_advise-message"></a><span data-ttu-id="309bc-104">Mensagem de aviso de \_ DDE do WM \_</span><span class="sxs-lookup"><span data-stu-id="309bc-104">WM\_DDE\_ADVISE message</span></span>

<span data-ttu-id="309bc-105">Um aplicativo cliente troca dinâmica de dados (DDE) posta a mensagem de **\_ \_ aviso de DDE do WM** em um aplicativo de servidor DDE para solicitar que o servidor forneça uma atualização para um item de dados sempre que o item for alterado.</span><span class="sxs-lookup"><span data-stu-id="309bc-105">A Dynamic Data Exchange (DDE) client application posts the **WM\_DDE\_ADVISE** message to a DDE server application to request the server to supply an update for a data item whenever the item changes.</span></span>

<span data-ttu-id="309bc-106">Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="309bc-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a><span data-ttu-id="309bc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="309bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="309bc-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="309bc-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="309bc-109">Um identificador para a janela do cliente que está postando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="309bc-109">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="309bc-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="309bc-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="309bc-111">A palavra de ordem inferior é um identificador para um objeto de memória global que contém uma estrutura [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) que especifica como os dados serão enviados.</span><span class="sxs-lookup"><span data-stu-id="309bc-111">The low-order word is a handle to a global memory object containing a [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) structure that specifies how the data is to be sent.</span></span>

<span data-ttu-id="309bc-112">A palavra de ordem superior contém um Atom que identifica o item de dados solicitado.</span><span class="sxs-lookup"><span data-stu-id="309bc-112">The high-order word contains an atom that identifies the requested data item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="309bc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="309bc-113">Remarks</span></span>

<span data-ttu-id="309bc-114">Se um aplicativo cliente oferecer suporte a mais de um formato de área de transferência para um único tópico e item, ele poderá postar várias mensagens de **\_ \_ aviso de DDE do WM** para o tópico e o item, especificando um formato de área de transferência diferente com cada mensagem.</span><span class="sxs-lookup"><span data-stu-id="309bc-114">If a client application supports more than one clipboard format for a single topic and item, it can post multiple **WM\_DDE\_ADVISE** messages for the topic and item, specifying a different clipboard format with each message.</span></span> <span data-ttu-id="309bc-115">Observe que um servidor pode dar suporte a vários formatos somente para links de dados dinâmicos, não para links de dados quentes.</span><span class="sxs-lookup"><span data-stu-id="309bc-115">Note that a server can support multiple formats only for hot data links, not warm data links.</span></span>

### <a name="posting"></a><span data-ttu-id="309bc-116">Lançamento</span><span class="sxs-lookup"><span data-stu-id="309bc-116">Posting</span></span>

<span data-ttu-id="309bc-117">O aplicativo cliente posta a mensagem de **\_ \_ aviso de DDE do WM** chamando a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , não a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="309bc-117">The client application posts the **WM\_DDE\_ADVISE** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="309bc-118">O aplicativo cliente aloca o objeto de memória global usando a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="309bc-118">The client application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="309bc-119">Ele aloca o Atom usando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="309bc-119">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="309bc-120">O aplicativo cliente deve criar ou reutilizar o parâmetro *lParam* do **\_ \_ visor de comunicação do WM** chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="309bc-120">The client application must create or reuse the **WM\_DDE\_ADVISE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="309bc-121">Se o aplicativo receptor (servidor) responder com uma mensagem [**de \_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa, o aplicativo de lançamento deverá excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="309bc-121">If the receiving (server) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting application must delete the object.</span></span>

<span data-ttu-id="309bc-122">O **sinalizador fRelease** não é usado em mensagens de **\_ \_ aviso de DDE do WM** , mas seu comportamento de liberação de dados é semelhante ao do [**WM \_ DDE \_ Data**](wm-dde-data.md) e ao [**WM \_ DDE \_**](wm-dde-poke.md) fazer mensagens em que **fRelease** é **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="309bc-122">The **fRelease** flag is not used in **WM\_DDE\_ADVISE** messages, but their data-freeing behavior is similar to that of [**WM\_DDE\_DATA**](wm-dde-data.md) and [**WM\_DDE\_POKE**](wm-dde-poke.md) messages where **fRelease** is **TRUE**.</span></span>

### <a name="receiving"></a><span data-ttu-id="309bc-123">Recebimento</span><span class="sxs-lookup"><span data-stu-id="309bc-123">Receiving</span></span>

<span data-ttu-id="309bc-124">O aplicativo de servidor posta a mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para responder positiva ou negativamente.</span><span class="sxs-lookup"><span data-stu-id="309bc-124">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="309bc-125">Ao lançar o aplicativo de **\_ \_ confirmação de DDE do WM**, ele pode reutilizar o Atom ou excluí-lo e criar um novo.</span><span class="sxs-lookup"><span data-stu-id="309bc-125">When posting **WM\_DDE\_ACK**, the application can reuse the atom or delete it and create a new one.</span></span> <span data-ttu-id="309bc-126">Se a mensagem de **\_ \_ ACK DDE do WM** for positiva, o aplicativo deverá excluir o objeto de memória global; caso contrário, o aplicativo não deverá excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="309bc-126">If the **WM\_DDE\_ACK** message is positive, the application should delete the global memory object; otherwise, the application should not delete the object.</span></span>

<span data-ttu-id="309bc-127">O servidor deve criar ou reutilizar o parâmetro de *lParam* [**\_ DDE \_ ACK do WM**](wm-dde-ack.md) chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="309bc-127">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="309bc-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="309bc-128">Requirements</span></span>



| <span data-ttu-id="309bc-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="309bc-129">Requirement</span></span> | <span data-ttu-id="309bc-130">Valor</span><span class="sxs-lookup"><span data-stu-id="309bc-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="309bc-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="309bc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="309bc-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="309bc-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="309bc-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="309bc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="309bc-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="309bc-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="309bc-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="309bc-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="309bc-136"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="309bc-136"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="309bc-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="309bc-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="309bc-138">**Referência**</span><span class="sxs-lookup"><span data-stu-id="309bc-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="309bc-139">**DDEADVISE**</span><span class="sxs-lookup"><span data-stu-id="309bc-139">**DDEADVISE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[<span data-ttu-id="309bc-140">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="309bc-140">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="309bc-141">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="309bc-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="309bc-142">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="309bc-142">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="309bc-143">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="309bc-143">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="309bc-144">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="309bc-144">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="309bc-145">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="309bc-145">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="309bc-146">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="309bc-146">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="309bc-147">**\_ACK de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="309bc-147">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="309bc-148">**\_dados DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="309bc-148">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="309bc-149">**o WM \_ DDE. \_**</span><span class="sxs-lookup"><span data-stu-id="309bc-149">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="309bc-150">**\_solicitação de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="309bc-150">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="309bc-151">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="309bc-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="309bc-152">Sobre troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="309bc-152">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


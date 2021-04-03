---
title: Mensagem de WM_DDE_POKE (DDE. h)
description: Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de envio de DDE do WM \_ \_ em um aplicativo de servidor DDE.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- Troca de dados de mensagem WM_DDE_POKE
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645198"
---
# <a name="wm_dde_poke-message"></a><span data-ttu-id="cc44f-104">Mensagem de remediar DDE do WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="cc44f-104">WM\_DDE\_POKE message</span></span>

<span data-ttu-id="cc44f-105">Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de envio de **\_ \_ DDE do WM** em um aplicativo de servidor DDE.</span><span class="sxs-lookup"><span data-stu-id="cc44f-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_POKE** message to a DDE server application.</span></span> <span data-ttu-id="cc44f-106">Um cliente usa essa mensagem para solicitar que o servidor aceite um item de dados não solicitado.</span><span class="sxs-lookup"><span data-stu-id="cc44f-106">A client uses this message to request the server to accept an unsolicited data item.</span></span> <span data-ttu-id="cc44f-107">Espera-se que o servidor responda com uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) indicando se ele aceitou o item de dados.</span><span class="sxs-lookup"><span data-stu-id="cc44f-107">The server is expected to reply with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message indicating whether it accepted the data item.</span></span>

<span data-ttu-id="cc44f-108">Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc44f-108">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a><span data-ttu-id="cc44f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc44f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc44f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc44f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc44f-111">Um identificador para a janela do cliente que está postando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="cc44f-111">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="cc44f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc44f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc44f-113">A palavra de ordem inferior é um identificador para um objeto de memória global que contém uma estrutura [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) com os dados e informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="cc44f-113">The low-order word is a handle to a global memory object containing a [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) structure with the data and additional information.</span></span>

<span data-ttu-id="cc44f-114">A palavra de ordem superior contém um átomo global que identifica o item de dados para o qual os dados ou a notificação estão sendo enviados.</span><span class="sxs-lookup"><span data-stu-id="cc44f-114">The high-order word contains a global atom that identifies the data item for which the data or notification is being sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc44f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc44f-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="cc44f-116">Lançamento</span><span class="sxs-lookup"><span data-stu-id="cc44f-116">Posting</span></span>

<span data-ttu-id="cc44f-117">O aplicativo cliente deve alocar memória para o objeto de memória global usando a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="cc44f-117">The client application must allocate memory for the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="cc44f-118">O aplicativo cliente deve excluir o objeto se qualquer uma das seguintes condições for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="cc44f-118">The client application must delete the object if either of the following conditions is true:</span></span>

-   <span data-ttu-id="cc44f-119">O aplicativo de servidor responde com uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa.</span><span class="sxs-lookup"><span data-stu-id="cc44f-119">The server application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>
-   <span data-ttu-id="cc44f-120">O membro **fRelease** é **false**, mas o aplicativo de servidor responde com um [**\_ \_ ACK DDE do WM**](wm-dde-ack.md)positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="cc44f-120">The **fRelease** member is **FALSE**, but the server application responds with either a positive or negative [**WM\_DDE\_ACK**](wm-dde-ack.md).</span></span>

<span data-ttu-id="cc44f-121">O aplicativo cliente deve criar o Atom usando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="cc44f-121">The client application must create the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="cc44f-122">O aplicativo cliente deve criar ou reutilizar o parâmetro de *lParam* de envio do **WM \_ DDE \_** , chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="cc44f-122">The client application must create or reuse the **WM\_DDE\_POKE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="cc44f-123">Recebimento</span><span class="sxs-lookup"><span data-stu-id="cc44f-123">Receiving</span></span>

<span data-ttu-id="cc44f-124">O aplicativo de servidor deve postar a mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para responder positivamente ou negativamente.</span><span class="sxs-lookup"><span data-stu-id="cc44f-124">The server application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="cc44f-125">Ao lançar o **WM \_ DDE \_ ACK**, o servidor pode reutilizar o Atom ou pode excluí-lo e criar um novo.</span><span class="sxs-lookup"><span data-stu-id="cc44f-125">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="cc44f-126">O servidor deve criar ou reutilizar o parâmetro de *lParam* [**\_ DDE \_ ACK do WM**](wm-dde-ack.md) chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="cc44f-126">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="cc44f-127">Para liberar o objeto de memória global, o servidor deve chamar a função [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="cc44f-127">To free the global memory object, the server should call the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="cc44f-128">Além disso, se o formato de dados for o [**CF \_ DSPMETAFILEPICT**](clipboard-formats.md) ou o **CF \_ METAFILEPICT**, o servidor também deverá chamar [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) com o identificador de metarquivo inserido.</span><span class="sxs-lookup"><span data-stu-id="cc44f-128">Also, if the data format is either [**CF\_DSPMETAFILEPICT**](clipboard-formats.md) or **CF\_METAFILEPICT**, the server must also call [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) with the embedded metafile handle.</span></span> <span data-ttu-id="cc44f-129">Esses dois formatos têm um nível extra de indireção; ou seja, um aplicativo deve bloquear o objeto para obter um ponteiro para um identificador e, em seguida, bloquear esse identificador para obter um ponteiro para uma estrutura [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) e, finalmente, chamar **DeleteMetaFile** com o identificador do membro **hMF** da estrutura **METAFILEPICT** .</span><span class="sxs-lookup"><span data-stu-id="cc44f-129">These two formats have an extra level of indirection; that is, an application must lock the object to get a pointer to a handle, then lock that handle to get a pointer to a [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) structure, and finally call **DeleteMetaFile** with the handle from the **hMF** member of the **METAFILEPICT** structure.</span></span>

<span data-ttu-id="cc44f-130">Para liberar o objeto, o servidor deve chamar a função [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .</span><span class="sxs-lookup"><span data-stu-id="cc44f-130">To free the object, the server should call the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc44f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc44f-131">Requirements</span></span>



| <span data-ttu-id="cc44f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc44f-132">Requirement</span></span> | <span data-ttu-id="cc44f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="cc44f-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc44f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc44f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cc44f-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cc44f-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cc44f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc44f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cc44f-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cc44f-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cc44f-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cc44f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc44f-139"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc44f-139"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc44f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc44f-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc44f-141">**Referência**</span><span class="sxs-lookup"><span data-stu-id="cc44f-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cc44f-142">**DDEPOKE**</span><span class="sxs-lookup"><span data-stu-id="cc44f-142">**DDEPOKE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[<span data-ttu-id="cc44f-143">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="cc44f-143">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="cc44f-144">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="cc44f-144">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="cc44f-145">**METAFILEPICT**</span><span class="sxs-lookup"><span data-stu-id="cc44f-145">**METAFILEPICT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
</dt> <dt>

[<span data-ttu-id="cc44f-146">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="cc44f-146">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="cc44f-147">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="cc44f-147">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="cc44f-148">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="cc44f-148">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="cc44f-149">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="cc44f-149">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="cc44f-150">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="cc44f-150">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="cc44f-151">**\_ACK de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="cc44f-151">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="cc44f-152">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="cc44f-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cc44f-153">Sobre troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="cc44f-153">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


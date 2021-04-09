---
title: Mensagem de WM_DDE_ACK (DDE. h)
description: A \_ mensagem de ACK DDE do WM \_ Notifica um aplicativo troca dinâmica de dados (DDE) do recebimento e do processamento das seguintes mensagens do WM \_ DDE enviar, do \_ WM \_ DDE \_ Execute, do WM DDE \_ \_ data, do WM \_ DDE \_ Advise, \_ do WM DDE UNADVISE, do WM \_ \_ DDE \_ INITIATE ou \_ \_ da solicitação DDE do WM (em alguns casos). Para postar essa mensagem, chame a função CreateMessage com os parâmetros a seguir.
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- Troca de dados de mensagem WM_DDE_ACK
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009288"
---
# <a name="wm_dde_ack-message"></a><span data-ttu-id="4ea26-105">\_Mensagem de ACK DDE do WM \_</span><span class="sxs-lookup"><span data-stu-id="4ea26-105">WM\_DDE\_ACK message</span></span>

<span data-ttu-id="4ea26-106">A **mensagem \_ de \_ ACK DDE do WM** notifica um aplicativo troca dinâmica de dados (DDE) do recebimento e do processamento das seguintes mensagens: [**WM \_ DDE \_**](wm-dde-poke.md)enviar, [**WM \_ DDE \_ Execute**](wm-dde-execute.md), [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM \_ DDE \_ Advise**](wm-dde-advise.md), [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md), [**WM \_ DDE \_ Iniciar**](wm-dde-initiate.md)ou a [**\_ \_ solicitação DDE do WM**](wm-dde-request.md) (em alguns casos).</span><span class="sxs-lookup"><span data-stu-id="4ea26-106">The **WM\_DDE\_ACK** message notifies a Dynamic Data Exchange (DDE) application of the receipt and processing of the following messages: [**WM\_DDE\_POKE**](wm-dde-poke.md), [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_ADVISE**](wm-dde-advise.md), [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md), [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), or [**WM\_DDE\_REQUEST**](wm-dde-request.md) (in some cases).</span></span>

<span data-ttu-id="4ea26-107">Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ea26-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a><span data-ttu-id="4ea26-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ea26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ea26-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ea26-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ea26-110">Ao responder ao [**WM \_ DDE \_ Iniciar**](wm-dde-initiate.md), esse parâmetro é um identificador para a janela do servidor que está enviando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="4ea26-110">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), this parameter is a handle to the server window sending the message.</span></span>

<span data-ttu-id="4ea26-111">Ao responder ao [**WM \_ DDE \_ Execute**](wm-dde-execute.md), esse parâmetro é um identificador para a janela do servidor que está postando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="4ea26-111">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), this parameter is a handle to the server window posting the message.</span></span>

<span data-ttu-id="4ea26-112">Ao responder a todas as outras mensagens, esse parâmetro é um identificador para a janela do cliente ou do servidor que está postando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="4ea26-112">When replying to all other messages, this parameter is a handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="4ea26-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ea26-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ea26-114">Ao responder ao [**WM \_ DDE \_ Iniciar**](wm-dde-initiate.md), a palavra de ordem inferior contém um Atom que identifica o aplicativo de resposta.</span><span class="sxs-lookup"><span data-stu-id="4ea26-114">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), the low-order word contains an atom that identifies the replying application.</span></span> <span data-ttu-id="4ea26-115">A palavra de ordem superior contém um átomo que identifica o tópico para o qual uma conversa está sendo estabelecida.</span><span class="sxs-lookup"><span data-stu-id="4ea26-115">The high-order word contains an atom that identifies the topic for which a conversation is being established.</span></span>

<span data-ttu-id="4ea26-116">Ao responder ao [**WM \_ DDE \_ Execute**](wm-dde-execute.md), a palavra de ordem inferior Especifica uma estrutura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) que contém uma série de sinalizadores que indicam o status da resposta.</span><span class="sxs-lookup"><span data-stu-id="4ea26-116">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="4ea26-117">A palavra de ordem superior é um identificador para um objeto de memória global que contém a cadeia de caracteres de comando que foi recebida na mensagem de **\_ \_ execução de DDE do WM** .</span><span class="sxs-lookup"><span data-stu-id="4ea26-117">The high-order word is a handle to a global memory object that contains the command string that was received in the **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="4ea26-118">Ao responder a todas as outras mensagens, a palavra de ordem inferior Especifica uma estrutura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) que contém uma série de sinalizadores que indicam o status da resposta.</span><span class="sxs-lookup"><span data-stu-id="4ea26-118">When replying to all other messages, the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="4ea26-119">A palavra de ordem superior contém um átomo global que identifica o nome do item de dados para o qual a resposta é enviada.</span><span class="sxs-lookup"><span data-stu-id="4ea26-119">The high-order word contains a global atom that identifies the name of the data item for which the response is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ea26-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ea26-120">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="4ea26-121">Lançamento</span><span class="sxs-lookup"><span data-stu-id="4ea26-121">Posting</span></span>

<span data-ttu-id="4ea26-122">Exceto em resposta à mensagem [**de \_ \_ início do WM DDE**](wm-dde-initiate.md) , o aplicativo envia a mensagem de **ACK do WM \_ DDE \_** chamando a função de postagem, não chamando a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) . [](/windows/desktop/api/winuser/nf-winuser-postmessagea)</span><span class="sxs-lookup"><span data-stu-id="4ea26-122">Except in response to the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message, the application posts the **WM\_DDE\_ACK** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not by calling the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="4ea26-123">Ao responder ao **WM \_ DDE \_ Iniciar**, o aplicativo envia a mensagem de **\_ \_ ACK DDE do WM** chamando **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="4ea26-123">When responding to **WM\_DDE\_INITIATE**, the application sends the **WM\_DDE\_ACK** message by calling **SendMessage**.</span></span> <span data-ttu-id="4ea26-124">Nesse caso, nem o átomo do nome do aplicativo nem o Atom do nome do tópico devem ser **nulos** (mesmo que a mensagem de **início do WM \_ DDE \_** especifique os átomos **nulos** ).</span><span class="sxs-lookup"><span data-stu-id="4ea26-124">In this case, neither the application-name atom nor the topic-name atom should be **NULL** (even if the **WM\_DDE\_INITIATE** message specified **NULL** atoms).</span></span>

<span data-ttu-id="4ea26-125">Ao confirmar qualquer mensagem com um átomo de acompanhamento, a postagem de aplicativo do **WM \_ DDE \_ ACK** pode reutilizar o Atom que acompanha a mensagem original ou pode excluí-la e criar uma nova.</span><span class="sxs-lookup"><span data-stu-id="4ea26-125">When acknowledging any message with an accompanying atom, the application posting **WM\_DDE\_ACK** can either reuse the atom that accompanied the original message, or it can delete it and create a new one.</span></span>

<span data-ttu-id="4ea26-126">Ao confirmar que o [**WM \_ DDE \_ é executado**](wm-dde-execute.md), o aplicativo que publica o **WM \_ DDE \_ ACK** deve reutilizar o objeto de memória global identificado na mensagem de **\_ \_ execução DDE do WM** original.</span><span class="sxs-lookup"><span data-stu-id="4ea26-126">When acknowledging [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the application that posts **WM\_DDE\_ACK** should reuse the global memory object identified in the original **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="4ea26-127">Todas as mensagens de **\_ \_ ACK DDE do WM** lançadas devem criar ou reutilizar o parâmetro *lParam* chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="4ea26-127">All posted **WM\_DDE\_ACK** messages must create or reuse the *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="4ea26-128">Se um aplicativo tiver iniciado o encerramento de uma conversa postando [**a \_ \_ Encerração do WM DDE**](wm-dde-terminate.md) e estiver aguardando a confirmação, o aplicativo em espera não deverá reconhecer (positiva ou negativamente) todas as mensagens subsequentes enviadas pelo outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4ea26-128">If an application has initiated the termination of a conversation by posting [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) and is awaiting confirmation, the waiting application should not acknowledge (positively or negatively) any subsequent messages sent by the other application.</span></span> <span data-ttu-id="4ea26-129">O aplicativo em espera deve excluir todos os átomos ou objetos de memória compartilhada recebidos nessas mensagens intervenientes.</span><span class="sxs-lookup"><span data-stu-id="4ea26-129">The waiting application should delete any atoms or shared memory objects received in these intervening messages.</span></span> <span data-ttu-id="4ea26-130">Os objetos de memória não devem ser liberados se o sinalizador **fRelease** estiver definido como **false** nas mensagens [**de \_ \_ dados**](wm-dde-data.md) DDE do WM e do WM DDE [**\_ \_**](wm-dde-poke.md) .</span><span class="sxs-lookup"><span data-stu-id="4ea26-130">Memory objects should not be freed if the **fRelease** flag is set to **FALSE** in [**WM\_DDE\_POKE**](wm-dde-poke.md) and [**WM\_DDE\_DATA**](wm-dde-data.md) messages.</span></span>

### <a name="receiving"></a><span data-ttu-id="4ea26-131">Recebimento</span><span class="sxs-lookup"><span data-stu-id="4ea26-131">Receiving</span></span>

<span data-ttu-id="4ea26-132">O aplicativo que recebe uma mensagem de **\_ \_ ACK DDE do WM** deve excluir todos os átomos que acompanham a mensagem.</span><span class="sxs-lookup"><span data-stu-id="4ea26-132">The application that receives a **WM\_DDE\_ACK** message should delete all atoms accompanying the message.</span></span> <span data-ttu-id="4ea26-133">Se o aplicativo receber uma **\_ \_ confirmação de DDE do WM** em resposta a uma mensagem com um objeto de memória global que o acompanha e o objeto tiver sido enviado com os sinalizadores **fRelease** definidos como **false**, o aplicativo será responsável por excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="4ea26-133">If the application receives a **WM\_DDE\_ACK** in response to a message with an accompanying global memory object, and the object was sent with the **fRelease** flags set to **FALSE**, the application is responsible for deleting the object.</span></span>

<span data-ttu-id="4ea26-134">Se o aplicativo receber uma mensagem **de \_ \_ ACK DDE do WM** negativa postada em resposta a uma mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-advise.md) , o aplicativo deverá excluir o objeto de memória global Postado com a mensagem de **\_ \_ aviso DDE do WM** original.</span><span class="sxs-lookup"><span data-stu-id="4ea26-134">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_ADVISE** message.</span></span> <span data-ttu-id="4ea26-135">Se o aplicativo receber uma mensagem **de \_ \_ ACK DDE do WM** negativa postada em resposta a uma mensagem de [**\_ \_ execução**](wm-dde-execute.md) do WM DDE [**\_ \_ Data**](wm-dde-data.md), do [**WM \_ DDE \_**](wm-dde-poke.md)ou do WM DDE, o aplicativo deverá excluir o objeto de memória global Postado com os **\_ \_ dados do WM DDE** original, o **WM \_ DDE \_** enviar ou a mensagem de **\_ \_ execução DDE do WM** .</span><span class="sxs-lookup"><span data-stu-id="4ea26-135">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_POKE**](wm-dde-poke.md), or [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_DATA**, **WM\_DDE\_POKE**, or **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="4ea26-136">O aplicativo que recebe uma mensagem **de \_ \_ ACK DDE do WM** lançada deve liberar o parâmetro *lParam* usando a função [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .</span><span class="sxs-lookup"><span data-stu-id="4ea26-136">The application that receives a posted **WM\_DDE\_ACK** message must free the *lParam* parameter by using the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ea26-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ea26-137">Requirements</span></span>



| <span data-ttu-id="4ea26-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ea26-138">Requirement</span></span> | <span data-ttu-id="4ea26-139">Valor</span><span class="sxs-lookup"><span data-stu-id="4ea26-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea26-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ea26-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4ea26-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4ea26-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4ea26-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ea26-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4ea26-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4ea26-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4ea26-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4ea26-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ea26-145"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ea26-145"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ea26-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ea26-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="4ea26-147">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4ea26-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4ea26-148">**DDEACK**</span><span class="sxs-lookup"><span data-stu-id="4ea26-148">**DDEACK**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[<span data-ttu-id="4ea26-149">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="4ea26-149">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="4ea26-150">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="4ea26-150">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="4ea26-151">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="4ea26-151">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="4ea26-152">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="4ea26-152">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="4ea26-153">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="4ea26-153">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="4ea26-154">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="4ea26-154">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="4ea26-155">**\_aviso de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="4ea26-155">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="4ea26-156">**\_dados DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="4ea26-156">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="4ea26-157">**\_execução de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="4ea26-157">**WM\_DDE\_EXECUTE**</span></span>](wm-dde-execute.md)
</dt> <dt>

[<span data-ttu-id="4ea26-158">**início do WM \_ DDE \_**</span><span class="sxs-lookup"><span data-stu-id="4ea26-158">**WM\_DDE\_INITIATE**</span></span>](wm-dde-initiate.md)
</dt> <dt>

[<span data-ttu-id="4ea26-159">**o WM \_ DDE. \_**</span><span class="sxs-lookup"><span data-stu-id="4ea26-159">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="4ea26-160">**\_solicitação de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="4ea26-160">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

[<span data-ttu-id="4ea26-161">**fim do WM \_ DDE \_**</span><span class="sxs-lookup"><span data-stu-id="4ea26-161">**WM\_DDE\_TERMINATE**</span></span>](wm-dde-terminate.md)
</dt> <dt>

[<span data-ttu-id="4ea26-162">**\_aviso de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="4ea26-162">**WM\_DDE\_UNADVISE**</span></span>](wm-dde-unadvise.md)
</dt> <dt>

<span data-ttu-id="4ea26-163">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="4ea26-163">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4ea26-164">Sobre troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="4ea26-164">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


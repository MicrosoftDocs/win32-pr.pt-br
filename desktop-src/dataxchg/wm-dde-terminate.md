---
title: Mensagem de WM_DDE_TERMINATE (DDE. h)
description: Um aplicativo troca dinâmica de dados (DDE) (cliente ou servidor) posta uma mensagem de encerramento de DDE do WM \_ \_ para encerrar uma conversa. Para postar essa mensagem, chame a função CreateMessage com os parâmetros a seguir.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- Troca de dados de mensagem WM_DDE_TERMINATE
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085430"
---
# <a name="wm_dde_terminate-message"></a><span data-ttu-id="45c8d-105">Mensagem de encerramento de \_ DDE do WM \_</span><span class="sxs-lookup"><span data-stu-id="45c8d-105">WM\_DDE\_TERMINATE message</span></span>

<span data-ttu-id="45c8d-106">Um aplicativo troca dinâmica de dados (DDE) (cliente ou servidor) posta uma mensagem de **\_ \_ encerramento de DDE do WM** para encerrar uma conversa.</span><span class="sxs-lookup"><span data-stu-id="45c8d-106">A Dynamic Data Exchange (DDE) application (client or server) posts a **WM\_DDE\_TERMINATE** message to terminate a conversation.</span></span>

<span data-ttu-id="45c8d-107">Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="45c8d-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a><span data-ttu-id="45c8d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45c8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45c8d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="45c8d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45c8d-110">Um identificador para a janela cliente ou servidor postando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="45c8d-110">A handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="45c8d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="45c8d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="45c8d-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="45c8d-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45c8d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="45c8d-113">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="45c8d-114">Lançamento</span><span class="sxs-lookup"><span data-stu-id="45c8d-114">Posting</span></span>

<span data-ttu-id="45c8d-115">Ao aguardar a confirmação do encerramento, o aplicativo de lançamento não deve postar nenhuma outra mensagem para o aplicativo de recebimento.</span><span class="sxs-lookup"><span data-stu-id="45c8d-115">While waiting for confirmation of the termination, the posting application should not post any other messages to the receiving application.</span></span> <span data-ttu-id="45c8d-116">Se o aplicativo de envio receber mensagens (diferente do **WM \_ DDE \_ Terminate**) do aplicativo de recebimento, ele deverá excluir todos os átomos ou objetos de memória compartilhados que acompanham as mensagens, exceto os objetos de memória global associados às mensagens de [**\_ \_ dados DDE**](wm-dde-data.md) do [**WM \_ \_**](wm-dde-poke.md) ou do WM que não têm o conjunto de membros **fRelease** .</span><span class="sxs-lookup"><span data-stu-id="45c8d-116">If the sending application receives messages (other than **WM\_DDE\_TERMINATE**) from the receiving application, it should delete any atoms or shared memory objects accompanying the messages, except global memory objects associated with [**WM\_DDE\_POKE**](wm-dde-poke.md) or [**WM\_DDE\_DATA**](wm-dde-data.md) messages that do not have the **fRelease** member set.</span></span>

### <a name="receiving"></a><span data-ttu-id="45c8d-117">Recebimento</span><span class="sxs-lookup"><span data-stu-id="45c8d-117">Receiving</span></span>

<span data-ttu-id="45c8d-118">O aplicativo cliente ou servidor deve responder postando uma mensagem de **\_ \_ encerramento de DDE do WM** .</span><span class="sxs-lookup"><span data-stu-id="45c8d-118">The client or server application should respond by posting a **WM\_DDE\_TERMINATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="45c8d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45c8d-119">Requirements</span></span>



| <span data-ttu-id="45c8d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="45c8d-120">Requirement</span></span> | <span data-ttu-id="45c8d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="45c8d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45c8d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45c8d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="45c8d-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="45c8d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="45c8d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45c8d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="45c8d-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="45c8d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="45c8d-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="45c8d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="45c8d-127"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45c8d-127"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45c8d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="45c8d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="45c8d-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="45c8d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="45c8d-130">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="45c8d-130">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="45c8d-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="45c8d-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="45c8d-132">**\_dados DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="45c8d-132">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="45c8d-133">**o WM \_ DDE. \_**</span><span class="sxs-lookup"><span data-stu-id="45c8d-133">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

<span data-ttu-id="45c8d-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="45c8d-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="45c8d-135">Sobre troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="45c8d-135">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


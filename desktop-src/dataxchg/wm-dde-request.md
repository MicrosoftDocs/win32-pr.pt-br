---
title: Mensagem de WM_DDE_REQUEST (DDE. h)
description: Um aplicativo cliente troca dinâmica de dados (DDE) posta uma \_ mensagem de solicitação de DDE do WM \_ em um aplicativo de servidor DDE para solicitar o valor de um item de dados. Para postar essa mensagem, chame a função CreateMessage com os parâmetros a seguir.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- Troca de dados de mensagem WM_DDE_REQUEST
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644546"
---
# <a name="wm_dde_request-message"></a><span data-ttu-id="f0e7f-105">Mensagem de solicitação de \_ DDE do WM \_</span><span class="sxs-lookup"><span data-stu-id="f0e7f-105">WM\_DDE\_REQUEST message</span></span>

<span data-ttu-id="f0e7f-106">Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de **\_ \_ solicitação de DDE do WM** em um aplicativo de servidor DDE para solicitar o valor de um item de dados.</span><span class="sxs-lookup"><span data-stu-id="f0e7f-106">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_REQUEST** message to a DDE server application to request the value of a data item.</span></span>

<span data-ttu-id="f0e7f-107">Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="f0e7f-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a><span data-ttu-id="f0e7f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0e7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0e7f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0e7f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0e7f-110">Um identificador para a janela do cliente que está enviando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="f0e7f-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="f0e7f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0e7f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0e7f-112">A palavra de ordem inferior Especifica um formato de área de transferência padrão ou registrado.</span><span class="sxs-lookup"><span data-stu-id="f0e7f-112">The low-order word specifies a standard or registered clipboard format.</span></span>

<span data-ttu-id="f0e7f-113">A palavra de ordem superior contém um Atom que identifica o item de dados solicitado do servidor.</span><span class="sxs-lookup"><span data-stu-id="f0e7f-113">The high-order word contains an atom that identifies the data item requested from the server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0e7f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0e7f-114">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="f0e7f-115">Lançamento</span><span class="sxs-lookup"><span data-stu-id="f0e7f-115">Posting</span></span>

<span data-ttu-id="f0e7f-116">O aplicativo cliente aloca o Atom chamando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="f0e7f-116">The client application allocates the atom by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="f0e7f-117">Recebimento</span><span class="sxs-lookup"><span data-stu-id="f0e7f-117">Receiving</span></span>

<span data-ttu-id="f0e7f-118">Se o aplicativo receptor (servidor) puder atender à solicitação, ele responderá com uma mensagem de [**\_ \_ dados DDE do WM**](wm-dde-data.md) contendo os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="f0e7f-118">If the receiving (server) application can satisfy the request, it responds with a [**WM\_DDE\_DATA**](wm-dde-data.md) message containing the requested data.</span></span> <span data-ttu-id="f0e7f-119">Caso contrário, ele responde com uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa.</span><span class="sxs-lookup"><span data-stu-id="f0e7f-119">Otherwise, it responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="f0e7f-120">Ao responder com uma mensagem do [**WM DDE \_ \_ Data**](wm-dde-data.md) ou do [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , o aplicativo de servidor pode reutilizar o Atom ou pode excluir o Atom e criar um novo.</span><span class="sxs-lookup"><span data-stu-id="f0e7f-120">When responding with either a [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the server application can either reuse the atom or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e7f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0e7f-121">Requirements</span></span>



| <span data-ttu-id="f0e7f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0e7f-122">Requirement</span></span> | <span data-ttu-id="f0e7f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f0e7f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e7f-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0e7f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f0e7f-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f0e7f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f0e7f-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0e7f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f0e7f-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f0e7f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f0e7f-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f0e7f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0e7f-129"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0e7f-129"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0e7f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0e7f-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="f0e7f-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="f0e7f-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f0e7f-132">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="f0e7f-132">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="f0e7f-133">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f0e7f-133">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="f0e7f-134">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="f0e7f-134">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="f0e7f-135">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f0e7f-135">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="f0e7f-136">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="f0e7f-136">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="f0e7f-137">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f0e7f-137">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="f0e7f-138">**\_ACK de DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f0e7f-138">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="f0e7f-139">**\_dados DDE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f0e7f-139">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

<span data-ttu-id="f0e7f-140">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="f0e7f-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f0e7f-141">Sobre troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="f0e7f-141">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 


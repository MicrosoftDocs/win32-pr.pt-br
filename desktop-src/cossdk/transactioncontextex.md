---
description: Cria um objeto transacional genérico que inicia uma transação. Ao chamar os métodos dessa classe, você pode compor o trabalho de vários objetos COM em uma única transação e confirmar explicitamente ou anular a transação.
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: Classe TransactionContextEx (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 8cf5c3aaa7ffe126124a909498a7c54cfb012c65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646484"
---
# <a name="transactioncontextex-class"></a><span data-ttu-id="21321-104">Classe TransactionContextEx</span><span class="sxs-lookup"><span data-stu-id="21321-104">TransactionContextEx class</span></span>

<span data-ttu-id="21321-105">Cria um objeto transacional genérico que inicia uma transação.</span><span class="sxs-lookup"><span data-stu-id="21321-105">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="21321-106">Ao chamar os métodos dessa classe, você pode compor o trabalho de vários objetos COM em uma única transação e confirmar explicitamente ou anular a transação.</span><span class="sxs-lookup"><span data-stu-id="21321-106">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="21321-107">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="21321-107">When to implement</span></span>

<span data-ttu-id="21321-108">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="21321-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="21321-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="21321-109">Requirement</span></span> | <span data-ttu-id="21321-110">Valor</span><span class="sxs-lookup"><span data-stu-id="21321-110">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="21321-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="21321-111">CLSID</span></span>      | <span data-ttu-id="21321-112">\_TRANSACTIONCONTEXTEX CLSID</span><span class="sxs-lookup"><span data-stu-id="21321-112">CLSID\_TransactionContextEx</span></span>                            |
| <span data-ttu-id="21321-113">ProgID</span><span class="sxs-lookup"><span data-stu-id="21321-113">ProgID</span></span>     | <span data-ttu-id="21321-114">L "TxCTx. TransactionContextEx"</span><span class="sxs-lookup"><span data-stu-id="21321-114">L"TxCTx.TransactionContextEx"</span></span>                          |
| <span data-ttu-id="21321-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="21321-115">Interfaces</span></span> | [<span data-ttu-id="21321-116">**ITransactionContextEx**</span><span class="sxs-lookup"><span data-stu-id="21321-116">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a><span data-ttu-id="21321-117">Quando usar</span><span class="sxs-lookup"><span data-stu-id="21321-117">When to use</span></span>

<span data-ttu-id="21321-118">Um cliente não transacional usa essa classe para iniciar uma transação.</span><span class="sxs-lookup"><span data-stu-id="21321-118">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="21321-119">Usando os métodos dessa classe, o cliente pode chamar objetos COM adicionais que, se configurados para participar de uma transação, são executados dentro do limite de transação do objeto de contexto de transação.</span><span class="sxs-lookup"><span data-stu-id="21321-119">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="21321-120">Com base em sua lógica de negócios, o cliente pode confirmar ou anular explicitamente a transação.</span><span class="sxs-lookup"><span data-stu-id="21321-120">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="21321-121">A classe **TransactionContextEx** limita a reutilização da lógica de negócios que orienta a transação.</span><span class="sxs-lookup"><span data-stu-id="21321-121">The **TransactionContextEx** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="21321-122">Por esse motivo, é recomendável que os objetos instanciados da classe **TransactionContextEx** sejam usados com moderação.</span><span class="sxs-lookup"><span data-stu-id="21321-122">For this reason, it is recommended that objects instantiated from the **TransactionContextEx** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="21321-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="21321-123">Remarks</span></span>

<span data-ttu-id="21321-124">Para criar esse objeto, chame [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="21321-124">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="21321-125">A classe **TransactionContextEx** não foi projetada para ser usada em Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="21321-125">The **TransactionContextEx** class was not designed to be used in Visual Basic.</span></span> <span data-ttu-id="21321-126">Em vez disso, use a classe [**TransactionContext**](transactioncontext.md) .</span><span class="sxs-lookup"><span data-stu-id="21321-126">Use the [**TransactionContext**](transactioncontext.md) class instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="21321-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21321-127">Requirements</span></span>



| <span data-ttu-id="21321-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="21321-128">Requirement</span></span> | <span data-ttu-id="21321-129">Valor</span><span class="sxs-lookup"><span data-stu-id="21321-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="21321-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21321-130">Minimum supported client</span></span><br/> | <span data-ttu-id="21321-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="21321-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="21321-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21321-132">Minimum supported server</span></span><br/> | <span data-ttu-id="21321-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="21321-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="21321-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="21321-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="21321-135"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="21321-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21321-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="21321-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21321-137">Configurando transações</span><span class="sxs-lookup"><span data-stu-id="21321-137">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="21321-138">**ITransactionContextEx**</span><span class="sxs-lookup"><span data-stu-id="21321-138">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[<span data-ttu-id="21321-139">**TransactionContext**</span><span class="sxs-lookup"><span data-stu-id="21321-139">**TransactionContext**</span></span>](transactioncontext.md)
</dt> </dl>

 

 





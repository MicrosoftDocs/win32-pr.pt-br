---
description: Cria um objeto transacional genérico que inicia uma transação.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: Classe TransactionContext (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: 595b5a3192b87420855eb43f1e1e33df37a45c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164137"
---
# <a name="transactioncontext-class"></a><span data-ttu-id="06748-103">Classe TransactionContext</span><span class="sxs-lookup"><span data-stu-id="06748-103">TransactionContext class</span></span>

<span data-ttu-id="06748-104">Cria um objeto transacional genérico que inicia uma transação.</span><span class="sxs-lookup"><span data-stu-id="06748-104">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="06748-105">Ao chamar os métodos dessa classe, você pode compor o trabalho de vários objetos COM em uma única transação e confirmar explicitamente ou anular a transação.</span><span class="sxs-lookup"><span data-stu-id="06748-105">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="06748-106">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="06748-106">When to implement</span></span>

<span data-ttu-id="06748-107">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="06748-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="06748-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="06748-108">Requirement</span></span> | <span data-ttu-id="06748-109">Valor</span><span class="sxs-lookup"><span data-stu-id="06748-109">Value</span></span> |
|------------|----------------------------------------------------|
| <span data-ttu-id="06748-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="06748-110">CLSID</span></span>      | <span data-ttu-id="06748-111">\_TRANSACTIONCONTEXT CLSID</span><span class="sxs-lookup"><span data-stu-id="06748-111">CLSID\_TransactionContext</span></span>                          |
| <span data-ttu-id="06748-112">ProgID</span><span class="sxs-lookup"><span data-stu-id="06748-112">ProgID</span></span>     | <span data-ttu-id="06748-113">L "TxCTx. TransactionContext"</span><span class="sxs-lookup"><span data-stu-id="06748-113">L"TxCTx.TransactionContext"</span></span>                        |
| <span data-ttu-id="06748-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="06748-114">Interfaces</span></span> | [<span data-ttu-id="06748-115">**ITransactionContext**</span><span class="sxs-lookup"><span data-stu-id="06748-115">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a><span data-ttu-id="06748-116">Quando usar</span><span class="sxs-lookup"><span data-stu-id="06748-116">When to use</span></span>

<span data-ttu-id="06748-117">Um cliente não transacional usa essa classe para iniciar uma transação.</span><span class="sxs-lookup"><span data-stu-id="06748-117">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="06748-118">Usando os métodos dessa classe, o cliente pode chamar objetos COM adicionais que, se configurados para participar de uma transação, são executados dentro do limite de transação do objeto de contexto de transação.</span><span class="sxs-lookup"><span data-stu-id="06748-118">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="06748-119">Com base em sua lógica de negócios, o cliente pode confirmar ou anular explicitamente a transação.</span><span class="sxs-lookup"><span data-stu-id="06748-119">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="06748-120">A classe **TransactionContext** limita a reutilização da lógica de negócios que orienta a transação.</span><span class="sxs-lookup"><span data-stu-id="06748-120">The **TransactionContext** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="06748-121">Por esse motivo, é recomendável que os objetos instanciados da classe **TransactionContext** sejam usados com moderação.</span><span class="sxs-lookup"><span data-stu-id="06748-121">For this reason, it is recommended that objects instantiated from the **TransactionContext** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="06748-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="06748-122">Remarks</span></span>

<span data-ttu-id="06748-123">Para criar esse objeto, chame [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="06748-123">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="06748-124">Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="06748-124">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="06748-125">Um objeto TransactionContext pode ser declarado usando "COMSVCSLib. TransactionContext" como o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="06748-125">A TransactionContext object can be declared using "COMSVCSLib.TransactionContext" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="06748-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06748-126">Requirements</span></span>



| <span data-ttu-id="06748-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="06748-127">Requirement</span></span> | <span data-ttu-id="06748-128">Valor</span><span class="sxs-lookup"><span data-stu-id="06748-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="06748-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06748-129">Minimum supported client</span></span><br/> | <span data-ttu-id="06748-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06748-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="06748-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06748-131">Minimum supported server</span></span><br/> | <span data-ttu-id="06748-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="06748-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="06748-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="06748-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="06748-134"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="06748-134"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06748-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="06748-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06748-136">Configurando transações</span><span class="sxs-lookup"><span data-stu-id="06748-136">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="06748-137">**ITransactionContext**</span><span class="sxs-lookup"><span data-stu-id="06748-137">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[<span data-ttu-id="06748-138">**TransactionContextEx**</span><span class="sxs-lookup"><span data-stu-id="06748-138">**TransactionContextEx**</span></span>](transactioncontextex.md)
</dt> </dl>

 

 





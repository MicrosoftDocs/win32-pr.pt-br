---
description: Fornece acesso a propriedades de objeto de contexto relacionadas a transações.
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: Interface IContextTransactionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 499ab2371eda6dda6512b5fddb097d3adc2a6f05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457054"
---
# <a name="icontexttransactioninfo-interface"></a><span data-ttu-id="68513-103">Interface IContextTransactionInfo</span><span class="sxs-lookup"><span data-stu-id="68513-103">IContextTransactionInfo interface</span></span>

<span data-ttu-id="68513-104">Fornece acesso a propriedades de objeto de contexto relacionadas a transações.</span><span class="sxs-lookup"><span data-stu-id="68513-104">Provides access to context object properties that relate to transactions.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="68513-105">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="68513-105">When to implement</span></span>

<span data-ttu-id="68513-106">Você não deve implementar essa interface.</span><span class="sxs-lookup"><span data-stu-id="68513-106">You should not implement this interface.</span></span> <span data-ttu-id="68513-107">A implementação padrão fornece a funcionalidade completa.</span><span class="sxs-lookup"><span data-stu-id="68513-107">The standard implementation provides complete functionality.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="68513-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="68513-108">When to use</span></span>

<span data-ttu-id="68513-109">Use essa interface para acessar propriedades de objeto de contexto relacionadas a transações.</span><span class="sxs-lookup"><span data-stu-id="68513-109">Use this interface to access context object properties that relate to transactions.</span></span>

## <a name="members"></a><span data-ttu-id="68513-110">Membros</span><span class="sxs-lookup"><span data-stu-id="68513-110">Members</span></span>

<span data-ttu-id="68513-111">A interface **IContextTransactionInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="68513-111">The **IContextTransactionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="68513-112">**IContextTransactionInfo** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="68513-112">**IContextTransactionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="68513-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="68513-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="68513-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="68513-114">Methods</span></span>

<span data-ttu-id="68513-115">A interface **IContextTransactionInfo** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="68513-115">The **IContextTransactionInfo** interface has these methods.</span></span>



| <span data-ttu-id="68513-116">Método</span><span class="sxs-lookup"><span data-stu-id="68513-116">Method</span></span>                                                                                         | <span data-ttu-id="68513-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="68513-117">Description</span></span>                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68513-118">**FetchTransaction**</span><span class="sxs-lookup"><span data-stu-id="68513-118">**FetchTransaction**</span></span>](icontexttransactioninfo-registertransactionproxy.md)                   | <span data-ttu-id="68513-119">Recupera a transação ou o proxy de transação que está associado ao contexto atual, se houver.</span><span class="sxs-lookup"><span data-stu-id="68513-119">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span><br/>              |
| [<span data-ttu-id="68513-120">**GetTxIsolationLevelAndTimeout**</span><span class="sxs-lookup"><span data-stu-id="68513-120">**GetTxIsolationLevelAndTimeout**</span></span>](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | <span data-ttu-id="68513-121">Recupera o nível de isolamento e o valor de tempo limite de uma transação hospedada no contexto de transação raiz.</span><span class="sxs-lookup"><span data-stu-id="68513-121">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span><br/> |
| [<span data-ttu-id="68513-122">**RegisterTransactionProxy**</span><span class="sxs-lookup"><span data-stu-id="68513-122">**RegisterTransactionProxy**</span></span>](icontexttransactioninfo-fetchtransaction.md)                   | <span data-ttu-id="68513-123">Associa uma implementação de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) com o contexto atual.</span><span class="sxs-lookup"><span data-stu-id="68513-123">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="68513-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68513-124">Requirements</span></span>



| <span data-ttu-id="68513-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="68513-125">Requirement</span></span> | <span data-ttu-id="68513-126">Valor</span><span class="sxs-lookup"><span data-stu-id="68513-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="68513-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68513-127">Minimum supported client</span></span><br/> | <span data-ttu-id="68513-128">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="68513-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="68513-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68513-129">Minimum supported server</span></span><br/> | <span data-ttu-id="68513-130">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="68513-130">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



 


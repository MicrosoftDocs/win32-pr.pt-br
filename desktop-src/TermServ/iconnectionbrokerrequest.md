---
title: Interface IConnectionBrokerRequest (Cbclient. h)
description: Fornece os métodos necessários para obter os resultados do método assíncrono IConnectionBrokerClient GetTargetInfo.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IConnectionBrokerRequest
- Serviços de Área de Trabalho Remota da interface IConnectionBrokerRequest, descrita
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645190"
---
# <a name="iconnectionbrokerrequest-interface"></a><span data-ttu-id="ddf7a-105">Interface IConnectionBrokerRequest</span><span class="sxs-lookup"><span data-stu-id="ddf7a-105">IConnectionBrokerRequest interface</span></span>

<span data-ttu-id="ddf7a-106">Fornece os métodos necessários para obter os resultados do método assíncrona [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="ddf7a-106">Provides the methods needed to obtain the results of the asynchronous [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

<span data-ttu-id="ddf7a-107">Essa interface é implementada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="ddf7a-107">This interface is implemented by the system.</span></span> <span data-ttu-id="ddf7a-108">Uma instância dessa interface é fornecida ao chamador com o método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="ddf7a-108">An instance of this interface is provided to the caller with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="ddf7a-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ddf7a-109">Members</span></span>

<span data-ttu-id="ddf7a-110">A interface **IConnectionBrokerRequest** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ddf7a-110">The **IConnectionBrokerRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ddf7a-111">**IConnectionBrokerRequest** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ddf7a-111">**IConnectionBrokerRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="ddf7a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ddf7a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ddf7a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ddf7a-113">Methods</span></span>

<span data-ttu-id="ddf7a-114">A interface **IConnectionBrokerRequest** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ddf7a-114">The **IConnectionBrokerRequest** interface has these methods.</span></span>



| <span data-ttu-id="ddf7a-115">Método</span><span class="sxs-lookup"><span data-stu-id="ddf7a-115">Method</span></span>                                                      | <span data-ttu-id="ddf7a-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ddf7a-116">Description</span></span>                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="ddf7a-117">**CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="ddf7a-117">**CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md) | <span data-ttu-id="ddf7a-118">Chamado para determinar o status de uma solicitação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ddf7a-118">Called to determine the status of an asynchronous request.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ddf7a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddf7a-119">Requirements</span></span>



| <span data-ttu-id="ddf7a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddf7a-120">Requirement</span></span> | <span data-ttu-id="ddf7a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ddf7a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf7a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ddf7a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ddf7a-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ddf7a-123">Windows 8</span></span><br/>                                                                        |
| <span data-ttu-id="ddf7a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ddf7a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ddf7a-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ddf7a-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="ddf7a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ddf7a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddf7a-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddf7a-127"><dt>Cbclient.h</dt></span></span> </dl>       |
| <span data-ttu-id="ddf7a-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ddf7a-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="ddf7a-129"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddf7a-129"><dt>Cbclient.lib</dt></span></span> </dl>     |
| <span data-ttu-id="ddf7a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ddf7a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddf7a-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddf7a-131"><dt>Cbclient.dll</dt></span></span> </dl>     |
| <span data-ttu-id="ddf7a-132">IID</span><span class="sxs-lookup"><span data-stu-id="ddf7a-132">IID</span></span><br/>                      | <span data-ttu-id="ddf7a-133">IID \_ IConnectionBrokerRequest é definido como 25114427-ED5D-46A6-AF53-C62D33A4108E</span><span class="sxs-lookup"><span data-stu-id="ddf7a-133">IID\_IConnectionBrokerRequest is defined as 25114427-ED5D-46A6-AF53-C62D33A4108E</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ddf7a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddf7a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf7a-135">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="ddf7a-135">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 


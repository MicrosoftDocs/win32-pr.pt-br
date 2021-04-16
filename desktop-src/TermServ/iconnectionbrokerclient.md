---
title: Interface IConnectionBrokerClient (Cbclient. h)
description: Fornece os métodos necessários para usar o cliente do agente do Conexão de Área de Trabalho Remota.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IConnectionBrokerClient
- Serviços de Área de Trabalho Remota da interface IConnectionBrokerClient, descrita
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a062059f7aa1f16e32514b3bacbfb31dc0a350f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455871"
---
# <a name="iconnectionbrokerclient-interface"></a><span data-ttu-id="6fc11-105">Interface IConnectionBrokerClient</span><span class="sxs-lookup"><span data-stu-id="6fc11-105">IConnectionBrokerClient interface</span></span>

<span data-ttu-id="6fc11-106">Fornece os métodos necessários para usar o cliente do agente do Conexão de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="6fc11-106">Provides the methods needed to use the Remote Desktop Connection Broker client.</span></span>

<span data-ttu-id="6fc11-107">Essa interface é implementada pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="6fc11-107">This interface is implemented by the system.</span></span> <span data-ttu-id="6fc11-108">Para obter uma instância dessa interface, use a função [**CBCreateClientInstance**](cbcreateclientinstance.md) .</span><span class="sxs-lookup"><span data-stu-id="6fc11-108">To obtain an instance of this interface, use the [**CBCreateClientInstance**](cbcreateclientinstance.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="6fc11-109">Membros</span><span class="sxs-lookup"><span data-stu-id="6fc11-109">Members</span></span>

<span data-ttu-id="6fc11-110">A interface **IConnectionBrokerClient** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6fc11-110">The **IConnectionBrokerClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6fc11-111">**IConnectionBrokerClient** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6fc11-111">**IConnectionBrokerClient** also has these types of members:</span></span>

-   [<span data-ttu-id="6fc11-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6fc11-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6fc11-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="6fc11-113">Methods</span></span>

<span data-ttu-id="6fc11-114">A interface **IConnectionBrokerClient** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6fc11-114">The **IConnectionBrokerClient** interface has these methods.</span></span>



| <span data-ttu-id="6fc11-115">Método</span><span class="sxs-lookup"><span data-stu-id="6fc11-115">Method</span></span>                                                         | <span data-ttu-id="6fc11-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fc11-116">Description</span></span>                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6fc11-117">**GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="6fc11-117">**GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md) | <span data-ttu-id="6fc11-118">Solicita informações sobre o computador de destino onde a conexão deve ser redirecionada.</span><span class="sxs-lookup"><span data-stu-id="6fc11-118">Requests information about the target computer where the connection should be redirected.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6fc11-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fc11-119">Requirements</span></span>



| <span data-ttu-id="6fc11-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fc11-120">Requirement</span></span> | <span data-ttu-id="6fc11-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6fc11-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc11-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fc11-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc11-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6fc11-123">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="6fc11-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fc11-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc11-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6fc11-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="6fc11-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fc11-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc11-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fc11-127"><dt>Cbclient.h</dt></span></span> </dl>      |
| <span data-ttu-id="6fc11-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6fc11-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="6fc11-129"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fc11-129"><dt>Cbclient.lib</dt></span></span> </dl>    |
| <span data-ttu-id="6fc11-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6fc11-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fc11-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fc11-131"><dt>Cbclient.dll</dt></span></span> </dl>    |
| <span data-ttu-id="6fc11-132">IID</span><span class="sxs-lookup"><span data-stu-id="6fc11-132">IID</span></span><br/>                      | <span data-ttu-id="6fc11-133">IID \_ IConnectionBrokerClient é definido como D6818DF2-8338-4EB7-AD77-DE210817987C</span><span class="sxs-lookup"><span data-stu-id="6fc11-133">IID\_IConnectionBrokerClient is defined as D6818DF2-8338-4EB7-AD77-DE210817987C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6fc11-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fc11-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fc11-135">**CBCreateClientInstance**</span><span class="sxs-lookup"><span data-stu-id="6fc11-135">**CBCreateClientInstance**</span></span>](cbcreateclientinstance.md)
</dt> </dl>

 


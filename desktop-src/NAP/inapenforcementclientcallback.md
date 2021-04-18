---
title: Interface INapEnforcementClientCallback (NapEnforcementClient. h)
description: Os clientes de imposição devem implementar o para permitir que o NapAgent se comunique com eles.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- INapEnforcementClientCallback da interface NAP
- INapEnforcementClientCallback interface NAP, descrita
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d5c7e066115a6d51879775d9b8cfab3cbe4888
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780618"
---
# <a name="inapenforcementclientcallback-interface"></a><span data-ttu-id="d6ad0-105">Interface INapEnforcementClientCallback</span><span class="sxs-lookup"><span data-stu-id="d6ad0-105">INapEnforcementClientCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="d6ad0-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="d6ad0-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d6ad0-107">A interface **INapEnforcementClientCallback** fornece métodos de retorno de chamada que os clientes de imposição devem implementar para permitir que o NapAgent se comunique com eles.</span><span class="sxs-lookup"><span data-stu-id="d6ad0-107">The **INapEnforcementClientCallback** interface provides callback methods that enforcement clients must implement to enable the NapAgent to communicate with them.</span></span>

## <a name="members"></a><span data-ttu-id="d6ad0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d6ad0-108">Members</span></span>

<span data-ttu-id="d6ad0-109">A interface **INapEnforcementClientCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d6ad0-109">The **INapEnforcementClientCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d6ad0-110">**INapEnforcementClientCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d6ad0-110">**INapEnforcementClientCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="d6ad0-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d6ad0-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d6ad0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d6ad0-112">Methods</span></span>

<span data-ttu-id="d6ad0-113">A interface **INapEnforcementClientCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d6ad0-113">The **INapEnforcementClientCallback** interface has these methods.</span></span>



| <span data-ttu-id="d6ad0-114">Método</span><span class="sxs-lookup"><span data-stu-id="d6ad0-114">Method</span></span>                                                                                                         | <span data-ttu-id="d6ad0-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6ad0-115">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="d6ad0-116">**INapEnforcementClientCallback:: GetConnections**</span><span class="sxs-lookup"><span data-stu-id="d6ad0-116">**INapEnforcementClientCallback::GetConnections**</span></span>](inapenforcementclientcallback-getconnections-method.md)   | <span data-ttu-id="d6ad0-117">Usado pelo NapAgent para recuperar conexões.</span><span class="sxs-lookup"><span data-stu-id="d6ad0-117">Used by the NapAgent to retrieve connections.</span></span><br/>                         |
| [<span data-ttu-id="d6ad0-118">**INapEnforcementClientCallback::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="d6ad0-118">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md) | <span data-ttu-id="d6ad0-119">Usado pelo NapAgent para informar o cliente de imposição de alterações SoH.</span><span class="sxs-lookup"><span data-stu-id="d6ad0-119">Used by the NapAgent to inform the enforcement client of SoH changes.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d6ad0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6ad0-120">Requirements</span></span>



| <span data-ttu-id="d6ad0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6ad0-121">Requirement</span></span> | <span data-ttu-id="d6ad0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d6ad0-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ad0-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6ad0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d6ad0-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6ad0-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d6ad0-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6ad0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d6ad0-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6ad0-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d6ad0-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6ad0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6ad0-128"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6ad0-128"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6ad0-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="d6ad0-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6ad0-130"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6ad0-130"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



 


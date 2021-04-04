---
title: Interface INapEnforcementClientConnection2 (NapEnforcementClient. h)
description: Permitir o gerenciamento de conexão do cliente. | Interface INapEnforcementClientConnection2 (NapEnforcementClient. h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- INapEnforcementClientConnection2 da interface NAP
- INapEnforcementClientConnection2 interface NAP, descrita
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3503e1bf6db01920e814b96e3daf5fe04eabc6b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837751"
---
# <a name="inapenforcementclientconnection2-interface"></a><span data-ttu-id="caf16-106">Interface INapEnforcementClientConnection2</span><span class="sxs-lookup"><span data-stu-id="caf16-106">INapEnforcementClientConnection2 interface</span></span>

> [!Note]  
> <span data-ttu-id="caf16-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="caf16-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="caf16-108">O **INapEnforcementClientConnection2** fornece métodos que permitem o gerenciamento de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="caf16-108">The **INapEnforcementClientConnection2** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="caf16-109">Essa interface herda todos os métodos de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) e deve ser usada em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="caf16-109">This interface inherits all the methods of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="caf16-110">Membros</span><span class="sxs-lookup"><span data-stu-id="caf16-110">Members</span></span>

<span data-ttu-id="caf16-111">A interface **INapEnforcementClientConnection2** herda de [**INapEnforcementClientConnection**](inapenforcementclientconnection.md).</span><span class="sxs-lookup"><span data-stu-id="caf16-111">The **INapEnforcementClientConnection2** interface inherits from [**INapEnforcementClientConnection**](inapenforcementclientconnection.md).</span></span> <span data-ttu-id="caf16-112">**INapEnforcementClientConnection2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="caf16-112">**INapEnforcementClientConnection2** also has these types of members:</span></span>

-   [<span data-ttu-id="caf16-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="caf16-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="caf16-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="caf16-114">Methods</span></span>

<span data-ttu-id="caf16-115">A interface **INapEnforcementClientConnection2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="caf16-115">The **INapEnforcementClientConnection2** interface has these methods.</span></span>



| <span data-ttu-id="caf16-116">Método</span><span class="sxs-lookup"><span data-stu-id="caf16-116">Method</span></span>                                                                                                              | <span data-ttu-id="caf16-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="caf16-117">Description</span></span>                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="caf16-118">**INapEnforcementClientConnection2::GetInstalledShvs**</span><span class="sxs-lookup"><span data-stu-id="caf16-118">**INapEnforcementClientConnection2::GetInstalledShvs**</span></span>](inapenforcementclientconnection2-getinstalledshvs.md)     | <span data-ttu-id="caf16-119">Usado para obter as IDs dos SHVs instalados para o cliente.</span><span class="sxs-lookup"><span data-stu-id="caf16-119">Used to get the IDs of the installed SHVs for the client.</span></span><br/>             |
| [<span data-ttu-id="caf16-120">**INapEnforcementClientConnection2::GetIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="caf16-120">**INapEnforcementClientConnection2::GetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-getisolationinfoex.md) | <span data-ttu-id="caf16-121">Usado para obter as informações de isolamento para o cliente.</span><span class="sxs-lookup"><span data-stu-id="caf16-121">Used to get the isolation information for the client.</span></span><br/>                 |
| [<span data-ttu-id="caf16-122">**INapEnforcementClientConnection2::SetInstalledShvs**</span><span class="sxs-lookup"><span data-stu-id="caf16-122">**INapEnforcementClientConnection2::SetInstalledShvs**</span></span>](inapenforcementclientconnection2-setinstalledshvs.md)     | <span data-ttu-id="caf16-123">Usado pelo NapAgent para definir as IDs SHV instaladas para o cliente.</span><span class="sxs-lookup"><span data-stu-id="caf16-123">Used by the NapAgent to set the installed SHV IDs for the client.</span></span><br/>     |
| [<span data-ttu-id="caf16-124">**INapEnforcementClientConnection2::SetIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="caf16-124">**INapEnforcementClientConnection2::SetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-setisolationinfoex.md) | <span data-ttu-id="caf16-125">Usado pelo NapAgent para definir as informações de isolamento para o cliente.</span><span class="sxs-lookup"><span data-stu-id="caf16-125">Used by the NapAgent to set the isolation information for the client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="caf16-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="caf16-126">Requirements</span></span>



| <span data-ttu-id="caf16-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="caf16-127">Requirement</span></span> | <span data-ttu-id="caf16-128">Valor</span><span class="sxs-lookup"><span data-stu-id="caf16-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf16-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="caf16-129">Minimum supported client</span></span><br/> | <span data-ttu-id="caf16-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="caf16-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="caf16-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="caf16-131">Minimum supported server</span></span><br/> | <span data-ttu-id="caf16-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="caf16-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="caf16-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="caf16-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="caf16-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="caf16-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="caf16-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="caf16-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="caf16-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="caf16-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="caf16-137">DLL</span><span class="sxs-lookup"><span data-stu-id="caf16-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caf16-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caf16-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="caf16-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="caf16-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf16-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="caf16-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> <dt>

[<span data-ttu-id="caf16-141">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="caf16-141">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="caf16-142">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="caf16-142">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 






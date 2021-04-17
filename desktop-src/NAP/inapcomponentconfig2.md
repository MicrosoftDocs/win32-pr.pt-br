---
title: Interface INapComponentConfig2 (NapCommon. h)
description: Fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema) para configurar uma interface de usuário do servidor de diretivas de rede (NPS) remotamente.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- INapComponentConfig2 da interface NAP
- INapComponentConfig2 interface NAP, descrita
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bd6fbea7696d0e4d5eacefd028ce7d33e549e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755338"
---
# <a name="inapcomponentconfig2-interface"></a><span data-ttu-id="d0b7e-105">Interface INapComponentConfig2</span><span class="sxs-lookup"><span data-stu-id="d0b7e-105">INapComponentConfig2 interface</span></span>

> [!Note]  
> <span data-ttu-id="d0b7e-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="d0b7e-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d0b7e-107">A interface **INapComponentConfig2** fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema) para configurar uma interface de usuário do servidor de diretivas de rede (NPS) remotamente.</span><span class="sxs-lookup"><span data-stu-id="d0b7e-107">The **INapComponentConfig2** interface provides NAP system configuration methods for system health validators (SHVs) to configure a network policy server (NPS) user interface remotely.</span></span>

> [!Note]  
> <span data-ttu-id="d0b7e-108">Essa interface herda todos os métodos de [**INapComponentConfig**](inapcomponentconfig.md) e deve ser usada em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="d0b7e-108">This interface inherits all the methods of [**INapComponentConfig**](inapcomponentconfig.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="d0b7e-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d0b7e-109">Members</span></span>

<span data-ttu-id="d0b7e-110">A interface **INapComponentConfig2** herda de [**INapComponentConfig**](inapcomponentconfig.md).</span><span class="sxs-lookup"><span data-stu-id="d0b7e-110">The **INapComponentConfig2** interface inherits from [**INapComponentConfig**](inapcomponentconfig.md).</span></span> <span data-ttu-id="d0b7e-111">**INapComponentConfig2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d0b7e-111">**INapComponentConfig2** also has these types of members:</span></span>

-   [<span data-ttu-id="d0b7e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d0b7e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d0b7e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d0b7e-113">Methods</span></span>

<span data-ttu-id="d0b7e-114">A interface **INapComponentConfig2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d0b7e-114">The **INapComponentConfig2** interface has these methods.</span></span>



| <span data-ttu-id="d0b7e-115">Método</span><span class="sxs-lookup"><span data-stu-id="d0b7e-115">Method</span></span>                                                                                                | <span data-ttu-id="d0b7e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0b7e-116">Description</span></span>                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0b7e-117">**INapComponentConfig2::InvokeUIForMachine**</span><span class="sxs-lookup"><span data-stu-id="d0b7e-117">**INapComponentConfig2::InvokeUIForMachine**</span></span>](inapcomponentconfig2-invokeuiformachine.md)           | <span data-ttu-id="d0b7e-118">Implementado por SHVs conforme necessário para gerenciar a configuração remota diretamente no computador especificado.</span><span class="sxs-lookup"><span data-stu-id="d0b7e-118">Implemented by SHVs as needed to manage remote configuration directly on the machine specified.</span></span><br/>                                                                 |
| [<span data-ttu-id="d0b7e-119">**INapComponentConfig2::InvokeUIFromConfigBlob**</span><span class="sxs-lookup"><span data-stu-id="d0b7e-119">**INapComponentConfig2::InvokeUIFromConfigBlob**</span></span>](inapcomponentconfig2-invokeuifromconfigblob.md)   | <span data-ttu-id="d0b7e-120">Implementado por SHVs conforme necessário para carregar a configuração do computador remoto na memória e para exibir uma interface do usuário que permite a manipulação dos dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="d0b7e-120">Implemented by SHVs as needed to load the configuration of the remote machine in memory and to display a UI that allows manipulation of the configuration data.</span></span><br/> |
| [<span data-ttu-id="d0b7e-121">**INapComponentConfig2::IsRemoteConfigSupported**</span><span class="sxs-lookup"><span data-stu-id="d0b7e-121">**INapComponentConfig2::IsRemoteConfigSupported**</span></span>](inapcomponentconfig2-isremoteconfigsupported.md) | <span data-ttu-id="d0b7e-122">Implementado por SHVs para indicar se há suporte para a configuração remota.</span><span class="sxs-lookup"><span data-stu-id="d0b7e-122">Implemented by SHVs to indicate whether remote configuration is supported.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="d0b7e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0b7e-123">Remarks</span></span>

<span data-ttu-id="d0b7e-124">Essa interface não deve ser implementada por agentes de integridade do sistema (SHAs) ou clientes de imposição de quarentena (QECs).</span><span class="sxs-lookup"><span data-stu-id="d0b7e-124">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b7e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0b7e-125">Requirements</span></span>



| <span data-ttu-id="d0b7e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0b7e-126">Requirement</span></span> | <span data-ttu-id="d0b7e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d0b7e-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b7e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0b7e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d0b7e-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d0b7e-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d0b7e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0b7e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d0b7e-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d0b7e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d0b7e-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0b7e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0b7e-133"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0b7e-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0b7e-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="d0b7e-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d0b7e-135"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d0b7e-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0b7e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0b7e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0b7e-137">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="d0b7e-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="d0b7e-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="d0b7e-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="d0b7e-139">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="d0b7e-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 






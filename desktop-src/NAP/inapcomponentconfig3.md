---
title: Interface INapComponentConfig3 (NapCommon. h)
description: Fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema) para definir e modificar dados de configuração para uma ID de configuração específica.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- INapComponentConfig3 da interface NAP
- INapComponentConfig3 interface NAP, descrita
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0cfead891da106a1a950ba83b9108b5950a738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782308"
---
# <a name="inapcomponentconfig3-interface"></a><span data-ttu-id="32c27-105">Interface INapComponentConfig3</span><span class="sxs-lookup"><span data-stu-id="32c27-105">INapComponentConfig3 interface</span></span>

> [!Note]  
> <span data-ttu-id="32c27-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="32c27-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="32c27-107">A interface **INapComponentConfig3** fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema) para definir e modificar dados de configuração para uma ID de configuração específica.</span><span class="sxs-lookup"><span data-stu-id="32c27-107">The **INapComponentConfig3** interface provides NAP system configuration methods for system health validators (SHVs) to set and modify configuration data for a specific configuration ID.</span></span>

> [!Note]  
> <span data-ttu-id="32c27-108">Essa interface herda todos os métodos de [**INapComponentConfig2**](inapcomponentconfig2.md) e deve ser usada em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="32c27-108">This interface inherits all the methods of [**INapComponentConfig2**](inapcomponentconfig2.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="32c27-109">Membros</span><span class="sxs-lookup"><span data-stu-id="32c27-109">Members</span></span>

<span data-ttu-id="32c27-110">A interface **INapComponentConfig3** herda de [**INapComponentConfig2**](inapcomponentconfig2.md).</span><span class="sxs-lookup"><span data-stu-id="32c27-110">The **INapComponentConfig3** interface inherits from [**INapComponentConfig2**](inapcomponentconfig2.md).</span></span> <span data-ttu-id="32c27-111">**INapComponentConfig3** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="32c27-111">**INapComponentConfig3** also has these types of members:</span></span>

-   [<span data-ttu-id="32c27-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="32c27-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="32c27-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="32c27-113">Methods</span></span>

<span data-ttu-id="32c27-114">A interface **INapComponentConfig3** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="32c27-114">The **INapComponentConfig3** interface has these methods.</span></span>



| <span data-ttu-id="32c27-115">Método</span><span class="sxs-lookup"><span data-stu-id="32c27-115">Method</span></span>                                                                                | <span data-ttu-id="32c27-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="32c27-116">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32c27-117">**INapComponentConfig3::D eleteAllConfig**</span><span class="sxs-lookup"><span data-stu-id="32c27-117">**INapComponentConfig3::DeleteAllConfig**</span></span>](inapcomponentconfig3-deleteallconfig.md) | <span data-ttu-id="32c27-118">Implementado por SHVs para fornecer uma maneira de redefinir o armazenamento SHV para seu estado original após a instalação.</span><span class="sxs-lookup"><span data-stu-id="32c27-118">Implemented by SHVs to provide a way to reset the SHV store to its original state after setup.</span></span><br/>      |
| [<span data-ttu-id="32c27-119">**INapComponentConfig3::D eleteConfig**</span><span class="sxs-lookup"><span data-stu-id="32c27-119">**INapComponentConfig3::DeleteConfig**</span></span>](inapcomponentconfig3-deleteconfig.md)       | <span data-ttu-id="32c27-120">Implementado por SHVs para fornecer uma maneira de excluir dados de configuração para uma ID de configuração específica.</span><span class="sxs-lookup"><span data-stu-id="32c27-120">Implemented by SHVs to provide a way to delete configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="32c27-121">**INapComponentConfig3::GetConfigFromID**</span><span class="sxs-lookup"><span data-stu-id="32c27-121">**INapComponentConfig3::GetConfigFromID**</span></span>](inapcomponentconfig3-getconfigfromid.md) | <span data-ttu-id="32c27-122">Implementado por SHVs para fornecer uma maneira de obter dados de configuração para uma ID de configuração específica.</span><span class="sxs-lookup"><span data-stu-id="32c27-122">Implemented by SHVs to provide a way to obtain configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="32c27-123">**INapComponentConfig3:: NewConfig**</span><span class="sxs-lookup"><span data-stu-id="32c27-123">**INapComponentConfig3::NewConfig**</span></span>](inapcomponentconfig3-newconfig.md)             | <span data-ttu-id="32c27-124">Implementado por SHVs para fornecer uma maneira de criar dados de configuração para uma ID de configuração específica.</span><span class="sxs-lookup"><span data-stu-id="32c27-124">Implemented by SHVs to provide a way to create configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="32c27-125">**INapComponentConfig3::SetConfigToID**</span><span class="sxs-lookup"><span data-stu-id="32c27-125">**INapComponentConfig3::SetConfigToID**</span></span>](inapcomponentconfig3-setconfigtoid.md)     | <span data-ttu-id="32c27-126">Implementado por SHVs para fornecer uma maneira de definir os dados de configuração para uma ID de configuração específica.</span><span class="sxs-lookup"><span data-stu-id="32c27-126">Implemented by SHVs to provide a way to set the configuration data for a specific configuration ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="32c27-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="32c27-127">Remarks</span></span>

<span data-ttu-id="32c27-128">Essa interface não deve ser implementada por agentes de integridade do sistema (SHAs) ou clientes de imposição de quarentena (QECs).</span><span class="sxs-lookup"><span data-stu-id="32c27-128">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="32c27-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32c27-129">Requirements</span></span>



| <span data-ttu-id="32c27-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="32c27-130">Requirement</span></span> | <span data-ttu-id="32c27-131">Valor</span><span class="sxs-lookup"><span data-stu-id="32c27-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32c27-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32c27-132">Minimum supported client</span></span><br/> | <span data-ttu-id="32c27-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="32c27-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="32c27-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32c27-134">Minimum supported server</span></span><br/> | <span data-ttu-id="32c27-135">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="32c27-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32c27-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32c27-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="32c27-137"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="32c27-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="32c27-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="32c27-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32c27-139"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="32c27-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32c27-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="32c27-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32c27-141">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="32c27-141">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> <dt>

[<span data-ttu-id="32c27-142">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="32c27-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="32c27-143">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="32c27-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 






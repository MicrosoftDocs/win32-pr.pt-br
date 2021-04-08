---
description: Representa o serviço de segurança. Ele é usado para definir as configurações de segurança do sistema virtual.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921858"
---
# <a name="msvm_securityservice-class"></a><span data-ttu-id="1c210-104">\_Classe Msvm SecurityService</span><span class="sxs-lookup"><span data-stu-id="1c210-104">Msvm\_SecurityService class</span></span>

<span data-ttu-id="1c210-105">Representa o serviço de segurança.</span><span class="sxs-lookup"><span data-stu-id="1c210-105">Represents the security service.</span></span> <span data-ttu-id="1c210-106">Ele é usado para definir as configurações de segurança do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="1c210-106">It is used for configuring virtual system security settings.</span></span>

<span data-ttu-id="1c210-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1c210-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c210-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c210-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="1c210-109">Membros</span><span class="sxs-lookup"><span data-stu-id="1c210-109">Members</span></span>

<span data-ttu-id="1c210-110">A classe **Msvm \_ SecurityService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1c210-110">The **Msvm\_SecurityService** class has these types of members:</span></span>

-   [<span data-ttu-id="1c210-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c210-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1c210-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c210-112">Methods</span></span>

<span data-ttu-id="1c210-113">A classe **Msvm \_ SecurityService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1c210-113">The **Msvm\_SecurityService** class has these methods.</span></span>



| <span data-ttu-id="1c210-114">Método</span><span class="sxs-lookup"><span data-stu-id="1c210-114">Method</span></span>                                                                                            | <span data-ttu-id="1c210-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c210-115">Description</span></span>                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="1c210-116">**GetKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="1c210-116">**GetKeyProtector**</span></span>](msvm-securityservice-getkeyprotector.md)                                   | <span data-ttu-id="1c210-117">Método para recuperar o protetor de chave para um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="1c210-117">Method to retrieve the key protector for a virtual system.</span></span><br/>   |
| [<span data-ttu-id="1c210-118">**ModifySecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="1c210-118">**ModifySecuritySettings**</span></span>](msvm-securityservice-modifysecuritysettings.md)                     | <span data-ttu-id="1c210-119">Modifica as configurações de segurança atuais de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c210-119">Modifies the current security settings of a virtual machine.</span></span><br/> |
| [<span data-ttu-id="1c210-120">**RestoreLastKnownGoodKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="1c210-120">**RestoreLastKnownGoodKeyProtector**</span></span>](msvm-securityservice-restorelastknowngoodkeyprotector.md) | <span data-ttu-id="1c210-121">Método para restaurar de volta para o último protetor de chave válido conhecido.</span><span class="sxs-lookup"><span data-stu-id="1c210-121">Method to restore back to the last known good key protector.</span></span><br/> |
| [<span data-ttu-id="1c210-122">**SetKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="1c210-122">**SetKeyProtector**</span></span>](msvm-securityservice-setkeyprotector.md)                                   | <span data-ttu-id="1c210-123">Método para definir o protetor de chave para um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="1c210-123">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="1c210-124">**Setsecuritypolicy**</span><span class="sxs-lookup"><span data-stu-id="1c210-124">**SetSecurityPolicy**</span></span>](msvm-securityservice-setsecuritypolicy.md)                               | <span data-ttu-id="1c210-125">Método para definir o protetor de chave para um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="1c210-125">Method to set the key protector for a virtual system.</span></span><br/>        |
| [<span data-ttu-id="1c210-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="1c210-126">**StartService**</span></span>](msvm-securityservice-startservice.md)                                         | <span data-ttu-id="1c210-127">Inicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="1c210-127">Starts the service.</span></span><br/>                                          |
| [<span data-ttu-id="1c210-128">**StopService**</span><span class="sxs-lookup"><span data-stu-id="1c210-128">**StopService**</span></span>](msvm-securityservice-stopservice.md)                                           | <span data-ttu-id="1c210-129">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="1c210-129">Stops the service.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="1c210-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c210-130">Requirements</span></span>



| <span data-ttu-id="1c210-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c210-131">Requirement</span></span> | <span data-ttu-id="1c210-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1c210-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c210-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c210-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1c210-134">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="1c210-134">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1c210-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c210-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1c210-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1c210-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1c210-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c210-137">Namespace</span></span><br/>                | <span data-ttu-id="1c210-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1c210-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1c210-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1c210-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c210-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c210-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c210-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1c210-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c210-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1c210-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1c210-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c210-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c210-144">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="1c210-144">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 





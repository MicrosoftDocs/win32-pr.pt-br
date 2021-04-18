---
description: Representa o registro de um serviço na plataforma Microsoft Hyper-V.
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Classe Msvm_VirtualizationComponentRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e9704dcade0474a10ca60383280941ec2e3591b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789798"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a><span data-ttu-id="1bf8f-103">\_Classe Msvm VirtualizationComponentRegistration</span><span class="sxs-lookup"><span data-stu-id="1bf8f-103">Msvm\_VirtualizationComponentRegistration class</span></span>

<span data-ttu-id="1bf8f-104">Representa o registro de um serviço na plataforma Microsoft Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="1bf8f-104">Represents the registration of a service in the Microsoft Hyper-V platform.</span></span>

<span data-ttu-id="1bf8f-105">A sintaxe a seguir é simplificada formato MOF código (MOF).</span><span class="sxs-lookup"><span data-stu-id="1bf8f-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf8f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bf8f-106">Syntax</span></span>

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a><span data-ttu-id="1bf8f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1bf8f-107">Members</span></span>

<span data-ttu-id="1bf8f-108">A classe **Msvm \_ VirtualizationComponentRegistration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1bf8f-108">The **Msvm\_VirtualizationComponentRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="1bf8f-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bf8f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bf8f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bf8f-110">Properties</span></span>

<span data-ttu-id="1bf8f-111">A classe **Msvm \_ VirtualizationComponentRegistration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1bf8f-111">The **Msvm\_VirtualizationComponentRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1bf8f-112">**Componente**</span><span class="sxs-lookup"><span data-stu-id="1bf8f-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf8f-113">Tipo de dados: **[ **Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="1bf8f-113">Data type: **[**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1bf8f-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bf8f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bf8f-115">Uma referência a uma instância que descreve o objeto COM que implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="1bf8f-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="1bf8f-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="1bf8f-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf8f-117">Tipo de dados: **[ **Msvm \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="1bf8f-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1bf8f-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bf8f-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bf8f-119">Uma referência a uma instância que descreve um tipo de recurso com suporte pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="1bf8f-119">A reference to an instance that describes a resource type supported by the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bf8f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bf8f-120">Remarks</span></span>

<span data-ttu-id="1bf8f-121">O acesso à classe **Msvm \_ VirtualizationComponentRegistration** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="1bf8f-121">Access to the **Msvm\_VirtualizationComponentRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1bf8f-122">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1bf8f-122">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf8f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bf8f-123">Requirements</span></span>



| <span data-ttu-id="1bf8f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bf8f-124">Requirement</span></span> | <span data-ttu-id="1bf8f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1bf8f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf8f-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bf8f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1bf8f-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1bf8f-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1bf8f-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bf8f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1bf8f-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1bf8f-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1bf8f-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1bf8f-130">End of client support</span></span><br/>    | <span data-ttu-id="1bf8f-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1bf8f-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1bf8f-132">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1bf8f-132">End of server support</span></span><br/>    | <span data-ttu-id="1bf8f-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1bf8f-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1bf8f-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="1bf8f-134">Namespace</span></span><br/>                | <span data-ttu-id="1bf8f-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1bf8f-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1bf8f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1bf8f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bf8f-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bf8f-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bf8f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1bf8f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bf8f-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1bf8f-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


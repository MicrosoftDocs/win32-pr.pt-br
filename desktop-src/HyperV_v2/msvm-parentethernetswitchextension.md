---
description: Representa a associação entre uma extensão de comutador Ethernet pai e uma extensão de comutador Ethernet filho.
ms.assetid: a0a60214-d85d-4c64-b720-1c34abc25287
title: Classe Msvm_ParentEthernetSwitchExtension
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentEthernetSwitchExtension
- Msvm_ParentEthernetSwitchExtension.Antecedent
- Msvm_ParentEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8e215a01c9de98baa545dbb32b8279db4555f9cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789801"
---
# <a name="msvm_parentethernetswitchextension-class"></a><span data-ttu-id="4baba-103">\_Classe Msvm ParentEthernetSwitchExtension</span><span class="sxs-lookup"><span data-stu-id="4baba-103">Msvm\_ParentEthernetSwitchExtension class</span></span>

<span data-ttu-id="4baba-104">Representa a associação entre uma extensão de comutador Ethernet pai e uma extensão de comutador Ethernet filho.</span><span class="sxs-lookup"><span data-stu-id="4baba-104">Represents the association between a parent Ethernet switch extension and a child Ethernet switch extension.</span></span>

<span data-ttu-id="4baba-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4baba-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4baba-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4baba-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentEthernetSwitchExtension : CIM_Dependency
{
  Msvm_EthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4baba-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4baba-107">Members</span></span>

<span data-ttu-id="4baba-108">A classe **Msvm \_ ParentEthernetSwitchExtension** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4baba-108">The **Msvm\_ParentEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="4baba-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4baba-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4baba-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4baba-110">Properties</span></span>

<span data-ttu-id="4baba-111">A classe **Msvm \_ ParentEthernetSwitchExtension** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4baba-111">The **Msvm\_ParentEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4baba-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="4baba-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4baba-113">Tipo de dados: **[ **Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="4baba-113">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4baba-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4baba-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4baba-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4baba-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4baba-116">Uma referência a uma instância da classe [**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representa a extensão de comutador pai.</span><span class="sxs-lookup"><span data-stu-id="4baba-116">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the parent switch extension.</span></span>

</dd> <dt>

<span data-ttu-id="4baba-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="4baba-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4baba-118">Tipo de dados: **[ **Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="4baba-118">Data type: **[**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4baba-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4baba-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4baba-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="4baba-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4baba-121">Uma referência a uma instância da classe [**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representa a extensão do comutador filho.</span><span class="sxs-lookup"><span data-stu-id="4baba-121">A reference to an instance of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represents the child switch extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4baba-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4baba-122">Requirements</span></span>



| <span data-ttu-id="4baba-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4baba-123">Requirement</span></span> | <span data-ttu-id="4baba-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4baba-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4baba-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4baba-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4baba-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4baba-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4baba-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4baba-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4baba-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4baba-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4baba-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="4baba-129">Namespace</span></span><br/>                | <span data-ttu-id="4baba-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4baba-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4baba-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4baba-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4baba-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4baba-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4baba-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4baba-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4baba-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4baba-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


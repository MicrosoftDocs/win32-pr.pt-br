---
description: Representa uma associação na qual uma entrada de um banco de dados de encaminhamento se aplica a uma porta de comutador.
ms.assetid: e63ac61d-ed0c-49e9-b056-4fcb6d1d5455
title: Classe CIM_SwitchPortDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPortDynamicForwarding
- CIM_SwitchPortDynamicForwarding.Antecedent
- CIM_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0e0d87e2ee5df6a7564d92fd1f8421dfa09abe20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750855"
---
# <a name="cim_switchportdynamicforwarding-class"></a><span data-ttu-id="6e8f0-103">\_Classe CIM SwitchPortDynamicForwarding</span><span class="sxs-lookup"><span data-stu-id="6e8f0-103">CIM\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="6e8f0-104">Representa uma associação na qual uma entrada de um banco de dados de encaminhamento se aplica a uma porta de comutador.</span><span class="sxs-lookup"><span data-stu-id="6e8f0-104">Represents an association in which an entry of a forwarding database applies to a switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e8f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e8f0-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_SwitchPortDynamicForwarding : CIM_Dependency
{
  CIM_SwitchPort             REF Antecedent;
  CIM_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6e8f0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6e8f0-106">Members</span></span>

<span data-ttu-id="6e8f0-107">A classe **CIM \_ SwitchPortDynamicForwarding** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6e8f0-107">The **CIM\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="6e8f0-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6e8f0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e8f0-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6e8f0-109">Properties</span></span>

<span data-ttu-id="6e8f0-110">A classe **CIM \_ SwitchPortDynamicForwarding** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6e8f0-110">The **CIM\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e8f0-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="6e8f0-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e8f0-112">Tipo de dados **: \_ switchport do CIM**</span><span class="sxs-lookup"><span data-stu-id="6e8f0-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="6e8f0-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e8f0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e8f0-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6e8f0-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6e8f0-115">Uma referência de [**\_ switchport do CIM**](cim-switchport.md) para a porta do comutador.</span><span class="sxs-lookup"><span data-stu-id="6e8f0-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="6e8f0-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="6e8f0-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e8f0-117">Tipo de dados: **CIM \_ DynamicForwardingEntry**</span><span class="sxs-lookup"><span data-stu-id="6e8f0-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="6e8f0-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6e8f0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e8f0-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="6e8f0-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6e8f0-120">Uma referência do [**CIM \_ DynamicForwardingEntry**](cim-dynamicforwardingentry.md) à entrada do banco de dados de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="6e8f0-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e8f0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e8f0-121">Requirements</span></span>



| <span data-ttu-id="6e8f0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e8f0-122">Requirement</span></span> | <span data-ttu-id="6e8f0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6e8f0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8f0-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e8f0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6e8f0-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e8f0-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6e8f0-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e8f0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6e8f0-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e8f0-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6e8f0-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e8f0-128">Namespace</span></span><br/>                | <span data-ttu-id="6e8f0-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6e8f0-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6e8f0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6e8f0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e8f0-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e8f0-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e8f0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6e8f0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e8f0-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e8f0-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6e8f0-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e8f0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e8f0-135">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="6e8f0-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


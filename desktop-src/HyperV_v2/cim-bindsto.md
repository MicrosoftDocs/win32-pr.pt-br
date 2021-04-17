---
description: Representa uma associação em que um \_ objeto CIM ServiceAccessPoint solicita serviços de protocolo de um \_ objeto CIM ProtocolEndpoint.
ms.assetid: d1ef774d-f0e0-43e7-8a9d-63c2fad5ca4a
title: Classe CIM_BindsTo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsTo
- CIM_BindsTo.Antecedent
- CIM_BindsTo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae32bd10d1e7d1944519fe8fb039453989c165fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769349"
---
# <a name="cim_bindsto-class"></a><span data-ttu-id="30839-103">\_Classe CIM BindsTo</span><span class="sxs-lookup"><span data-stu-id="30839-103">CIM\_BindsTo class</span></span>

<span data-ttu-id="30839-104">Representa uma associação em que um objeto [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) solicita serviços de protocolo de um objeto [**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md) .</span><span class="sxs-lookup"><span data-stu-id="30839-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) object requests protocol services from a [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="30839-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30839-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_BindsTo : CIM_SAPSAPDependency
{
  CIM_ProtocolEndpoint   REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="30839-106">Membros</span><span class="sxs-lookup"><span data-stu-id="30839-106">Members</span></span>

<span data-ttu-id="30839-107">A classe **CIM \_ BindsTo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="30839-107">The **CIM\_BindsTo** class has these types of members:</span></span>

-   [<span data-ttu-id="30839-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="30839-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30839-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="30839-109">Properties</span></span>

<span data-ttu-id="30839-110">A classe **CIM \_ BindsTo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="30839-110">The **CIM\_BindsTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30839-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="30839-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30839-112">Tipo de dados: **CIM \_ ProtocolEndpoint**</span><span class="sxs-lookup"><span data-stu-id="30839-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="30839-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30839-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30839-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="30839-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="30839-115">O ponto de extremidade de nível inferior que é acessado pelo Access Service.</span><span class="sxs-lookup"><span data-stu-id="30839-115">The lower level endpoint that is accessed by the service access point.</span></span>

</dd> <dt>

<span data-ttu-id="30839-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="30839-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30839-117">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="30839-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="30839-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="30839-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30839-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="30839-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="30839-120">O ponto de acesso ou a extremidade do protocolo que é dependente do ponto de extremidade de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="30839-120">The access point or protocol endpoint that is dependent on the lower level endpoint.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30839-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30839-121">Requirements</span></span>



| <span data-ttu-id="30839-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="30839-122">Requirement</span></span> | <span data-ttu-id="30839-123">Valor</span><span class="sxs-lookup"><span data-stu-id="30839-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30839-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30839-124">Minimum supported client</span></span><br/> | <span data-ttu-id="30839-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="30839-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="30839-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30839-126">Minimum supported server</span></span><br/> | <span data-ttu-id="30839-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30839-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="30839-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="30839-128">Namespace</span></span><br/>                | <span data-ttu-id="30839-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="30839-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="30839-130">MOF</span><span class="sxs-lookup"><span data-stu-id="30839-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30839-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30839-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="30839-132">DLL</span><span class="sxs-lookup"><span data-stu-id="30839-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30839-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="30839-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="30839-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="30839-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30839-135">**\_SAPSAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="30839-135">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 


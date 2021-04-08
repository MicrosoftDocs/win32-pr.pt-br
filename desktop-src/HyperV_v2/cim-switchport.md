---
description: Representa uma porta de comutador que envia e recebe quadros de dados.
ms.assetid: 015eed2a-1393-40ef-a190-832ab48766f9
title: Classe CIM_SwitchPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPort
- CIM_SwitchPort.PortNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf63843fc5a246012d3af6a059c897956d6f19b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921783"
---
# <a name="cim_switchport-class"></a><span data-ttu-id="bcf67-103">\_Classe switchport do CIM</span><span class="sxs-lookup"><span data-stu-id="bcf67-103">CIM\_SwitchPort class</span></span>

<span data-ttu-id="bcf67-104">Representa uma porta de comutador que envia e recebe quadros de dados.</span><span class="sxs-lookup"><span data-stu-id="bcf67-104">Represents a switch port that sends and receives data frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf67-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bcf67-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints")]
class CIM_SwitchPort : CIM_ProtocolEndpoint
{
  uint16 PortNumber;
};
```

## <a name="members"></a><span data-ttu-id="bcf67-106">Membros</span><span class="sxs-lookup"><span data-stu-id="bcf67-106">Members</span></span>

<span data-ttu-id="bcf67-107">A **classe \_ switchport do CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bcf67-107">The **CIM\_SwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="bcf67-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bcf67-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bcf67-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bcf67-109">Properties</span></span>

<span data-ttu-id="bcf67-110">A **classe \_ switchport do CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bcf67-110">The **CIM\_SwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bcf67-111">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="bcf67-111">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcf67-112">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bcf67-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bcf67-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bcf67-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcf67-114">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dPort ")</span><span class="sxs-lookup"><span data-stu-id="bcf67-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dPort")</span></span>
</dt> </dl>

<span data-ttu-id="bcf67-115">O identificador numérico da porta do comutador.</span><span class="sxs-lookup"><span data-stu-id="bcf67-115">The numeric identifier of the switch port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcf67-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcf67-116">Requirements</span></span>



| <span data-ttu-id="bcf67-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcf67-117">Requirement</span></span> | <span data-ttu-id="bcf67-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bcf67-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf67-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcf67-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf67-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bcf67-120">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="bcf67-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcf67-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf67-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bcf67-122">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="bcf67-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="bcf67-123">Namespace</span></span><br/>                | <span data-ttu-id="bcf67-124">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="bcf67-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bcf67-125">MOF</span><span class="sxs-lookup"><span data-stu-id="bcf67-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcf67-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcf67-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcf67-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bcf67-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcf67-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bcf67-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bcf67-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcf67-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf67-130">**CIM \_ ProtocolEndpoint**</span><span class="sxs-lookup"><span data-stu-id="bcf67-130">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 


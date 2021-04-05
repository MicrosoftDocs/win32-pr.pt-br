---
description: Representa o aspecto de ponte transparente de um \_ objeto CIM SwitchService.
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: Classe CIM_TransparentBridgingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed2c21c0f00bd89b0054667274a559ef25ce9326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827886"
---
# <a name="cim_transparentbridgingservice-class"></a><span data-ttu-id="1d3b6-103">\_Classe CIM TransparentBridgingService</span><span class="sxs-lookup"><span data-stu-id="1d3b6-103">CIM\_TransparentBridgingService class</span></span>

<span data-ttu-id="1d3b6-104">Representa o aspecto de ponte transparente de um objeto [**CIM \_ SwitchService**](cim-switchservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1d3b6-104">Represents the transparent bridging aspect of a [**CIM\_SwitchService**](cim-switchservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d3b6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d3b6-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a><span data-ttu-id="1d3b6-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1d3b6-106">Members</span></span>

<span data-ttu-id="1d3b6-107">A classe **CIM \_ TransparentBridgingService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1d3b6-107">The **CIM\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="1d3b6-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1d3b6-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d3b6-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1d3b6-109">Properties</span></span>

<span data-ttu-id="1d3b6-110">A classe **CIM \_ TransparentBridgingService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1d3b6-110">The **CIM\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d3b6-111">**Envelhecimento**</span><span class="sxs-lookup"><span data-stu-id="1d3b6-111">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3b6-112">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d3b6-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d3b6-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d3b6-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d3b6-114">Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpAgingTime ")</span><span class="sxs-lookup"><span data-stu-id="1d3b6-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpAgingTime")</span></span>
</dt> </dl>

<span data-ttu-id="1d3b6-115">O período de tempo limite, em segundos, para expiração de informações de encaminhamento de forma dinâmica.</span><span class="sxs-lookup"><span data-stu-id="1d3b6-115">The timeout period, in seconds, for aging out dynamically learned forwarding information.</span></span> <span data-ttu-id="1d3b6-116">O padrão 802.1 D-1990 recomenda um padrão de 300 segundos.</span><span class="sxs-lookup"><span data-stu-id="1d3b6-116">The 802.1D-1990 standard recommends a default of 300 seconds.</span></span>

</dd> <dt>

<span data-ttu-id="1d3b6-117">**FID**</span><span class="sxs-lookup"><span data-stu-id="1d3b6-117">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d3b6-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d3b6-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d3b6-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d3b6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d3b6-120">Identificador de banco de dados de filtragem usado por comutadores com reconhecimento de VLAN que têm mais de um banco de dados de filtragem.</span><span class="sxs-lookup"><span data-stu-id="1d3b6-120">Filtering Database Identifier used by VLAN-aware switches that have more than one filtering database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d3b6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d3b6-121">Requirements</span></span>



| <span data-ttu-id="1d3b6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d3b6-122">Requirement</span></span> | <span data-ttu-id="1d3b6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1d3b6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d3b6-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d3b6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1d3b6-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1d3b6-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1d3b6-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d3b6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1d3b6-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d3b6-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1d3b6-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d3b6-128">Namespace</span></span><br/>                | <span data-ttu-id="1d3b6-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1d3b6-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1d3b6-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1d3b6-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d3b6-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d3b6-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d3b6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1d3b6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d3b6-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d3b6-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1d3b6-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d3b6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d3b6-135">**\_FORWARDINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1d3b6-135">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 


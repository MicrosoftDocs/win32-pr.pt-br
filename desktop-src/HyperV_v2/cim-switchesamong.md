---
description: Representa um serviço de comutador, que alterna os quadros entre as portas do comutador.
ms.assetid: ee2d4831-df00-408c-b350-26d2d1d3e8aa
title: Classe CIM_SwitchesAmong
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchesAmong
- CIM_SwitchesAmong.Antecedent
- CIM_SwitchesAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16a87797b4a138ef79be3d5ea8c6304d2ce4a942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090641"
---
# <a name="cim_switchesamong-class"></a><span data-ttu-id="2c608-103">\_Classe CIM SwitchesAmong</span><span class="sxs-lookup"><span data-stu-id="2c608-103">CIM\_SwitchesAmong class</span></span>

<span data-ttu-id="2c608-104">Representa um serviço de comutador, que alterna os quadros entre as portas do comutador.</span><span class="sxs-lookup"><span data-stu-id="2c608-104">Represents a switch service, which switches frames between switch ports.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c608-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c608-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchesAmong : CIM_ForwardsAmong
{
  CIM_SwitchPort    REF Antecedent;
  CIM_SwitchService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2c608-106">Membros</span><span class="sxs-lookup"><span data-stu-id="2c608-106">Members</span></span>

<span data-ttu-id="2c608-107">A classe **CIM \_ SwitchesAmong** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2c608-107">The **CIM\_SwitchesAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="2c608-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2c608-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c608-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2c608-109">Properties</span></span>

<span data-ttu-id="2c608-110">A classe **CIM \_ SwitchesAmong** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2c608-110">The **CIM\_SwitchesAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c608-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="2c608-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c608-112">Tipo de dados **: \_ switchport do CIM**</span><span class="sxs-lookup"><span data-stu-id="2c608-112">Data type: **CIM\_SwitchPort**</span></span>
</dt> <dt>

<span data-ttu-id="2c608-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c608-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c608-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="2c608-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2c608-115">Uma referência de [**\_ switchport do CIM**](cim-switchport.md) para a porta do comutador.</span><span class="sxs-lookup"><span data-stu-id="2c608-115">A [**CIM\_SwitchPort**](cim-switchport.md) reference to the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="2c608-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="2c608-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c608-117">Tipo de dados: **CIM \_ SwitchService**</span><span class="sxs-lookup"><span data-stu-id="2c608-117">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="2c608-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c608-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c608-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="2c608-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="2c608-120">Uma referência do [**CIM \_ SwitchService**](cim-switchservice.md) ao serviço de comutação.</span><span class="sxs-lookup"><span data-stu-id="2c608-120">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c608-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c608-121">Requirements</span></span>



| <span data-ttu-id="2c608-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c608-122">Requirement</span></span> | <span data-ttu-id="2c608-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2c608-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c608-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c608-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2c608-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2c608-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2c608-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c608-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2c608-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2c608-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2c608-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c608-128">Namespace</span></span><br/>                | <span data-ttu-id="2c608-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2c608-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2c608-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2c608-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c608-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c608-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c608-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2c608-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c608-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c608-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2c608-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c608-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c608-135">**\_FORWARDSAMONG CIM**</span><span class="sxs-lookup"><span data-stu-id="2c608-135">**CIM\_ForwardsAmong**</span></span>](cim-forwardsamong.md)
</dt> </dl>

 


---
description: Associa um serviço de ponte transparente com uma entrada de seu banco de dados de encaminhamento.
ms.assetid: 6db93e71-c9b7-4710-a9ee-99a1055cfd82
title: Classe CIM_TransparentBridgingDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingDynamicForwarding
- CIM_TransparentBridgingDynamicForwarding.Antecedent
- CIM_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d089ca662880ad269cb9d9c63cb0935ff6de0b5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758985"
---
# <a name="cim_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="b2fe1-103">\_Classe CIM TransparentBridgingDynamicForwarding</span><span class="sxs-lookup"><span data-stu-id="b2fe1-103">CIM\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="b2fe1-104">Associa um serviço de ponte transparente com uma entrada de seu banco de dados de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="b2fe1-104">Associates a transparent bridging service with an entry of its forwarding database.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2fe1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2fe1-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingDynamicForwarding : CIM_Dependency
{
  CIM_TransparentBridgingService REF Antecedent;
  CIM_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b2fe1-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b2fe1-106">Members</span></span>

<span data-ttu-id="b2fe1-107">A classe **CIM \_ TransparentBridgingDynamicForwarding** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b2fe1-107">The **CIM\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="b2fe1-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b2fe1-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2fe1-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b2fe1-109">Properties</span></span>

<span data-ttu-id="b2fe1-110">A classe **CIM \_ TransparentBridgingDynamicForwarding** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b2fe1-110">The **CIM\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2fe1-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="b2fe1-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fe1-112">Tipo de dados: **CIM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="b2fe1-112">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="b2fe1-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b2fe1-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2fe1-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="b2fe1-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b2fe1-115">Uma referência do [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) ao serviço de ponte transparente.</span><span class="sxs-lookup"><span data-stu-id="b2fe1-115">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="b2fe1-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="b2fe1-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2fe1-117">Tipo de dados: **CIM \_ DynamicForwardingEntry**</span><span class="sxs-lookup"><span data-stu-id="b2fe1-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="b2fe1-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b2fe1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2fe1-119">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b2fe1-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b2fe1-120">Uma referência de [**\_ DynamicForwardingEntry CIM**](cim-dynamicforwardingentry.md) para a entrada de banco de dados de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="b2fe1-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the forwarding database entry.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2fe1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2fe1-121">Requirements</span></span>



| <span data-ttu-id="b2fe1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2fe1-122">Requirement</span></span> | <span data-ttu-id="b2fe1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b2fe1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2fe1-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2fe1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b2fe1-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b2fe1-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b2fe1-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2fe1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b2fe1-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b2fe1-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b2fe1-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2fe1-128">Namespace</span></span><br/>                | <span data-ttu-id="b2fe1-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b2fe1-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b2fe1-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b2fe1-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2fe1-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2fe1-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2fe1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b2fe1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2fe1-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2fe1-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2fe1-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2fe1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2fe1-135">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="b2fe1-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


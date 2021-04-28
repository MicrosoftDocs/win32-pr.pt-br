---
description: Classe Msvm_EthernetDeviceSAPImplementation – representa uma associação entre um ponto de acesso de serviço e o dispositivo lógico que o implementa.
ms.assetid: C0DDB199-AD97-4DD7-8056-BD6BD0CECFA8
title: Classe Msvm_EthernetDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetDeviceSAPImplementation
- Msvm_EthernetDeviceSAPImplementation.Antecedent
- Msvm_EthernetDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fddce9505ca2f8692044239d294904eb17c95ffa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111944"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a><span data-ttu-id="6040b-103">\_Classe Msvm EthernetDeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="6040b-103">Msvm\_EthernetDeviceSAPImplementation class</span></span>

<span data-ttu-id="6040b-104">Representa uma associação entre um ponto de acesso de serviço e o dispositivo lógico que o implementa.</span><span class="sxs-lookup"><span data-stu-id="6040b-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="6040b-105">A cardinalidade dessa associação é muitos-para-muitos.</span><span class="sxs-lookup"><span data-stu-id="6040b-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="6040b-106">Um SAP (ponto de acesso A serviços) pode ser fornecido por mais de um dispositivo lógico, operando em conjunto.</span><span class="sxs-lookup"><span data-stu-id="6040b-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="6040b-107">Qualquer dispositivo pode fornecer mais de um SAP.</span><span class="sxs-lookup"><span data-stu-id="6040b-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="6040b-108">Quando muitos dispositivos lógicos são associados a um único SAP, supõe-se que esses elementos operam em conjunto para fornecer o ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="6040b-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="6040b-109">Se diferentes implementações de um SAP existirem, cada uma dessas implementações resultaria em instanciações individuais do objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="6040b-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="6040b-110">Essas instanciações individuais teriam associações para as implementações exclusivas.</span><span class="sxs-lookup"><span data-stu-id="6040b-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="6040b-111">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6040b-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6040b-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6040b-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_EthernetPort REF Antecedent;
  Msvm_LANEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="6040b-113">Membros</span><span class="sxs-lookup"><span data-stu-id="6040b-113">Members</span></span>

<span data-ttu-id="6040b-114">A classe **Msvm \_ EthernetDeviceSAPImplementation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6040b-114">The **Msvm\_EthernetDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="6040b-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6040b-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6040b-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6040b-116">Properties</span></span>

<span data-ttu-id="6040b-117">A classe **Msvm \_ EthernetDeviceSAPImplementation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6040b-117">The **Msvm\_EthernetDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6040b-118">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="6040b-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6040b-119">Tipo de dados: **[ **CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span><span class="sxs-lookup"><span data-stu-id="6040b-119">Data type: **[**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span></span>
</dt> <dt>

<span data-ttu-id="6040b-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6040b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6040b-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="6040b-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6040b-122">Uma referência a uma classe derivada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) que representa o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6040b-122">A reference to a class derived from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="6040b-123">**Depende**</span><span class="sxs-lookup"><span data-stu-id="6040b-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6040b-124">Tipo de dados: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="6040b-124">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="6040b-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6040b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6040b-126">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="6040b-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6040b-127">Uma referência a uma instância da classe [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) que representa o SAP que está usando o **Antecedent**.</span><span class="sxs-lookup"><span data-stu-id="6040b-127">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6040b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6040b-128">Requirements</span></span>



| <span data-ttu-id="6040b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6040b-129">Requirement</span></span> | <span data-ttu-id="6040b-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6040b-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6040b-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6040b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6040b-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6040b-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6040b-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6040b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6040b-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6040b-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6040b-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="6040b-135">Namespace</span></span><br/>                | <span data-ttu-id="6040b-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6040b-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6040b-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6040b-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6040b-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6040b-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6040b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6040b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6040b-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6040b-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


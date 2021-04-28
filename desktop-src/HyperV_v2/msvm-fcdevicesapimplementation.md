---
description: Classe Msvm_FcDeviceSAPImplementation – representa uma associação entre um ponto de acesso de serviço e o dispositivo lógico que o implementa.
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Classe Msvm_FcDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcDeviceSAPImplementation
- Msvm_FcDeviceSAPImplementation.Antecedent
- Msvm_FcDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b0df7a198b3ee52d131800073f8be30d51d93181
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119024"
---
# <a name="msvm_fcdevicesapimplementation-class"></a><span data-ttu-id="a8d72-103">\_Classe Msvm FcDeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="a8d72-103">Msvm\_FcDeviceSAPImplementation class</span></span>

<span data-ttu-id="a8d72-104">Representa uma associação entre um ponto de acesso de serviço e o dispositivo lógico que o implementa.</span><span class="sxs-lookup"><span data-stu-id="a8d72-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="a8d72-105">A cardinalidade dessa associação é muitos-para-muitos.</span><span class="sxs-lookup"><span data-stu-id="a8d72-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="a8d72-106">Um SAP (ponto de acesso A serviços) pode ser fornecido por mais de um dispositivo lógico, operando em conjunto.</span><span class="sxs-lookup"><span data-stu-id="a8d72-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="a8d72-107">Qualquer dispositivo pode fornecer mais de um SAP.</span><span class="sxs-lookup"><span data-stu-id="a8d72-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="a8d72-108">Quando muitos dispositivos lógicos são associados a um único SAP, supõe-se que esses elementos operam em conjunto para fornecer o ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="a8d72-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="a8d72-109">Se diferentes implementações de um SAP existirem, cada uma dessas implementações resultaria em instanciações individuais do objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="a8d72-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="a8d72-110">Essas instanciações individuais teriam associações para as implementações exclusivas.</span><span class="sxs-lookup"><span data-stu-id="a8d72-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="a8d72-111">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a8d72-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d72-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8d72-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="a8d72-113">Membros</span><span class="sxs-lookup"><span data-stu-id="a8d72-113">Members</span></span>

<span data-ttu-id="a8d72-114">A classe **Msvm \_ FcDeviceSAPImplementation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a8d72-114">The **Msvm\_FcDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="a8d72-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a8d72-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8d72-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a8d72-116">Properties</span></span>

<span data-ttu-id="a8d72-117">A classe **Msvm \_ FcDeviceSAPImplementation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a8d72-117">The **Msvm\_FcDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8d72-118">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="a8d72-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8d72-119">Tipo de dados: **CIM \_ FCPort**</span><span class="sxs-lookup"><span data-stu-id="a8d72-119">Data type: **CIM\_FCPort**</span></span>
</dt> <dt>

<span data-ttu-id="a8d72-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8d72-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8d72-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="a8d72-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a8d72-122">Uma referência a uma classe derivada do **CIM \_ FCPort** que representa o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a8d72-122">A reference to a class derived from **CIM\_FCPort** that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="a8d72-123">**Depende**</span><span class="sxs-lookup"><span data-stu-id="a8d72-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8d72-124">Tipo de dados: **Msvm \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="a8d72-124">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="a8d72-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8d72-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8d72-126">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="a8d72-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a8d72-127">Uma referência a uma instância da classe [**Msvm \_ FcEndpoint**](msvm-fcendpoint.md) que representa o SAP que está usando o **Antecedent**.</span><span class="sxs-lookup"><span data-stu-id="a8d72-127">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8d72-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8d72-128">Requirements</span></span>



| <span data-ttu-id="a8d72-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8d72-129">Requirement</span></span> | <span data-ttu-id="a8d72-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a8d72-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d72-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8d72-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a8d72-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a8d72-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a8d72-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8d72-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a8d72-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a8d72-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a8d72-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8d72-135">Namespace</span></span><br/>                | <span data-ttu-id="a8d72-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a8d72-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a8d72-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a8d72-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8d72-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8d72-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8d72-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a8d72-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8d72-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a8d72-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


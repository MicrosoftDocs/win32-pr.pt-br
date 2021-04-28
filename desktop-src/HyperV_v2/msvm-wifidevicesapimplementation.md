---
description: Classe de Msvm_WiFiDeviceSAPImplementation – uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado.
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Classe Msvm_WiFiDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99826ce3a37e19867cef1a6ddf276f5136b21a3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109244"
---
# <a name="msvm_wifidevicesapimplementation-class"></a><span data-ttu-id="41eb8-103">\_Classe Msvm WiFiDeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="41eb8-103">Msvm\_WiFiDeviceSAPImplementation class</span></span>

<span data-ttu-id="41eb8-104">Uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado.</span><span class="sxs-lookup"><span data-stu-id="41eb8-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="41eb8-105">A cardinalidade dessa associação é muitos-para-muitos.</span><span class="sxs-lookup"><span data-stu-id="41eb8-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="41eb8-106">Um SAP pode ser fornecido por mais de um dispositivo lógico, operando em conjunto.</span><span class="sxs-lookup"><span data-stu-id="41eb8-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="41eb8-107">Qualquer dispositivo pode fornecer mais de um SAP.</span><span class="sxs-lookup"><span data-stu-id="41eb8-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="41eb8-108">Quando muitos dispositivos lógicos são associados a um único SAP, supõe-se que esses elementos operam em conjunto para fornecer o ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="41eb8-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="41eb8-109">Se diferentes implementações de um SAP existirem, cada uma dessas implementações resultaria em instanciações individuais do objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="41eb8-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="41eb8-110">Essas instanciações individuais teriam associações para as implementações exclusivas.</span><span class="sxs-lookup"><span data-stu-id="41eb8-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="41eb8-111">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="41eb8-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="41eb8-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41eb8-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="41eb8-113">Membros</span><span class="sxs-lookup"><span data-stu-id="41eb8-113">Members</span></span>

<span data-ttu-id="41eb8-114">A classe **Msvm \_ WiFiDeviceSAPImplementation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="41eb8-114">The **Msvm\_WiFiDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="41eb8-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41eb8-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41eb8-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41eb8-116">Properties</span></span>

<span data-ttu-id="41eb8-117">A classe **Msvm \_ WiFiDeviceSAPImplementation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="41eb8-117">The **Msvm\_WiFiDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41eb8-118">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="41eb8-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41eb8-119">Tipo de dados: **[ **Msvm \_ WiFiPort**](msvm-wifiport.md)**</span><span class="sxs-lookup"><span data-stu-id="41eb8-119">Data type: **[**Msvm\_WiFiPort**](msvm-wifiport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="41eb8-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41eb8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41eb8-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="41eb8-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="41eb8-122">Uma instância da classe [**Msvm \_ WiFiPort**](msvm-wifiport.md) que representa o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="41eb8-122">An instance of the [**Msvm\_WiFiPort**](msvm-wifiport.md) class that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="41eb8-123">**Depende**</span><span class="sxs-lookup"><span data-stu-id="41eb8-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41eb8-124">Tipo de dados: **[ **Msvm \_ WiFiEndpoint**](msvm-wifiendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="41eb8-124">Data type: **[**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="41eb8-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41eb8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41eb8-126">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="41eb8-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="41eb8-127">Uma instância da classe [**Msvm \_ WiFiEndpoint**](msvm-wifiendpoint.md) que representa o ponto de acesso de serviço implementado usando o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="41eb8-127">An instance of the [**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md) class that represents the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41eb8-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41eb8-128">Requirements</span></span>



| <span data-ttu-id="41eb8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="41eb8-129">Requirement</span></span> | <span data-ttu-id="41eb8-130">Valor</span><span class="sxs-lookup"><span data-stu-id="41eb8-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41eb8-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41eb8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="41eb8-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="41eb8-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="41eb8-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41eb8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="41eb8-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="41eb8-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41eb8-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="41eb8-135">Namespace</span></span><br/>                | <span data-ttu-id="41eb8-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="41eb8-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="41eb8-137">MOF</span><span class="sxs-lookup"><span data-stu-id="41eb8-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41eb8-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41eb8-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41eb8-139">DLL</span><span class="sxs-lookup"><span data-stu-id="41eb8-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41eb8-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41eb8-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


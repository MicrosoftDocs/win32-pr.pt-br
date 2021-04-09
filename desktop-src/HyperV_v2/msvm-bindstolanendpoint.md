---
description: Essa associação estabelece um serviço de ponto de acesso (SAP) como um solicitante de serviços de protocolo a partir de um ponto de extremidade de protocolo.
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Classe Msvm_BindsToLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BindsToLANEndpoint
- Msvm_BindsToLANEndpoint.Antecedent
- Msvm_BindsToLANEndpoint.Dependent
- Msvm_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2fa01c8e9e7df40a2907e6e43a9cb4b507a53d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922555"
---
# <a name="msvm_bindstolanendpoint-class"></a><span data-ttu-id="138dd-103">\_Classe Msvm BindsToLANEndpoint</span><span class="sxs-lookup"><span data-stu-id="138dd-103">Msvm\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="138dd-104">Essa associação estabelece um serviço de ponto de acesso (SAP) como um solicitante de serviços de protocolo a partir de um ponto de extremidade de protocolo.</span><span class="sxs-lookup"><span data-stu-id="138dd-104">This association establishes a service access point (SAP) as a requester of protocol services from a protocol endpoint.</span></span> <span data-ttu-id="138dd-105">Normalmente, essa associação é executada entre SAPs e pontos de extremidade em um único sistema.</span><span class="sxs-lookup"><span data-stu-id="138dd-105">Typically, this association runs between SAPs and endpoints on a single system.</span></span> <span data-ttu-id="138dd-106">Como um ponto de extremidade de protocolo é um tipo de SAP, essa associação pode ser usada para estabelecer uma camada de dois protocolos, com a camada superior representada pelo **dependente** e a camada inferior representada pelo **Antecedent**.</span><span class="sxs-lookup"><span data-stu-id="138dd-106">Because a protocol endpoint is a kind of SAP, this binding can be used to establish a layering of two protocols, with the upper layer represented by the **Dependent** and the lower layer represented by the **Antecedent**.</span></span>

<span data-ttu-id="138dd-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="138dd-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="138dd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="138dd-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BindsToLANEndpoint : CIM_BindsToLANEndpoint
{
  Msvm_LANEndpoint  REF Antecedent;
  Msvm_VLANEndpoint REF Dependent;
  uint16                FrameType;
};
```

## <a name="members"></a><span data-ttu-id="138dd-109">Membros</span><span class="sxs-lookup"><span data-stu-id="138dd-109">Members</span></span>

<span data-ttu-id="138dd-110">A classe **Msvm \_ BindsToLANEndpoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="138dd-110">The **Msvm\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="138dd-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="138dd-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="138dd-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="138dd-112">Properties</span></span>

<span data-ttu-id="138dd-113">A classe **Msvm \_ BindsToLANEndpoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="138dd-113">The **Msvm\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="138dd-114">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="138dd-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="138dd-115">Tipo de dados: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="138dd-115">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="138dd-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="138dd-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="138dd-117">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="138dd-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="138dd-118">Uma referência a uma classe [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) que representa a porta do comutador.</span><span class="sxs-lookup"><span data-stu-id="138dd-118">A reference to an [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the switch port.</span></span> <span data-ttu-id="138dd-119">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="138dd-119">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="138dd-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="138dd-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="138dd-121">Tipo de dados: **[ **Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="138dd-121">Data type: **[**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="138dd-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="138dd-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="138dd-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="138dd-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="138dd-124">Uma referência ao [**Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md) associado à porta do comutador.</span><span class="sxs-lookup"><span data-stu-id="138dd-124">A reference to the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) associated with the switch port.</span></span> <span data-ttu-id="138dd-125">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="138dd-125">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="138dd-126">**Conjunto de quadros**</span><span class="sxs-lookup"><span data-stu-id="138dd-126">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="138dd-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="138dd-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="138dd-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="138dd-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="138dd-129">Descreve o método de enquadramento para a camada superior SAP ou o ponto de extremidade associado ao ponto de extremidade da LAN.</span><span class="sxs-lookup"><span data-stu-id="138dd-129">Describes the framing method for the upper layer SAP or endpoint that is bound to the LAN endpoint.</span></span> <span data-ttu-id="138dd-130">Essa propriedade é herdada do **CIM \_ BindsToLANEndpoint** e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="138dd-130">This property is inherited from **CIM\_BindsToLANEndpoint**, and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="138dd-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="138dd-131">Requirements</span></span>



| <span data-ttu-id="138dd-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="138dd-132">Requirement</span></span> | <span data-ttu-id="138dd-133">Valor</span><span class="sxs-lookup"><span data-stu-id="138dd-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="138dd-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="138dd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="138dd-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="138dd-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="138dd-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="138dd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="138dd-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="138dd-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="138dd-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="138dd-138">Namespace</span></span><br/>                | <span data-ttu-id="138dd-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="138dd-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="138dd-140">MOF</span><span class="sxs-lookup"><span data-stu-id="138dd-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="138dd-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="138dd-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="138dd-142">DLL</span><span class="sxs-lookup"><span data-stu-id="138dd-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="138dd-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="138dd-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


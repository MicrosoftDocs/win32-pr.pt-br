---
description: Descreve um conjunto de classes com propriedades e métodos necessários, necessários para gerenciar uma entidade do mundo real ou para dar suporte a um cenário de uso de maneira interoperável.
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Classe Msvm_RegisteredProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a7014687355524fbe10ff01869cac6c3fd35a894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011087"
---
# <a name="msvm_registeredprofile-class"></a><span data-ttu-id="ac447-103">\_Classe Msvm RegisteredProfile</span><span class="sxs-lookup"><span data-stu-id="ac447-103">Msvm\_RegisteredProfile class</span></span>

<span data-ttu-id="ac447-104">Descreve um conjunto de classes com propriedades e métodos necessários, necessários para gerenciar uma entidade do mundo real ou para dar suporte a um cenário de uso de maneira interoperável.</span><span class="sxs-lookup"><span data-stu-id="ac447-104">Describes a set of classes with required properties and methods, necessary to manage a real-world entity or to support a usage scenario, in an interoperable fashion.</span></span>

<span data-ttu-id="ac447-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ac447-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac447-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac447-106">Syntax</span></span>

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="ac447-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ac447-107">Members</span></span>

<span data-ttu-id="ac447-108">A classe **Msvm \_ RegisteredProfile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ac447-108">The **Msvm\_RegisteredProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="ac447-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ac447-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac447-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ac447-110">Properties</span></span>

<span data-ttu-id="ac447-111">A classe **Msvm \_ RegisteredProfile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ac447-111">The **Msvm\_RegisteredProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac447-112">**AdvertiseTypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ac447-112">**AdvertiseTypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac447-113">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac447-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ac447-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac447-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac447-115">Uma matriz de cadeias de caracteres que fornece informações adicionais relacionadas à propriedade **advertisetype** .</span><span class="sxs-lookup"><span data-stu-id="ac447-115">An array of strings that provides additional information related to the **AdvertiseType** property.</span></span> <span data-ttu-id="ac447-116">Uma descrição deve ser fornecida quando **advertisetype** for 1 (Other).</span><span class="sxs-lookup"><span data-stu-id="ac447-116">A description must be provided when the **AdvertiseType** is 1 (Other).</span></span> <span data-ttu-id="ac447-117">Uma entrada nessa matriz corresponde ao mesmo índice na matriz **AdvertiseTypes** .</span><span class="sxs-lookup"><span data-stu-id="ac447-117">An entry in this array corresponds to the same index in the **AdvertiseTypes** array.</span></span> <span data-ttu-id="ac447-118">Essa propriedade é herdada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac447-118">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ac447-119">**AdvertiseTypes**</span><span class="sxs-lookup"><span data-stu-id="ac447-119">**AdvertiseTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac447-120">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac447-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac447-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac447-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac447-122">Especifica o anúncio das informações de perfil.</span><span class="sxs-lookup"><span data-stu-id="ac447-122">Specifies the advertisement for the profile information.</span></span> <span data-ttu-id="ac447-123">Ele é usado pelos serviços de anúncio da infraestrutura do WBEM para determinar o que deve ser anunciado, por meio de quais mecanismos.</span><span class="sxs-lookup"><span data-stu-id="ac447-123">It is used by the advertising services of the WBEM infrastructure to determine what should be advertised, through what mechanisms.</span></span> <span data-ttu-id="ac447-124">A propriedade é uma matriz para que o perfil possa ser anunciado usando vários mecanismos.</span><span class="sxs-lookup"><span data-stu-id="ac447-124">The property is an array so that the profile can be advertised using several mechanisms.</span></span> <span data-ttu-id="ac447-125">Se essa propriedade for **nula**, isso será equivalente a especificar o valor 2 (não anunciado).</span><span class="sxs-lookup"><span data-stu-id="ac447-125">If this property is **Null**, this is equivalent to specifying the value 2 (Not Advertised).</span></span> <span data-ttu-id="ac447-126">Essa propriedade é herdada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac447-126">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="ac447-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="ac447-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Não anunciado** (2)</span><span class="sxs-lookup"><span data-stu-id="ac447-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Not Advertised** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3)</span><span class="sxs-lookup"><span data-stu-id="ac447-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac447-130">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ac447-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac447-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac447-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac447-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac447-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac447-133">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="ac447-133">A short description of the object.</span></span> <span data-ttu-id="ac447-134">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ac447-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac447-135">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ac447-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac447-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac447-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac447-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac447-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac447-138">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="ac447-138">A description of the object.</span></span> <span data-ttu-id="ac447-139">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ac447-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac447-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ac447-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac447-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac447-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac447-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac447-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac447-143">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="ac447-143">A display name for the object.</span></span> <span data-ttu-id="ac447-144">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ac447-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac447-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac447-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac447-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac447-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac447-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac447-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac447-148">Qualificadores: **chave**, **substituição**</span><span class="sxs-lookup"><span data-stu-id="ac447-148">Qualifiers: **Key**, **Override**</span></span>
</dt> </dl>

<span data-ttu-id="ac447-149">Uma cadeia de caracteres que identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="ac447-149">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ac447-150">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ac447-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ac447-151">**OtherRegisteredOrganization**</span><span class="sxs-lookup"><span data-stu-id="ac447-151">**OtherRegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac447-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac447-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac447-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac447-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac447-154">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="ac447-154">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="ac447-155">Uma cadeia de caracteres que fornece uma descrição da organização quando **RegisteredOrganization** contém 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="ac447-155">A string that provides a description of the organization when **RegisteredOrganization** contains 1 (Other).</span></span> <span data-ttu-id="ac447-156">Essa propriedade é herdada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac447-156">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ac447-157">**Registeredname**</span><span class="sxs-lookup"><span data-stu-id="ac447-157">**RegisteredName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac447-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac447-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac447-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac447-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac447-160">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="ac447-160">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="ac447-161">O nome deste perfil registrado.</span><span class="sxs-lookup"><span data-stu-id="ac447-161">The name of this registered profile.</span></span> <span data-ttu-id="ac447-162">Como várias versões podem existir para o mesmo **registeredname**, a combinação de **registeredname**, **RegisteredOrganization** e **RegisteredVersion** deve identificar exclusivamente o perfil registrado no escopo da organização.</span><span class="sxs-lookup"><span data-stu-id="ac447-162">Since multiple versions can exist for the same **RegisteredName**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="ac447-163">Essa propriedade é herdada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac447-163">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ac447-164">**RegisteredOrganization**</span><span class="sxs-lookup"><span data-stu-id="ac447-164">**RegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac447-165">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac447-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac447-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac447-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac447-167">A organização que define esse perfil.</span><span class="sxs-lookup"><span data-stu-id="ac447-167">The organization that defines this profile.</span></span> <span data-ttu-id="ac447-168">Essa propriedade é herdada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac447-168">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="ac447-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="ac447-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span><span class="sxs-lookup"><span data-stu-id="ac447-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)</span><span class="sxs-lookup"><span data-stu-id="ac447-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consórcio para inovação de serviço** (4)</span><span class="sxs-lookup"><span data-stu-id="ac447-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consortium for Service Innovation** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-173"><span id="FAST"></span><span id="fast"></span>**Rápido** (5)</span><span class="sxs-lookup"><span data-stu-id="ac447-173"><span id="FAST"></span><span id="fast"></span>**FAST** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-174"><span id="GGF"></span><span id="ggf"></span>**GGF** (6)</span><span class="sxs-lookup"><span data-stu-id="ac447-174"><span id="GGF"></span><span id="ggf"></span>**GGF** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-175"><span id="INTAP"></span><span id="intap"></span>**INTAP** (7)</span><span class="sxs-lookup"><span data-stu-id="ac447-175"><span id="INTAP"></span><span id="intap"></span>**INTAP** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)</span><span class="sxs-lookup"><span data-stu-id="ac447-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span><span class="sxs-lookup"><span data-stu-id="ac447-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**10-aliança de eficiência de energia do noroeste** (10)</span><span class="sxs-lookup"><span data-stu-id="ac447-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**//10 Northwest Energy Efficiency Alliance** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-179"><span id="SNIA"></span><span id="snia"></span>**SNIA** (11)</span><span class="sxs-lookup"><span data-stu-id="ac447-179"><span id="SNIA"></span><span id="snia"></span>**SNIA** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**Fórum TM** (12)</span><span class="sxs-lookup"><span data-stu-id="ac447-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**TM Forum** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**O grupo aberto** (13)</span><span class="sxs-lookup"><span data-stu-id="ac447-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**The Open Group** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span><span class="sxs-lookup"><span data-stu-id="ac447-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span><span class="sxs-lookup"><span data-stu-id="ac447-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span><span class="sxs-lookup"><span data-stu-id="ac447-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-185"><span id="INCITS"></span><span id="incits"></span>**INCITS** (17)</span><span class="sxs-lookup"><span data-stu-id="ac447-185"><span id="INCITS"></span><span id="incits"></span>**INCITS** (17)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span><span class="sxs-lookup"><span data-stu-id="ac447-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span><span class="sxs-lookup"><span data-stu-id="ac447-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**20 OGF** (20)</span><span class="sxs-lookup"><span data-stu-id="ac447-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**//20 OGF** (20)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**A grade verde** (21)</span><span class="sxs-lookup"><span data-stu-id="ac447-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**The Green Grid** (21)</span></span>
</dt> <dt>

<span data-ttu-id="ac447-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="ac447-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="ac447-191">)</span><span class="sxs-lookup"><span data-stu-id="ac447-191">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac447-192">**RegisteredVersion**</span><span class="sxs-lookup"><span data-stu-id="ac447-192">**RegisteredVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac447-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ac447-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac447-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ac447-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac447-195">A versão deste perfil.</span><span class="sxs-lookup"><span data-stu-id="ac447-195">The version of this profile.</span></span> <span data-ttu-id="ac447-196">A cadeia de caracteres deve estar no formato: "*M*. *N*. *U*"onde:</span><span class="sxs-lookup"><span data-stu-id="ac447-196">The string must be in the form: "*M*.*N*.*U*" Where:</span></span>

-   <span data-ttu-id="ac447-197">*M* é a versão principal (em formato numérico) que descreve a criação ou a última modificação do perfil.</span><span class="sxs-lookup"><span data-stu-id="ac447-197">*M* is the major version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="ac447-198">*N* é a versão secundária (em formato numérico) que descreve a criação ou a última modificação do perfil.</span><span class="sxs-lookup"><span data-stu-id="ac447-198">*N* is the minor version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="ac447-199">*U* é a atualização (em formato numérico) que descreve a criação ou a última modificação do perfil.</span><span class="sxs-lookup"><span data-stu-id="ac447-199">*U* is the update (in numeric form) describing the profile's creation or last modification.</span></span>

<span data-ttu-id="ac447-200">Essa propriedade é herdada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ac447-200">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac447-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac447-201">Requirements</span></span>



| <span data-ttu-id="ac447-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac447-202">Requirement</span></span> | <span data-ttu-id="ac447-203">Valor</span><span class="sxs-lookup"><span data-stu-id="ac447-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac447-204">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac447-204">Minimum supported client</span></span><br/> | <span data-ttu-id="ac447-205">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ac447-205">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ac447-206">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac447-206">Minimum supported server</span></span><br/> | <span data-ttu-id="ac447-207">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="ac447-207">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ac447-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac447-208">Namespace</span></span><br/>                | <span data-ttu-id="ac447-209">\\Interoperabilidade raiz</span><span class="sxs-lookup"><span data-stu-id="ac447-209">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="ac447-210">MOF</span><span class="sxs-lookup"><span data-stu-id="ac447-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac447-211"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac447-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac447-212">DLL</span><span class="sxs-lookup"><span data-stu-id="ac447-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac447-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac447-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


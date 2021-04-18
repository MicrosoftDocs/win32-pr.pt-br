---
description: Define o meio pelo qual um cliente pode descobrir o intervalo válido de configurações padrão para um recurso de comutador Ethernet.
ms.assetid: 84ae7656-2cc4-4ca7-b4ae-95d9905c9aad
title: Classe Msvm_EthernetSwitchFeatureCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureCapabilities
- Msvm_EthernetSwitchFeatureCapabilities.InstanceID
- Msvm_EthernetSwitchFeatureCapabilities.Caption
- Msvm_EthernetSwitchFeatureCapabilities.Description
- Msvm_EthernetSwitchFeatureCapabilities.ElementName
- Msvm_EthernetSwitchFeatureCapabilities.FeatureId
- Msvm_EthernetSwitchFeatureCapabilities.Applicability
- Msvm_EthernetSwitchFeatureCapabilities.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ba145ca6a43a2031a676e565f38210dc6771f40e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764688"
---
# <a name="msvm_ethernetswitchfeaturecapabilities-class"></a><span data-ttu-id="1bd93-103">\_Classe Msvm EthernetSwitchFeatureCapabilities</span><span class="sxs-lookup"><span data-stu-id="1bd93-103">Msvm\_EthernetSwitchFeatureCapabilities class</span></span>

<span data-ttu-id="1bd93-104">Define o meio pelo qual um cliente pode descobrir o intervalo válido de configurações padrão para um recurso de comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="1bd93-104">Defines the means by which a client can discover the valid range of default settings for an Ethernet switch feature.</span></span> <span data-ttu-id="1bd93-105">Um objeto **Msvm \_ EthernetSwitchFeatureCapabilities** está associado a cada Comutador Ethernet virtual, para cada recurso compatível com a opção.</span><span class="sxs-lookup"><span data-stu-id="1bd93-105">An **Msvm\_EthernetSwitchFeatureCapabilities** object is associated with each virtual Ethernet switch, for each feature that the switch supports.</span></span> <span data-ttu-id="1bd93-106">Quatro objetos [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) são associados ao objeto **Msvm \_ EthernetSwitchFeatureCapabilities** para descrever os valores mínimo, máximo, padrão e incremental para os recursos de recurso do comutador fornecido.</span><span class="sxs-lookup"><span data-stu-id="1bd93-106">Four [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) objects are associated with the **Msvm\_EthernetSwitchFeatureCapabilities** object to describe the minimum, maximum, default, and incremental values for the given switch's feature capabilities.</span></span>

<span data-ttu-id="1bd93-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1bd93-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bd93-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bd93-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = " Ethernet Switch Feature Capabilities";
  string Description = "Microsoft Virtual Ethernet Switch Feature Capabilities";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  string FeatureId;
  uint16 Applicability;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="1bd93-109">Membros</span><span class="sxs-lookup"><span data-stu-id="1bd93-109">Members</span></span>

<span data-ttu-id="1bd93-110">A classe **Msvm \_ EthernetSwitchFeatureCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1bd93-110">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="1bd93-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bd93-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bd93-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1bd93-112">Properties</span></span>

<span data-ttu-id="1bd93-113">A classe **Msvm \_ EthernetSwitchFeatureCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1bd93-113">The **Msvm\_EthernetSwitchFeatureCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1bd93-114">**Aplicabilidade**</span><span class="sxs-lookup"><span data-stu-id="1bd93-114">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bd93-115">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1bd93-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1bd93-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bd93-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bd93-117">Descreve se esse recurso é aplicado a um comutador Ethernet ou a uma porta de comutador Ethernet específica.</span><span class="sxs-lookup"><span data-stu-id="1bd93-117">Describes whether this feature is applied to an Ethernet switch or a particular Ethernet switch port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1bd93-118">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1bd93-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Port"></span><span id="port"></span><span id="PORT"></span>

<span data-ttu-id="1bd93-119">**Porta** (1)</span><span class="sxs-lookup"><span data-stu-id="1bd93-119">**Port** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="1bd93-120">**Opção** (2)</span><span class="sxs-lookup"><span data-stu-id="1bd93-120">**Switch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1bd93-121">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1bd93-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bd93-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1bd93-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bd93-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bd93-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bd93-124">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="1bd93-124">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="1bd93-125">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1bd93-125">A short description of the object.</span></span> <span data-ttu-id="1bd93-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1bd93-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bd93-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1bd93-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bd93-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1bd93-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bd93-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bd93-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bd93-130">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="1bd93-130">A description of the object.</span></span> <span data-ttu-id="1bd93-131">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1bd93-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bd93-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1bd93-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bd93-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1bd93-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bd93-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bd93-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bd93-135">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1bd93-135">A display name for the object.</span></span> <span data-ttu-id="1bd93-136">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1bd93-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bd93-137">**Recurso de funcionalidade**</span><span class="sxs-lookup"><span data-stu-id="1bd93-137">**FeatureId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bd93-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1bd93-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bd93-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bd93-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bd93-140">O identificador do recurso ao qual este objeto fornece informações sobre recursos.</span><span class="sxs-lookup"><span data-stu-id="1bd93-140">The identifier of the feature this object provides capabilities information for.</span></span>

</dd> <dt>

<span data-ttu-id="1bd93-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1bd93-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bd93-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1bd93-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bd93-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bd93-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bd93-144">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="1bd93-144">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1bd93-145">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="1bd93-145">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1bd93-146">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1bd93-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1bd93-147">**Versão**</span><span class="sxs-lookup"><span data-stu-id="1bd93-147">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bd93-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1bd93-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bd93-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1bd93-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bd93-150">A versão do recurso em um formato de "Major. Minor", por exemplo, "2,0".</span><span class="sxs-lookup"><span data-stu-id="1bd93-150">The version of the feature in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1bd93-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bd93-151">Requirements</span></span>



| <span data-ttu-id="1bd93-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bd93-152">Requirement</span></span> | <span data-ttu-id="1bd93-153">Valor</span><span class="sxs-lookup"><span data-stu-id="1bd93-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bd93-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bd93-154">Minimum supported client</span></span><br/> | <span data-ttu-id="1bd93-155">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1bd93-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1bd93-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bd93-156">Minimum supported server</span></span><br/> | <span data-ttu-id="1bd93-157">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1bd93-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1bd93-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="1bd93-158">Namespace</span></span><br/>                | <span data-ttu-id="1bd93-159">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1bd93-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1bd93-160">MOF</span><span class="sxs-lookup"><span data-stu-id="1bd93-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bd93-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bd93-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bd93-162">DLL</span><span class="sxs-lookup"><span data-stu-id="1bd93-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bd93-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1bd93-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


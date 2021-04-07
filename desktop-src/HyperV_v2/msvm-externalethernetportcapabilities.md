---
description: Descreve os recursos do ExternalEthernetPort Msvm associado \_ .
ms.assetid: 63731b62-b1c7-4dd9-b906-03225bbc3154
title: Classe Msvm_ExternalEthernetPortCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPortCapabilities
- Msvm_ExternalEthernetPortCapabilities.InstanceID
- Msvm_ExternalEthernetPortCapabilities.Caption
- Msvm_ExternalEthernetPortCapabilities.Description
- Msvm_ExternalEthernetPortCapabilities.ElementName
- Msvm_ExternalEthernetPortCapabilities.IOVSupport
- Msvm_ExternalEthernetPortCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 748b207151fb1d11b013af7c736de52bbe5bec8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827302"
---
# <a name="msvm_externalethernetportcapabilities-class"></a><span data-ttu-id="eb936-103">\_Classe Msvm ExternalEthernetPortCapabilities</span><span class="sxs-lookup"><span data-stu-id="eb936-103">Msvm\_ExternalEthernetPortCapabilities class</span></span>

<span data-ttu-id="eb936-104">Descreve os recursos do [**\_ ExternalEthernetPort Msvm**](msvm-externalethernetport.md)associado.</span><span class="sxs-lookup"><span data-stu-id="eb936-104">Describes the capabilities of the associated [**Msvm\_ExternalEthernetPort**](msvm-externalethernetport.md).</span></span>

<span data-ttu-id="eb936-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="eb936-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb936-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb936-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPortCapabilities : CIM_Capabilities
{
  string  InstanceID;
  string  Caption = "Ethernet Port Capabilities";
  string  Description = "Describes the capabilities of the Microsoft External Ethernet Port";
  string  ElementName = "Ethernet Port Capabilities";
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="eb936-107">Membros</span><span class="sxs-lookup"><span data-stu-id="eb936-107">Members</span></span>

<span data-ttu-id="eb936-108">A classe **Msvm \_ ExternalEthernetPortCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="eb936-108">The **Msvm\_ExternalEthernetPortCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="eb936-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eb936-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb936-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eb936-110">Properties</span></span>

<span data-ttu-id="eb936-111">A classe **Msvm \_ ExternalEthernetPortCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="eb936-111">The **Msvm\_ExternalEthernetPortCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb936-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="eb936-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb936-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eb936-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb936-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb936-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb936-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="eb936-115">A short description of the object.</span></span> <span data-ttu-id="eb936-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "capacidades de porta Ethernet".</span><span class="sxs-lookup"><span data-stu-id="eb936-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="eb936-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="eb936-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb936-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eb936-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb936-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb936-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb936-120">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="eb936-120">A description of the object.</span></span> <span data-ttu-id="eb936-121">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "descreve os recursos da porta Ethernet externa da Microsoft".</span><span class="sxs-lookup"><span data-stu-id="eb936-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the capabilities of the Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="eb936-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="eb936-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb936-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eb936-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb936-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb936-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb936-125">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="eb936-125">A display name for the object.</span></span> <span data-ttu-id="eb936-126">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "capacidades de porta Ethernet".</span><span class="sxs-lookup"><span data-stu-id="eb936-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="eb936-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eb936-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb936-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eb936-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb936-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb936-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb936-130">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="eb936-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="eb936-131">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="eb936-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="eb936-132">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="eb936-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="eb936-133">**IOVSupport**</span><span class="sxs-lookup"><span data-stu-id="eb936-133">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb936-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="eb936-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb936-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb936-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb936-136">Um valor booliano que indica se o adaptador de rede oferece suporte a virtualização de e/s (IOV).</span><span class="sxs-lookup"><span data-stu-id="eb936-136">A boolean value that indicates whether I/O virtualization (IOV) is supported by the network adapter.</span></span> <span data-ttu-id="eb936-137">Se o valor for **true**, a IOV será suportada pelo adaptador de rede e a propriedade **IOVSupportReasons** estará vazia.</span><span class="sxs-lookup"><span data-stu-id="eb936-137">If the value is **True**, then IOV is supported by the network adapter and the **IOVSupportReasons** property will be empty.</span></span> <span data-ttu-id="eb936-138">Caso contrário, a propriedade **IOVSupportReasons** terá os motivos pelos quais a IOV não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="eb936-138">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="eb936-139">**IOVSupportReasons**</span><span class="sxs-lookup"><span data-stu-id="eb936-139">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb936-140">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eb936-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eb936-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb936-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb936-142">Uma matriz de cadeias de caracteres que indica as possíveis razões pelas quais a IOV não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="eb936-142">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="eb936-143">Se o valor de **IOVSupport** for **true**, essa matriz estará vazia.</span><span class="sxs-lookup"><span data-stu-id="eb936-143">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb936-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb936-144">Requirements</span></span>



| <span data-ttu-id="eb936-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb936-145">Requirement</span></span> | <span data-ttu-id="eb936-146">Valor</span><span class="sxs-lookup"><span data-stu-id="eb936-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb936-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb936-147">Minimum supported client</span></span><br/> | <span data-ttu-id="eb936-148">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="eb936-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="eb936-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb936-149">Minimum supported server</span></span><br/> | <span data-ttu-id="eb936-150">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="eb936-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb936-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb936-151">Namespace</span></span><br/>                | <span data-ttu-id="eb936-152">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="eb936-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eb936-153">MOF</span><span class="sxs-lookup"><span data-stu-id="eb936-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb936-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb936-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb936-155">DLL</span><span class="sxs-lookup"><span data-stu-id="eb936-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb936-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eb936-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


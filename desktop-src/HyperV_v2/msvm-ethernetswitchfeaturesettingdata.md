---
description: Uma classe abstrata que representa as configurações de uma determinada instância de um recurso de comutador Ethernet.
ms.assetid: c1720649-585f-45a9-8329-06787bd8b600
title: Classe Msvm_EthernetSwitchFeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureSettingData
- Msvm_EthernetSwitchFeatureSettingData.InstanceID
- Msvm_EthernetSwitchFeatureSettingData.Caption
- Msvm_EthernetSwitchFeatureSettingData.Description
- Msvm_EthernetSwitchFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a71d9b4a78ffedb6ffc0a0c1e01562ce7638ef65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757812"
---
# <a name="msvm_ethernetswitchfeaturesettingdata-class"></a><span data-ttu-id="17d96-103">\_Classe Msvm EthernetSwitchFeatureSettingData</span><span class="sxs-lookup"><span data-stu-id="17d96-103">Msvm\_EthernetSwitchFeatureSettingData class</span></span>

<span data-ttu-id="17d96-104">Uma classe abstrata que representa as configurações de uma determinada instância de um recurso de comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="17d96-104">An abstract class that represents settings for a given instance of an Ethernet switch feature.</span></span> <span data-ttu-id="17d96-105">A classe de gerenciamento de recursos do comutador Ethernet deve derivar dessa classe abstrata.</span><span class="sxs-lookup"><span data-stu-id="17d96-105">Ethernet Switch Features settings management class must derive from this abstract class.</span></span>

<span data-ttu-id="17d96-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="17d96-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d96-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17d96-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="17d96-108">Membros</span><span class="sxs-lookup"><span data-stu-id="17d96-108">Members</span></span>

<span data-ttu-id="17d96-109">A classe **Msvm \_ EthernetSwitchFeatureSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="17d96-109">The **Msvm\_EthernetSwitchFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="17d96-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="17d96-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17d96-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="17d96-111">Properties</span></span>

<span data-ttu-id="17d96-112">A classe **Msvm \_ EthernetSwitchFeatureSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="17d96-112">The **Msvm\_EthernetSwitchFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17d96-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="17d96-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17d96-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="17d96-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17d96-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="17d96-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17d96-116">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="17d96-116">A short description of the object.</span></span> <span data-ttu-id="17d96-117">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="17d96-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="17d96-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="17d96-118">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17d96-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="17d96-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17d96-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="17d96-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17d96-121">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="17d96-121">A description of the object.</span></span> <span data-ttu-id="17d96-122">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="17d96-122">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="17d96-123">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="17d96-123">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17d96-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="17d96-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17d96-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="17d96-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17d96-126">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="17d96-126">A display name for the object.</span></span> <span data-ttu-id="17d96-127">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17d96-127">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="17d96-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="17d96-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17d96-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="17d96-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17d96-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="17d96-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17d96-131">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="17d96-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="17d96-132">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="17d96-132">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="17d96-133">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17d96-133">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17d96-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17d96-134">Requirements</span></span>



| <span data-ttu-id="17d96-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="17d96-135">Requirement</span></span> | <span data-ttu-id="17d96-136">Valor</span><span class="sxs-lookup"><span data-stu-id="17d96-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17d96-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17d96-137">Minimum supported client</span></span><br/> | <span data-ttu-id="17d96-138">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="17d96-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="17d96-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17d96-139">Minimum supported server</span></span><br/> | <span data-ttu-id="17d96-140">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="17d96-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17d96-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="17d96-141">Namespace</span></span><br/>                | <span data-ttu-id="17d96-142">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="17d96-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="17d96-143">MOF</span><span class="sxs-lookup"><span data-stu-id="17d96-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17d96-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17d96-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="17d96-145">DLL</span><span class="sxs-lookup"><span data-stu-id="17d96-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17d96-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="17d96-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


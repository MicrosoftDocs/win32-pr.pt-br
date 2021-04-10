---
description: Classe base abstrata para classes que representam configurações para um recurso de porta de comutador Ethernet.
ms.assetid: 26c40dd0-fe1e-4432-a177-8a565bf678e6
title: Classe Msvm_EthernetSwitchPortFeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortFeatureSettingData
- Msvm_EthernetSwitchPortFeatureSettingData.InstanceID
- Msvm_EthernetSwitchPortFeatureSettingData.Caption
- Msvm_EthernetSwitchPortFeatureSettingData.Description
- Msvm_EthernetSwitchPortFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0734fa89d99d80e26e4d5fc841bdac89cfd8dfe6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296861"
---
# <a name="msvm_ethernetswitchportfeaturesettingdata-class"></a><span data-ttu-id="80c4f-103">\_Classe Msvm EthernetSwitchPortFeatureSettingData</span><span class="sxs-lookup"><span data-stu-id="80c4f-103">Msvm\_EthernetSwitchPortFeatureSettingData class</span></span>

<span data-ttu-id="80c4f-104">Classe base abstrata para classes que representam configurações para um recurso de porta de comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="80c4f-104">Abstract base class for classes that represent settings for an Ethernet switch port feature.</span></span>

<span data-ttu-id="80c4f-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="80c4f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c4f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80c4f-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPortFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="80c4f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="80c4f-107">Members</span></span>

<span data-ttu-id="80c4f-108">A classe **Msvm \_ EthernetSwitchPortFeatureSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="80c4f-108">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="80c4f-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="80c4f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80c4f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="80c4f-110">Properties</span></span>

<span data-ttu-id="80c4f-111">A classe **Msvm \_ EthernetSwitchPortFeatureSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="80c4f-111">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80c4f-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="80c4f-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c4f-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="80c4f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80c4f-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="80c4f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80c4f-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="80c4f-115">A short description of the object.</span></span> <span data-ttu-id="80c4f-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="80c4f-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="80c4f-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80c4f-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c4f-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="80c4f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80c4f-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="80c4f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80c4f-120">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="80c4f-120">A description of the object.</span></span> <span data-ttu-id="80c4f-121">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="80c4f-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="80c4f-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="80c4f-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c4f-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="80c4f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80c4f-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="80c4f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80c4f-125">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="80c4f-125">A display name for the object.</span></span> <span data-ttu-id="80c4f-126">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="80c4f-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="80c4f-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="80c4f-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c4f-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="80c4f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80c4f-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="80c4f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80c4f-130">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="80c4f-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="80c4f-131">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="80c4f-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="80c4f-132">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="80c4f-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80c4f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80c4f-133">Requirements</span></span>



| <span data-ttu-id="80c4f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="80c4f-134">Requirement</span></span> | <span data-ttu-id="80c4f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="80c4f-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80c4f-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80c4f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="80c4f-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="80c4f-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="80c4f-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80c4f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="80c4f-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="80c4f-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80c4f-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="80c4f-140">Namespace</span></span><br/>                | <span data-ttu-id="80c4f-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="80c4f-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="80c4f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="80c4f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80c4f-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80c4f-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80c4f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="80c4f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80c4f-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80c4f-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


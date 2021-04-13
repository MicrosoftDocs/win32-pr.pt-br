---
description: Uma classe abstrata que representa as configurações de um recurso específico de um sistema ou componente.
ms.assetid: f55eacdd-a802-4374-8756-a59733af6d2c
title: Classe Msvm_FeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingData
- Msvm_FeatureSettingData.InstanceID
- Msvm_FeatureSettingData.Caption
- Msvm_FeatureSettingData.Description
- Msvm_FeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98f022515ac877c0dd598cb9a962bc3133f76eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501383"
---
# <a name="msvm_featuresettingdata-class"></a><span data-ttu-id="effe7-103">\_Classe Msvm FeatureSettingData</span><span class="sxs-lookup"><span data-stu-id="effe7-103">Msvm\_FeatureSettingData class</span></span>

<span data-ttu-id="effe7-104">Uma classe abstrata que representa as configurações de um recurso específico de um sistema ou componente.</span><span class="sxs-lookup"><span data-stu-id="effe7-104">An abstract class that represents settings for a specific feature of a system or component.</span></span>

<span data-ttu-id="effe7-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="effe7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="effe7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="effe7-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="effe7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="effe7-107">Members</span></span>

<span data-ttu-id="effe7-108">A classe **Msvm \_ FeatureSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="effe7-108">The **Msvm\_FeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="effe7-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="effe7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="effe7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="effe7-110">Properties</span></span>

<span data-ttu-id="effe7-111">A classe **Msvm \_ FeatureSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="effe7-111">The **Msvm\_FeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="effe7-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="effe7-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="effe7-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="effe7-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="effe7-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="effe7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="effe7-115">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="effe7-115">A short description of the object.</span></span> <span data-ttu-id="effe7-116">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="effe7-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="effe7-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="effe7-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="effe7-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="effe7-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="effe7-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="effe7-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="effe7-120">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="effe7-120">A description of the object.</span></span> <span data-ttu-id="effe7-121">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="effe7-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="effe7-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="effe7-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="effe7-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="effe7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="effe7-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="effe7-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="effe7-125">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="effe7-125">A display name for the object.</span></span> <span data-ttu-id="effe7-126">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="effe7-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="effe7-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="effe7-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="effe7-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="effe7-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="effe7-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="effe7-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="effe7-130">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="effe7-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="effe7-131">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="effe7-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="effe7-132">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="effe7-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="effe7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="effe7-133">Requirements</span></span>



| <span data-ttu-id="effe7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="effe7-134">Requirement</span></span> | <span data-ttu-id="effe7-135">Valor</span><span class="sxs-lookup"><span data-stu-id="effe7-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="effe7-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="effe7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="effe7-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="effe7-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="effe7-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="effe7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="effe7-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="effe7-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="effe7-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="effe7-140">Namespace</span></span><br/>                | <span data-ttu-id="effe7-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="effe7-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="effe7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="effe7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="effe7-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="effe7-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="effe7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="effe7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="effe7-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="effe7-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


---
description: Representa as configurações do serviço 3D sintético presente em um único sistema de host.
ms.assetid: ed5d9bba-faad-40a6-8f08-258a94272a11
title: Classe Msvm_Synthetic3DServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DServiceSettingData
- Msvm_Synthetic3DServiceSettingData.InstanceID
- Msvm_Synthetic3DServiceSettingData.Caption
- Msvm_Synthetic3DServiceSettingData.Description
- Msvm_Synthetic3DServiceSettingData.ElementName
- Msvm_Synthetic3DServiceSettingData.GPUOvercommitEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b625064f90ef4c0241dfa48bea9900110f37a4d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091333"
---
# <a name="msvm_synthetic3dservicesettingdata-class"></a><span data-ttu-id="6c0c7-103">\_Classe Msvm Synthetic3DServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="6c0c7-103">Msvm\_Synthetic3DServiceSettingData class</span></span>

<span data-ttu-id="6c0c7-104">Representa as configurações do serviço 3D sintético presente em um único sistema de host.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-104">Represents the settings for the synthetic 3-D service present on a single host system.</span></span> <span data-ttu-id="6c0c7-105">As propriedades desta classe não podem ser modificadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="6c0c7-106">O cliente deve chamar o método [**Msvm \_ Synthetic3DService. ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) para modificar qualquer uma dessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-106">The client must call the [**Msvm\_Synthetic3DService.ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="6c0c7-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c0c7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c0c7-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Synthetic3D Service Settings";
  string  Description = "Configuration Settings for Synthetic3D Service.";
  string  ElementName = "Synthetic3D Service Settings";
  boolean GPUOvercommitEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="6c0c7-109">Membros</span><span class="sxs-lookup"><span data-stu-id="6c0c7-109">Members</span></span>

<span data-ttu-id="6c0c7-110">A classe **Msvm \_ Synthetic3DServiceSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6c0c7-110">The **Msvm\_Synthetic3DServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="6c0c7-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6c0c7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c0c7-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6c0c7-112">Properties</span></span>

<span data-ttu-id="6c0c7-113">A classe **Msvm \_ Synthetic3DServiceSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-113">The **Msvm\_Synthetic3DServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c0c7-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c0c7-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c0c7-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c0c7-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c0c7-117">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-117">A short description of the object.</span></span> <span data-ttu-id="6c0c7-118">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6c0c7-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6c0c7-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c0c7-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c0c7-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c0c7-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c0c7-122">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="6c0c7-122">A description of the object.</span></span> <span data-ttu-id="6c0c7-123">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6c0c7-123">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6c0c7-124">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-124">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c0c7-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c0c7-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c0c7-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c0c7-127">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-127">A display name for the object.</span></span> <span data-ttu-id="6c0c7-128">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6c0c7-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6c0c7-129">**GPUOvercommitEnabled**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-129">**GPUOvercommitEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c0c7-130">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c0c7-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c0c7-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c0c7-132">Controla se a atribuição de máquina virtual leva em conta limitações de memória de GPU.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-132">Controls whether virtual machine assignment takes GPU memory limitations into account.</span></span>

</dd> <dt>

<span data-ttu-id="6c0c7-133">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-133">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c0c7-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c0c7-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c0c7-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c0c7-136">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="6c0c7-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6c0c7-137">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="6c0c7-137">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6c0c7-138">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6c0c7-138">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c0c7-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c0c7-139">Requirements</span></span>



| <span data-ttu-id="6c0c7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c0c7-140">Requirement</span></span> | <span data-ttu-id="6c0c7-141">Valor</span><span class="sxs-lookup"><span data-stu-id="6c0c7-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c0c7-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c0c7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6c0c7-143">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6c0c7-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6c0c7-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c0c7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6c0c7-145">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6c0c7-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6c0c7-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c0c7-146">Namespace</span></span><br/>                | <span data-ttu-id="6c0c7-147">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6c0c7-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6c0c7-148">MOF</span><span class="sxs-lookup"><span data-stu-id="6c0c7-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c0c7-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c0c7-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c0c7-150">DLL</span><span class="sxs-lookup"><span data-stu-id="6c0c7-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c0c7-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6c0c7-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


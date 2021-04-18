---
description: Contém informações sobre uma GPU (unidade de processamento gráfico físico) do RemoteFX.
ms.assetid: 86B47AAE-DBFF-43EF-88C6-44836D6C3AFA
title: Classe Msvm_PhysicalGPUInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PhysicalGPUInfo
- Msvm_PhysicalGPUInfo.InstanceID
- Msvm_PhysicalGPUInfo.Caption
- Msvm_PhysicalGPUInfo.Description
- Msvm_PhysicalGPUInfo.ElementName
- Msvm_PhysicalGPUInfo.Name
- Msvm_PhysicalGPUInfo.ID
- Msvm_PhysicalGPUInfo.TotalVideoMemory
- Msvm_PhysicalGPUInfo.AvailableVideoMemory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cd4ccf65b364620e84063ea6398c59dd0e467f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756757"
---
# <a name="msvm_physicalgpuinfo-class"></a><span data-ttu-id="b24ee-103">\_Classe Msvm PhysicalGPUInfo</span><span class="sxs-lookup"><span data-stu-id="b24ee-103">Msvm\_PhysicalGPUInfo class</span></span>

<span data-ttu-id="b24ee-104">Contém informações sobre uma GPU (unidade de processamento gráfico físico) do RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="b24ee-104">Contains information about a RemoteFX physical graphics processing unit (GPU).</span></span>

<span data-ttu-id="b24ee-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b24ee-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b24ee-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b24ee-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PhysicalGPUInfo : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  string ID;
  uint64 TotalVideoMemory;
  uint64 AvailableVideoMemory;
};
```

## <a name="members"></a><span data-ttu-id="b24ee-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b24ee-107">Members</span></span>

<span data-ttu-id="b24ee-108">A classe **Msvm \_ PhysicalGPUInfo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b24ee-108">The **Msvm\_PhysicalGPUInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="b24ee-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b24ee-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b24ee-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b24ee-110">Properties</span></span>

<span data-ttu-id="b24ee-111">A classe **Msvm \_ PhysicalGPUInfo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b24ee-111">The **Msvm\_PhysicalGPUInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b24ee-112">**AvailableVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="b24ee-112">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b24ee-113">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b24ee-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b24ee-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b24ee-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b24ee-115">A quantidade de memória de vídeo não usada, em bytes, na GPU física que pode ser usada pelo RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="b24ee-115">The amount of unused video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="b24ee-116">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b24ee-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b24ee-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b24ee-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b24ee-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b24ee-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b24ee-119">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="b24ee-119">A short description of the object.</span></span> <span data-ttu-id="b24ee-120">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b24ee-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b24ee-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b24ee-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b24ee-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b24ee-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b24ee-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b24ee-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b24ee-124">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="b24ee-124">A description of the object.</span></span> <span data-ttu-id="b24ee-125">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b24ee-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b24ee-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b24ee-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b24ee-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b24ee-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b24ee-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b24ee-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b24ee-129">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="b24ee-129">A display name for the object.</span></span> <span data-ttu-id="b24ee-130">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b24ee-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b24ee-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="b24ee-131">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b24ee-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b24ee-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b24ee-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b24ee-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b24ee-134">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="b24ee-134">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="b24ee-135">O identificador exclusivo da GPU física.</span><span class="sxs-lookup"><span data-stu-id="b24ee-135">The unique identifier of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="b24ee-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b24ee-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b24ee-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b24ee-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b24ee-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b24ee-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b24ee-139">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="b24ee-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b24ee-140">Uma cadeia de caracteres que identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="b24ee-140">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b24ee-141">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b24ee-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b24ee-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b24ee-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b24ee-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b24ee-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b24ee-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b24ee-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b24ee-145">Qualificadores: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="b24ee-145">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="b24ee-146">O nome de exibição da GPU física.</span><span class="sxs-lookup"><span data-stu-id="b24ee-146">The display name of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="b24ee-147">**TotalVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="b24ee-147">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b24ee-148">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b24ee-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b24ee-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b24ee-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b24ee-150">A quantidade total de memória de vídeo, em bytes, na GPU física que pode ser usada pelo RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="b24ee-150">The total amount of video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b24ee-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b24ee-151">Requirements</span></span>



| <span data-ttu-id="b24ee-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="b24ee-152">Requirement</span></span> | <span data-ttu-id="b24ee-153">Valor</span><span class="sxs-lookup"><span data-stu-id="b24ee-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b24ee-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b24ee-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b24ee-155">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b24ee-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b24ee-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b24ee-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b24ee-157">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b24ee-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b24ee-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="b24ee-158">Namespace</span></span><br/>                | <span data-ttu-id="b24ee-159">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b24ee-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b24ee-160">MOF</span><span class="sxs-lookup"><span data-stu-id="b24ee-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b24ee-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b24ee-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b24ee-162">DLL</span><span class="sxs-lookup"><span data-stu-id="b24ee-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b24ee-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b24ee-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b24ee-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="b24ee-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b24ee-165">**\_Managedelement do CIM**</span><span class="sxs-lookup"><span data-stu-id="b24ee-165">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 


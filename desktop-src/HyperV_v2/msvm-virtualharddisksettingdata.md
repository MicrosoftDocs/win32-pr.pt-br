---
description: Fornece dados de configuração para um disco rígido virtual.
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Classe Msvm_VirtualHardDiskSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e13efbb068d15ca4051995e7d9f317eb2ccacab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090001"
---
# <a name="msvm_virtualharddisksettingdata-class"></a><span data-ttu-id="ceca9-103">\_Classe Msvm VirtualHardDiskSettingData</span><span class="sxs-lookup"><span data-stu-id="ceca9-103">Msvm\_VirtualHardDiskSettingData class</span></span>

<span data-ttu-id="ceca9-104">Fornece dados de configuração para um disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="ceca9-104">Provides setting data for a virtual hard disk.</span></span>

<span data-ttu-id="ceca9-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ceca9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceca9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ceca9-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a><span data-ttu-id="ceca9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ceca9-107">Members</span></span>

<span data-ttu-id="ceca9-108">A classe **Msvm \_ VirtualHardDiskSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ceca9-108">The **Msvm\_VirtualHardDiskSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ceca9-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ceca9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ceca9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ceca9-110">Properties</span></span>

<span data-ttu-id="ceca9-111">A classe **Msvm \_ VirtualHardDiskSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ceca9-111">The **Msvm\_VirtualHardDiskSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ceca9-112">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="ceca9-112">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceca9-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ceca9-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-115">O tamanho do bloco usado pelo disco rígido virtual, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ceca9-115">The block size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ceca9-116">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ceca9-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ceca9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ceca9-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-119">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="ceca9-119">A short description of the object.</span></span> <span data-ttu-id="ceca9-120">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "dados de configuração de disco rígido virtual".</span><span class="sxs-lookup"><span data-stu-id="ceca9-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Hard Disk Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="ceca9-121">**Alinhamento de data-**</span><span class="sxs-lookup"><span data-stu-id="ceca9-121">**DataAlignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-122">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceca9-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ceca9-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-124">Especifica o alinhamento desejado, em bytes, para a carga de dados do disco virtual</span><span class="sxs-lookup"><span data-stu-id="ceca9-124">Specifies the desired alignment, in bytes, for the data payload of the virtual disk</span></span>

> [!Note]  
> <span data-ttu-id="ceca9-125">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="ceca9-125">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="ceca9-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ceca9-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ceca9-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ceca9-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-129">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="ceca9-129">A description of the object.</span></span> <span data-ttu-id="ceca9-130">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "definindo dados para um disco rígido virtual".</span><span class="sxs-lookup"><span data-stu-id="ceca9-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Setting Data for a Virtual Hard Disk".</span></span>

</dd> <dt>

<span data-ttu-id="ceca9-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ceca9-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ceca9-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ceca9-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-134">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="ceca9-134">A display name for the object.</span></span> <span data-ttu-id="ceca9-135">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ceca9-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ceca9-136">**Formato**</span><span class="sxs-lookup"><span data-stu-id="ceca9-136">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-137">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ceca9-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ceca9-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-139">O formato do disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="ceca9-139">The format for the virtual hard disk.</span></span> <span data-ttu-id="ceca9-140">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ceca9-140">This will be one of the following values.</span></span>

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span data-ttu-id="ceca9-141"><span id="VHD"></span><span id="vhd"></span>**VHD** (2)</span><span class="sxs-lookup"><span data-stu-id="ceca9-141"><span id="VHD"></span><span id="vhd"></span>**VHD** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span data-ttu-id="ceca9-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)</span><span class="sxs-lookup"><span data-stu-id="ceca9-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span data-ttu-id="ceca9-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)</span><span class="sxs-lookup"><span data-stu-id="ceca9-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="ceca9-144">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ceca9-144">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ceca9-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ceca9-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ceca9-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ceca9-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-148">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="ceca9-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-149">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="ceca9-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ceca9-150">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ceca9-150">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ceca9-151">**IsPmemCompatible**</span><span class="sxs-lookup"><span data-stu-id="ceca9-151">**IsPmemCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-152">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ceca9-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ceca9-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-154">Especifica se o disco virtual pode ser usado como o armazenamento de backup para um dispositivo de memória persistente.</span><span class="sxs-lookup"><span data-stu-id="ceca9-154">Specifies whether the virtual disk can be used as the backing store for a persistent memory device.</span></span>

> [!Note]  
> <span data-ttu-id="ceca9-155">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="ceca9-155">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="ceca9-156">**LogicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="ceca9-156">**LogicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceca9-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ceca9-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-159">O tamanho do setor lógico usado pelo disco rígido virtual, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ceca9-159">The logical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ceca9-160">**MaxInternalSize**</span><span class="sxs-lookup"><span data-stu-id="ceca9-160">**MaxInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-161">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ceca9-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-162">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ceca9-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-163">O tamanho máximo do disco rígido virtual como visível pela máquina virtual, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ceca9-163">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="ceca9-164">Esse tamanho será arredondado para o próximo maior múltiplo do tamanho do setor.</span><span class="sxs-lookup"><span data-stu-id="ceca9-164">This size will be rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="ceca9-165">**ParentIdentifier**</span><span class="sxs-lookup"><span data-stu-id="ceca9-165">**ParentIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ceca9-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ceca9-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-168">O GUID usado para identificar exclusivamente o pai do disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="ceca9-168">The GUID used to uniquely identify the parent of the virtual hard disk.</span></span> <span data-ttu-id="ceca9-169">Se o disco rígido virtual não tiver um pai, esse campo estará vazio.</span><span class="sxs-lookup"><span data-stu-id="ceca9-169">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="ceca9-170">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ceca9-170">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="ceca9-171">**ParentPath**</span><span class="sxs-lookup"><span data-stu-id="ceca9-171">**ParentPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ceca9-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ceca9-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-174">O pai do disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="ceca9-174">The parent of the virtual hard disk.</span></span> <span data-ttu-id="ceca9-175">Se o disco rígido virtual não tiver um pai, essa propriedade estará vazia.</span><span class="sxs-lookup"><span data-stu-id="ceca9-175">If the virtual hard disk does not have a parent, then this property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="ceca9-176">**ParentTimestamp**</span><span class="sxs-lookup"><span data-stu-id="ceca9-176">**ParentTimestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-177">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ceca9-177">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ceca9-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-179">O carimbo de data/hora do pai do disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="ceca9-179">The timestamp of the parent of the virtual hard disk.</span></span> <span data-ttu-id="ceca9-180">Se o disco rígido virtual não tiver um pai, esse campo estará vazio.</span><span class="sxs-lookup"><span data-stu-id="ceca9-180">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="ceca9-181">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ceca9-181">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="ceca9-182">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="ceca9-182">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ceca9-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ceca9-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-185">O caminho totalmente qualificado do disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="ceca9-185">The fully qualified path of the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="ceca9-186">**PhysicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="ceca9-186">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-187">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ceca9-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-188">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ceca9-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-189">O tamanho do setor físico usado pelo disco rígido virtual, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ceca9-189">The physical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ceca9-190">**PmemAddressAbstractionType**</span><span class="sxs-lookup"><span data-stu-id="ceca9-190">**PmemAddressAbstractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-191">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ceca9-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-192">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ceca9-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-193">O método de abstração de endereço de memória persistente a ser usado com este disco virtual.</span><span class="sxs-lookup"><span data-stu-id="ceca9-193">The persistent memory address abstraction method to be used with this virtual disk.</span></span>

> [!Note]  
> <span data-ttu-id="ceca9-194">Adicionado no Windows 10, versão 1709.</span><span class="sxs-lookup"><span data-stu-id="ceca9-194">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="ceca9-195">**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="ceca9-195">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

<span data-ttu-id="ceca9-196">**BTT** (1)</span><span class="sxs-lookup"><span data-stu-id="ceca9-196">**BTT** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ceca9-197">**Desconhecido** (65535)</span><span class="sxs-lookup"><span data-stu-id="ceca9-197">**Unknown** (65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ceca9-198">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ceca9-198">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-199">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ceca9-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-200">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ceca9-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-201">O tipo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="ceca9-201">The type of virtual hard disk.</span></span> <span data-ttu-id="ceca9-202">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ceca9-202">This will be one of the following values.</span></span>

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="ceca9-203">**Fixo** (2)</span><span class="sxs-lookup"><span data-stu-id="ceca9-203">**Fixed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

<span data-ttu-id="ceca9-204">**Dinâmico** (3)</span><span class="sxs-lookup"><span data-stu-id="ceca9-204">**Dynamic** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

<span data-ttu-id="ceca9-205">**Diferenciação** (4)</span><span class="sxs-lookup"><span data-stu-id="ceca9-205">**Differencing** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ceca9-206">**VirtualDiskId**</span><span class="sxs-lookup"><span data-stu-id="ceca9-206">**VirtualDiskId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ceca9-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ceca9-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ceca9-208">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ceca9-208">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ceca9-209">O GUID que é usado para identificar exclusivamente o disco virtual.</span><span class="sxs-lookup"><span data-stu-id="ceca9-209">The GUID that is used to uniquely identify the virtual disk.</span></span>

<span data-ttu-id="ceca9-210">Quando o método [**Msvm \_ imagens. GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) retorna uma instância de **Msvm \_ VirtualHardDiskSettingData**, o cliente pode usar essa propriedade para obter a ID de disco exclusiva do VHD.</span><span class="sxs-lookup"><span data-stu-id="ceca9-210">When the [**Msvm\_ImageManagementService.GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) method returns an instance of **Msvm\_VirtualHardDiskSettingData**, the client can use this property to get the unique disk ID of the VHD.</span></span>

<span data-ttu-id="ceca9-211">Na detecção de conflitos ou de outra forma, um cliente pode definir o valor de **VirtualDiskId** para um novo GUID e passar essa instância do **Msvm \_ VirtualHardDiskSettingData** para o método [**Msvm \_ imagens. SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) para alterar a ID do disco do VHD.</span><span class="sxs-lookup"><span data-stu-id="ceca9-211">On conflict detection or otherwise, a client can set the **VirtualDiskId** value to a new GUID and pass this **Msvm\_VirtualHardDiskSettingData** instance to the [**Msvm\_ImageManagementService.SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) method to change the disk ID of the VHD.</span></span> <span data-ttu-id="ceca9-212">Se o VHD não for um VHD VHDX ou se o VHD estiver anexado, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="ceca9-212">If the VHD is not a VHDX VHD, or if the VHD is attached, the operation fails.</span></span> <span data-ttu-id="ceca9-213">A operação também falhará se o valor transmitido estiver malformado, ou seja, não for um GUID ou tiver todos 0s.</span><span class="sxs-lookup"><span data-stu-id="ceca9-213">The operation also fails if the passed value is malformed, that is, not a GUID or has all 0s.</span></span> <span data-ttu-id="ceca9-214">A operação será silenciosa com êxito se o valor passado for igual à ID do disco atual.</span><span class="sxs-lookup"><span data-stu-id="ceca9-214">The operation silently succeeds if the passed value is the same as the current disk ID.</span></span>

<span data-ttu-id="ceca9-215">Os erros gerados pela função [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) são emergidos por meio dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="ceca9-215">Errors generated by the [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) function are bubbled up through this property.</span></span> <span data-ttu-id="ceca9-216">Um cliente também pode usar o mesmo mecanismo para fornecer o valor de **VirtualDiskId** na criação do VHD por meio do método [**Msvm \_ imagens. CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) no mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="ceca9-216">A client can also use the same mechanism to provide the **VirtualDiskId** value at VHD creation via the [**Msvm\_ImageManagementService.CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) method in the same namespace.</span></span> <span data-ttu-id="ceca9-217">Isso pode ser usado para criar VHDs VHD1 ou VHD2.</span><span class="sxs-lookup"><span data-stu-id="ceca9-217">This can be used to create VHD1 or VHD2 VHDs.</span></span>

<span data-ttu-id="ceca9-218">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="ceca9-218">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ceca9-219">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ceca9-219">Requirements</span></span>



| <span data-ttu-id="ceca9-220">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceca9-220">Requirement</span></span> | <span data-ttu-id="ceca9-221">Valor</span><span class="sxs-lookup"><span data-stu-id="ceca9-221">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceca9-222">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ceca9-222">Minimum supported client</span></span><br/> | <span data-ttu-id="ceca9-223">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ceca9-223">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ceca9-224">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ceca9-224">Minimum supported server</span></span><br/> | <span data-ttu-id="ceca9-225">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ceca9-225">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ceca9-226">Namespace</span><span class="sxs-lookup"><span data-stu-id="ceca9-226">Namespace</span></span><br/>                | <span data-ttu-id="ceca9-227">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ceca9-227">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ceca9-228">MOF</span><span class="sxs-lookup"><span data-stu-id="ceca9-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ceca9-229"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ceca9-229"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ceca9-230">DLL</span><span class="sxs-lookup"><span data-stu-id="ceca9-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ceca9-231"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ceca9-231"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ceca9-232">Confira também</span><span class="sxs-lookup"><span data-stu-id="ceca9-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceca9-233">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="ceca9-233">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="ceca9-234">**GetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="ceca9-234">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 


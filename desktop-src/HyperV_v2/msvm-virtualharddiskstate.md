---
description: Fornece informações de estado para uma imagem de disco rígido virtual existente.
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Classe Msvm_VirtualHardDiskState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15d0a8b150e83c17946a6d1b66c7086383f08466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460968"
---
# <a name="msvm_virtualharddiskstate-class"></a><span data-ttu-id="fcaf0-103">\_Classe Msvm VirtualHardDiskState</span><span class="sxs-lookup"><span data-stu-id="fcaf0-103">Msvm\_VirtualHardDiskState class</span></span>

<span data-ttu-id="fcaf0-104">Fornece informações de estado para uma imagem de disco rígido virtual existente.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-104">Provides state information for an existing virtual hard disk image.</span></span>

<span data-ttu-id="fcaf0-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcaf0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcaf0-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a><span data-ttu-id="fcaf0-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fcaf0-107">Members</span></span>

<span data-ttu-id="fcaf0-108">A classe **Msvm \_ VirtualHardDiskState** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fcaf0-108">The **Msvm\_VirtualHardDiskState** class has these types of members:</span></span>

-   [<span data-ttu-id="fcaf0-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fcaf0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fcaf0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fcaf0-110">Properties</span></span>

<span data-ttu-id="fcaf0-111">A classe **Msvm \_ VirtualHardDiskState** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-111">The **Msvm\_VirtualHardDiskState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fcaf0-112">**Alinhamento**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-112">**Alignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcaf0-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcaf0-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcaf0-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcaf0-115">Especifica o tipo de alinhamento do disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-115">Specifies the type of alignment of the virtual hard disk.</span></span> <span data-ttu-id="fcaf0-116">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-116">This will be one of the following values.</span></span>



| <span data-ttu-id="fcaf0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="fcaf0-117">Value</span></span>                                                                        | <span data-ttu-id="fcaf0-118">Significado</span><span class="sxs-lookup"><span data-stu-id="fcaf0-118">Meaning</span></span>                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="fcaf0-119"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fcaf0-119"><dt>0</dt></span></span> </dl> | <span data-ttu-id="fcaf0-120">alinhamento de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-120">512 byte alignment.</span></span><br/> |
| <dl> <span data-ttu-id="fcaf0-121"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fcaf0-121"><dt>1</dt></span></span> </dl> | <span data-ttu-id="fcaf0-122">alinhamento de 4 KB.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-122">4 KB alignment.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="fcaf0-123">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-123">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcaf0-124">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcaf0-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcaf0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcaf0-126">O tamanho do arquivo de disco rígido virtual (a quantidade real de armazenamento que está sendo consumida pelo arquivo), em bytes.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-126">The size of the virtual hard disk file (the actual amount of storage being consumed by the file), in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fcaf0-127">**FragmentationPercentage**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-127">**FragmentationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcaf0-128">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcaf0-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcaf0-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcaf0-130">Uma aproximação da porcentagem de blocos de disco virtual que estão fragmentados no arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-130">An approximation of the percentage of virtual disk blocks that are fragmented in the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="fcaf0-131">**InUse**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-131">**InUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcaf0-132">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fcaf0-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcaf0-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcaf0-134">Esta propriedade está reservada para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-134">This property is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="fcaf0-135">**MinInternalSize**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-135">**MinInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcaf0-136">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcaf0-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcaf0-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcaf0-138">O tamanho mínimo no qual o disco rígido virtual pode ser reduzido, em bytes.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-138">The minimum size that the virtual hard disk can be shrunk to, in bytes.</span></span> <span data-ttu-id="fcaf0-139">Esse tamanho é arredondado para o próximo maior múltiplo do tamanho do setor.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-139">This size is rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="fcaf0-140">**PhysicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-140">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcaf0-141">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcaf0-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcaf0-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcaf0-143">O tamanho do setor físico usado pelo disco físico subjacente, em bytes.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-143">The physical sector size used by the underlying physical disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fcaf0-144">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-144">**Timestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcaf0-145">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="fcaf0-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcaf0-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcaf0-147">O carimbo de data/hora do disco rígido virtual</span><span class="sxs-lookup"><span data-stu-id="fcaf0-147">The timestamp of the virtual hard disk</span></span>

> [!Note]  
> <span data-ttu-id="fcaf0-148">Adicionado ao Windows 10 e ao Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="fcaf0-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fcaf0-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcaf0-149">Requirements</span></span>



| <span data-ttu-id="fcaf0-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcaf0-150">Requirement</span></span> | <span data-ttu-id="fcaf0-151">Valor</span><span class="sxs-lookup"><span data-stu-id="fcaf0-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcaf0-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcaf0-152">Minimum supported client</span></span><br/> | <span data-ttu-id="fcaf0-153">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fcaf0-153">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fcaf0-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcaf0-154">Minimum supported server</span></span><br/> | <span data-ttu-id="fcaf0-155">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fcaf0-155">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fcaf0-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="fcaf0-156">Namespace</span></span><br/>                | <span data-ttu-id="fcaf0-157">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fcaf0-157">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fcaf0-158">MOF</span><span class="sxs-lookup"><span data-stu-id="fcaf0-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcaf0-159"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fcaf0-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fcaf0-160">DLL</span><span class="sxs-lookup"><span data-stu-id="fcaf0-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcaf0-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fcaf0-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fcaf0-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcaf0-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcaf0-163">**GetVirtualHardDiskState**</span><span class="sxs-lookup"><span data-stu-id="fcaf0-163">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 





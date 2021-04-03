---
description: Fornece informações detalhadas sobre uma imagem de armazenamento montada manualmente.
ms.assetid: 40b94c5f-c277-40c8-a55d-ebc64cb231ca
title: Classe Msvm_MountedStorageImage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage
- Msvm_MountedStorageImage.InstanceID
- Msvm_MountedStorageImage.Caption
- Msvm_MountedStorageImage.Description
- Msvm_MountedStorageImage.ElementName
- Msvm_MountedStorageImage.InstallDate
- Msvm_MountedStorageImage.Name
- Msvm_MountedStorageImage.OperationalStatus
- Msvm_MountedStorageImage.StatusDescriptions
- Msvm_MountedStorageImage.Status
- Msvm_MountedStorageImage.HealthState
- Msvm_MountedStorageImage.CommunicationStatus
- Msvm_MountedStorageImage.DetailedStatus
- Msvm_MountedStorageImage.OperatingStatus
- Msvm_MountedStorageImage.PrimaryStatus
- Msvm_MountedStorageImage.Type
- Msvm_MountedStorageImage.Access
- Msvm_MountedStorageImage.PortNumber
- Msvm_MountedStorageImage.PathId
- Msvm_MountedStorageImage.TargetId
- Msvm_MountedStorageImage.Lun
- Msvm_MountedStorageImage.PnpDevicePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1b6f00b137fc73bcf8f79d39e6f7bfb5a6d7c944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663205"
---
# <a name="msvm_mountedstorageimage-class"></a><span data-ttu-id="c3efa-103">\_Classe Msvm MountedStorageImage</span><span class="sxs-lookup"><span data-stu-id="c3efa-103">Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="c3efa-104">Fornece informações detalhadas sobre uma imagem de armazenamento montada manualmente.</span><span class="sxs-lookup"><span data-stu-id="c3efa-104">Provides detailed information about a manually mounted storage image.</span></span>

<span data-ttu-id="c3efa-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c3efa-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3efa-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3efa-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MountedStorageImage : CIM_LogicalElement
{
  string   InstanceID;
  string   Caption = "Mounted Storage Image";
  string   Description = "Information about a mounted storage image.";
  string   ElementName = "Mounted Storage Image";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   Type;
  uint16   Access;
  UINT8    PortNumber;
  UINT8    PathId;
  UINT8    TargetId;
  UINT8    Lun;
  string   PnpDevicePath;
};
```

## <a name="members"></a><span data-ttu-id="c3efa-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c3efa-107">Members</span></span>

<span data-ttu-id="c3efa-108">A classe **Msvm \_ MountedStorageImage** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c3efa-108">The **Msvm\_MountedStorageImage** class has these types of members:</span></span>

-   [<span data-ttu-id="c3efa-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c3efa-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c3efa-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c3efa-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c3efa-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c3efa-111">Methods</span></span>

<span data-ttu-id="c3efa-112">A classe **Msvm \_ MountedStorageImage** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c3efa-112">The **Msvm\_MountedStorageImage** class has these methods.</span></span>



| <span data-ttu-id="c3efa-113">Método</span><span class="sxs-lookup"><span data-stu-id="c3efa-113">Method</span></span>                                                                          | <span data-ttu-id="c3efa-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3efa-114">Description</span></span>                                    |
|:--------------------------------------------------------------------------------|:-----------------------------------------------|
| [<span data-ttu-id="c3efa-115">**DetachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="c3efa-115">**DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md) | <span data-ttu-id="c3efa-116">Desanexa a imagem de armazenamento montada.</span><span class="sxs-lookup"><span data-stu-id="c3efa-116">Detaches the mounted storage image.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c3efa-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c3efa-117">Properties</span></span>

<span data-ttu-id="c3efa-118">A classe **Msvm \_ MountedStorageImage** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3efa-118">The **Msvm\_MountedStorageImage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3efa-119">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="c3efa-119">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-120">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3efa-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-122">O acesso no qual a imagem de armazenamento é montada.</span><span class="sxs-lookup"><span data-stu-id="c3efa-122">The access under which the storage image is mounted.</span></span>

<dt>

<span id="Read-only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="c3efa-123">**Somente leitura** (1)</span><span class="sxs-lookup"><span data-stu-id="c3efa-123">**Read-only** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="c3efa-124">**Leitura/gravação** (2)</span><span class="sxs-lookup"><span data-stu-id="c3efa-124">**Read/Write** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c3efa-125">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c3efa-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c3efa-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-128">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c3efa-128">A short description of the object.</span></span> <span data-ttu-id="c3efa-129">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre contém "imagem de armazenamento montada".</span><span class="sxs-lookup"><span data-stu-id="c3efa-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-130">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c3efa-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-131">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3efa-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-133">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="c3efa-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c3efa-134">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c3efa-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-135">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c3efa-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c3efa-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-138">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="c3efa-138">A description of the object.</span></span> <span data-ttu-id="c3efa-139">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre contém "informações sobre uma imagem de armazenamento montada".</span><span class="sxs-lookup"><span data-stu-id="c3efa-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Information about a mounted storage image.".</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-140">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c3efa-140">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-141">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3efa-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-143">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="c3efa-143">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c3efa-144">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c3efa-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c3efa-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c3efa-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-148">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c3efa-148">A display name for the object.</span></span> <span data-ttu-id="c3efa-149">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre contém "imagem de armazenamento montada".</span><span class="sxs-lookup"><span data-stu-id="c3efa-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c3efa-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3efa-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-153">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="c3efa-153">The current health of the element.</span></span> <span data-ttu-id="c3efa-154">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c3efa-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="c3efa-155">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="c3efa-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="c3efa-156">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5.</span><span class="sxs-lookup"><span data-stu-id="c3efa-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c3efa-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-158">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c3efa-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-160">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="c3efa-160">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="c3efa-161">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c3efa-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-162">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c3efa-162">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c3efa-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-165">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="c3efa-165">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-166">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="c3efa-166">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c3efa-167">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre **nula**.</span><span class="sxs-lookup"><span data-stu-id="c3efa-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-168">**LUN**</span><span class="sxs-lookup"><span data-stu-id="c3efa-168">**Lun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-169">Tipo de dados: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="c3efa-169">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-171">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c3efa-171">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-172">A ID do LUN do endereço SCSI.</span><span class="sxs-lookup"><span data-stu-id="c3efa-172">The SCSI address LUN ID.</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-173">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c3efa-173">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c3efa-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-176">O caminho para o VHD que é montado.</span><span class="sxs-lookup"><span data-stu-id="c3efa-176">The path to the VHD that is mounted.</span></span> <span data-ttu-id="c3efa-177">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c3efa-177">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-178">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c3efa-178">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-179">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3efa-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-181">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="c3efa-181">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c3efa-182">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c3efa-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-183">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c3efa-183">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-184">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3efa-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-186">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c3efa-186">The current status of the object.</span></span> <span data-ttu-id="c3efa-187">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c3efa-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-188">**Caminhoid**</span><span class="sxs-lookup"><span data-stu-id="c3efa-188">**PathId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-189">Tipo de dados: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="c3efa-189">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-191">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c3efa-191">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-192">A ID do caminho do endereço SCSI.</span><span class="sxs-lookup"><span data-stu-id="c3efa-192">The SCSI address path ID.</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-193">**PnpDevicePath**</span><span class="sxs-lookup"><span data-stu-id="c3efa-193">**PnpDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c3efa-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-196">O caminho do dispositivo PNP.</span><span class="sxs-lookup"><span data-stu-id="c3efa-196">The PNP device path.</span></span>

<span data-ttu-id="c3efa-197">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c3efa-197">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-198">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="c3efa-198">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-199">Tipo de dados: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="c3efa-199">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-201">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c3efa-201">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-202">O número da porta do endereço SCSI.</span><span class="sxs-lookup"><span data-stu-id="c3efa-202">The SCSI address port number.</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-203">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c3efa-203">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-204">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3efa-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-206">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="c3efa-206">Provides high level status information.</span></span> <span data-ttu-id="c3efa-207">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c3efa-207">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="c3efa-208">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c3efa-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-209">**Status**</span><span class="sxs-lookup"><span data-stu-id="c3efa-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-210">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c3efa-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-212">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "OK".</span><span class="sxs-lookup"><span data-stu-id="c3efa-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-213">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c3efa-213">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-214">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c3efa-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-216">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c3efa-216">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c3efa-217">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como "OK".</span><span class="sxs-lookup"><span data-stu-id="c3efa-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-218">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="c3efa-218">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-219">Tipo de dados: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="c3efa-219">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-221">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c3efa-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-222">A ID de destino do endereço SCSI.</span><span class="sxs-lookup"><span data-stu-id="c3efa-222">The SCSI address target ID.</span></span>

</dd> <dt>

<span data-ttu-id="c3efa-223">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c3efa-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3efa-224">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c3efa-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c3efa-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3efa-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3efa-226">O tipo de imagem de armazenamento montada.</span><span class="sxs-lookup"><span data-stu-id="c3efa-226">The type of storage image mounted.</span></span>

<dt>

<span id="Virtual_Hard_Disk"></span><span id="virtual_hard_disk"></span><span id="VIRTUAL_HARD_DISK"></span>

<span data-ttu-id="c3efa-227">**Disco rígido virtual** (0)</span><span class="sxs-lookup"><span data-stu-id="c3efa-227">**Virtual Hard Disk** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_Image"></span><span id="iso_image"></span><span id="ISO_IMAGE"></span>

<span data-ttu-id="c3efa-228">**Imagem ISO** (1)</span><span class="sxs-lookup"><span data-stu-id="c3efa-228">**ISO Image** (1)</span></span>


<span data-ttu-id="c3efa-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c3efa-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c3efa-230">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3efa-230">Remarks</span></span>

<span data-ttu-id="c3efa-231">O acesso à classe **Msvm \_ MountedStorageImage** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="c3efa-231">Access to the **Msvm\_MountedStorageImage** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c3efa-232">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c3efa-232">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3efa-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3efa-233">Requirements</span></span>



| <span data-ttu-id="c3efa-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3efa-234">Requirement</span></span> | <span data-ttu-id="c3efa-235">Valor</span><span class="sxs-lookup"><span data-stu-id="c3efa-235">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3efa-236">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3efa-236">Minimum supported client</span></span><br/> | <span data-ttu-id="c3efa-237">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c3efa-237">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c3efa-238">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3efa-238">Minimum supported server</span></span><br/> | <span data-ttu-id="c3efa-239">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c3efa-239">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3efa-240">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3efa-240">Namespace</span></span><br/>                | <span data-ttu-id="c3efa-241">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c3efa-241">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c3efa-242">MOF</span><span class="sxs-lookup"><span data-stu-id="c3efa-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3efa-243"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3efa-243"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3efa-244">DLL</span><span class="sxs-lookup"><span data-stu-id="c3efa-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3efa-245"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3efa-245"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c3efa-246">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3efa-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3efa-247">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="c3efa-247">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="c3efa-248">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="c3efa-248">**CIM\_LogicalElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalelement)
</dt> <dt>

[<span data-ttu-id="c3efa-249">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c3efa-249">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


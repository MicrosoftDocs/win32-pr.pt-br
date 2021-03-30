---
description: Gerencia os arquivos de mídia virtual (. VHD,. vhdx,. ISO ou. VFD) para uma máquina virtual.
ms.assetid: 7caa720e-37cf-454e-8634-f2bd82bcf83d
title: Classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService
- Msvm_ImageManagementService.InstanceID
- Msvm_ImageManagementService.Caption
- Msvm_ImageManagementService.Description
- Msvm_ImageManagementService.ElementName
- Msvm_ImageManagementService.InstallDate
- Msvm_ImageManagementService.OperationalStatus
- Msvm_ImageManagementService.StatusDescriptions
- Msvm_ImageManagementService.Status
- Msvm_ImageManagementService.HealthState
- Msvm_ImageManagementService.CommunicationStatus
- Msvm_ImageManagementService.DetailedStatus
- Msvm_ImageManagementService.OperatingStatus
- Msvm_ImageManagementService.PrimaryStatus
- Msvm_ImageManagementService.EnabledState
- Msvm_ImageManagementService.OtherEnabledState
- Msvm_ImageManagementService.RequestedState
- Msvm_ImageManagementService.EnabledDefault
- Msvm_ImageManagementService.TimeOfLastStateChange
- Msvm_ImageManagementService.AvailableRequestedStates
- Msvm_ImageManagementService.TransitioningToState
- Msvm_ImageManagementService.SystemCreationClassName
- Msvm_ImageManagementService.SystemName
- Msvm_ImageManagementService.CreationClassName
- Msvm_ImageManagementService.Name
- Msvm_ImageManagementService.PrimaryOwnerName
- Msvm_ImageManagementService.PrimaryOwnerContact
- Msvm_ImageManagementService.StartMode
- Msvm_ImageManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36a45041ec41b8fbd87801a65fa2b28ac99da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647367"
---
# <a name="msvm_imagemanagementservice-class"></a><span data-ttu-id="41ce6-103">\_Classe Msvm imagens</span><span class="sxs-lookup"><span data-stu-id="41ce6-103">Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="41ce6-104">Gerencia os arquivos de mídia virtual (. VHD,. vhdx,. ISO ou. VFD) para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="41ce6-104">Manages the virtual media (.vhd, .vhdx, .iso, or .vfd files) for a virtual machine.</span></span>

<span data-ttu-id="41ce6-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="41ce6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="41ce6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41ce6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ImageManagementService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Image Management Service";
  string   Description = "Provides Image Management servicing for Hyper-V";
  string   ElementName = "Hyper-V Image Management Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ImageManagementService";
  string   Name = "vhdsvc";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="41ce6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="41ce6-107">Members</span></span>

<span data-ttu-id="41ce6-108">A classe **Msvm \_ imagens** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="41ce6-108">The **Msvm\_ImageManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="41ce6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="41ce6-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="41ce6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41ce6-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="41ce6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="41ce6-111">Methods</span></span>

<span data-ttu-id="41ce6-112">A classe **Msvm \_ imagens** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="41ce6-112">The **Msvm\_ImageManagementService** class has these methods.</span></span>



| <span data-ttu-id="41ce6-113">Método</span><span class="sxs-lookup"><span data-stu-id="41ce6-113">Method</span></span>                                                                                                           | <span data-ttu-id="41ce6-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="41ce6-114">Description</span></span>                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41ce6-115">**AttachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="41ce6-115">**AttachVirtualHardDisk**</span></span>](attachvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="41ce6-116">Anexa um arquivo de imagem de disco virtual no modo de loopback.</span><span class="sxs-lookup"><span data-stu-id="41ce6-116">Attaches a virtual disk image file in loopback mode.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="41ce6-117">**CompactVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="41ce6-117">**CompactVirtualHardDisk**</span></span>](compactvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="41ce6-118">Compacta um arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="41ce6-118">Compacts a virtual hard disk file.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="41ce6-119">**ConvertVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="41ce6-119">**ConvertVirtualHardDisk**</span></span>](convertvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="41ce6-120">Converte um disco rígido virtual existente em um tipo ou formato diferente.</span><span class="sxs-lookup"><span data-stu-id="41ce6-120">Converts an existing virtual hard disk to a different type or format.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="41ce6-121">**ConvertVirtualHardDiskToVHDSet**</span><span class="sxs-lookup"><span data-stu-id="41ce6-121">**ConvertVirtualHardDiskToVHDSet**</span></span>](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md)             | <span data-ttu-id="41ce6-122">Converte um arquivo de disco rígido virtual criando um novo arquivo de conjunto de VHD junto com o disco rígido virtual existente.</span><span class="sxs-lookup"><span data-stu-id="41ce6-122">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="41ce6-123">**CreateVirtualFloppyDisk**</span><span class="sxs-lookup"><span data-stu-id="41ce6-123">**CreateVirtualFloppyDisk**</span></span>](createvirtualfloppydisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="41ce6-124">Cria um arquivo de disquete virtual.</span><span class="sxs-lookup"><span data-stu-id="41ce6-124">Creates a virtual floppy disk file.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="41ce6-125">**CreateVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="41ce6-125">**CreateVirtualHardDisk**</span></span>](createvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="41ce6-126">Cria um arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="41ce6-126">Creates a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="41ce6-127">**DeleteVHDSnapshot**</span><span class="sxs-lookup"><span data-stu-id="41ce6-127">**DeleteVHDSnapshot**</span></span>](msvm-imagemanagementservice-deletevhdsnapshot.md)                                       | <span data-ttu-id="41ce6-128">Exclui uma entrada de instantâneo VHD em um arquivo de conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="41ce6-128">Deletes a VHD Snapshot entry within a VHD Set file.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="41ce6-129">**FindMountedStorageImageInstance**</span><span class="sxs-lookup"><span data-stu-id="41ce6-129">**FindMountedStorageImageInstance**</span></span>](msvm-imagemanagementservice-findmountedstorageimageinstance.md)           | <span data-ttu-id="41ce6-130">Localiza um \_ objeto Msvm MountedStorageImage para um determinado caminho de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="41ce6-130">Finds a Msvm\_MountedStorageImage object for a given disk image path.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="41ce6-131">**GetVHDSetInformation**</span><span class="sxs-lookup"><span data-stu-id="41ce6-131">**GetVHDSetInformation**</span></span>](msvm-imagemanagementservice-getvhdsetinformation.md)                                 | <span data-ttu-id="41ce6-132">Recupera informações sobre um arquivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="41ce6-132">Retrieves information about a VHD Set file.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="41ce6-133">**GetVHDSnapshotInformation**</span><span class="sxs-lookup"><span data-stu-id="41ce6-133">**GetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-getvhdsnapshotinformation.md)                       | <span data-ttu-id="41ce6-134">Recupera informações sobre um instantâneo VHD em um arquivo de conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="41ce6-134">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="41ce6-135">**GetVirtualDiskChanges**</span><span class="sxs-lookup"><span data-stu-id="41ce6-135">**GetVirtualDiskChanges**</span></span>](msvm-imagemanagementservice-getvirtualdiskchanges.md)                               | <span data-ttu-id="41ce6-136">Recupera uma lista de alterações na região especificada de um disco virtual desde a ID de Controle de Alterações resiliente fornecida ou a ID de instantâneo VHDSet.</span><span class="sxs-lookup"><span data-stu-id="41ce6-136">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span><br/>                                                                                     |
| [<span data-ttu-id="41ce6-137">**GetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="41ce6-137">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="41ce6-138">Recupera dados de configuração associados a arquivos de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="41ce6-138">Retrieves setting data associated with virtual hard disk files.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="41ce6-139">**GetVirtualHardDiskState**</span><span class="sxs-lookup"><span data-stu-id="41ce6-139">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)                           | <span data-ttu-id="41ce6-140">Recupera o estado dos arquivos do disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="41ce6-140">Retrieves state of virtual hard disk files.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="41ce6-141">**MergeVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="41ce6-141">**MergeVirtualHardDisk**</span></span>](mergevirtualharddisk-msvm-imagemanagementservice.md)                                 | <span data-ttu-id="41ce6-142">Mescla um disco rígido virtual filho em uma cadeia diferencial com um ou mais discos rígidos virtuais pai na cadeia.</span><span class="sxs-lookup"><span data-stu-id="41ce6-142">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="41ce6-143">**OptimizeVHDSet**</span><span class="sxs-lookup"><span data-stu-id="41ce6-143">**OptimizeVHDSet**</span></span>](msvm-imagemanagementservice-optimizevhdset.md)                                             | <span data-ttu-id="41ce6-144">Otimiza um arquivo de conjunto VHD para usar menos espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="41ce6-144">Optimizes a VHD Set file to use less disk space.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="41ce6-145">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="41ce6-145">**RequestStateChange**</span></span>](msvm-imagemanagementservice-requeststatechange.md)                                     | <span data-ttu-id="41ce6-146">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="41ce6-146">Requests a state change.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="41ce6-147">**ResizeVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="41ce6-147">**ResizeVirtualHardDisk**</span></span>](resizevirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="41ce6-148">Redimensiona um disco rígido virtual existente.</span><span class="sxs-lookup"><span data-stu-id="41ce6-148">Resizes an existing virtual hard disk.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="41ce6-149">**SetParentVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="41ce6-149">**SetParentVirtualHardDisk**</span></span>](setparentvirtualharddisk-msvm-imagemanagementservice.md)                         | <span data-ttu-id="41ce6-150">Atualiza o pai para os arquivos de disco rígido virtual de folha e filho especificados.</span><span class="sxs-lookup"><span data-stu-id="41ce6-150">Updates the parent for the specified leaf and child virtual hard disk files.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="41ce6-151">**SetVHDSnapshotInformation**</span><span class="sxs-lookup"><span data-stu-id="41ce6-151">**SetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-setvhdsnapshotinformation.md)                       | <span data-ttu-id="41ce6-152">Edita uma entrada de instantâneo VHD em um arquivo de conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="41ce6-152">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="41ce6-153">Se a ID de instantâneo em questão já existir, a entrada de instantâneo existente será substituída pela nova entrada.</span><span class="sxs-lookup"><span data-stu-id="41ce6-153">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="41ce6-154">Caso contrário, a nova entrada será adicionada ao arquivo do conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="41ce6-154">Otherwise, the new entry will be added to the VHD Set file.</span></span><br/> |
| [<span data-ttu-id="41ce6-155">**SetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="41ce6-155">**SetVirtualHardDiskSettingData**</span></span>](setvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="41ce6-156">Define um arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="41ce6-156">Sets a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="41ce6-157">**StartService**</span><span class="sxs-lookup"><span data-stu-id="41ce6-157">**StartService**</span></span>](msvm-imagemanagementservice-startservice.md)                                                 | <span data-ttu-id="41ce6-158">Inicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="41ce6-158">Starts the service.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="41ce6-159">**StopService**</span><span class="sxs-lookup"><span data-stu-id="41ce6-159">**StopService**</span></span>](msvm-imagemanagementservice-stopservice.md)                                                   | <span data-ttu-id="41ce6-160">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="41ce6-160">Stops the service.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="41ce6-161">**ValidatePersistentReservationSupport**</span><span class="sxs-lookup"><span data-stu-id="41ce6-161">**ValidatePersistentReservationSupport**</span></span>](msvm-imagemanagementservice-validatepersistentreservationsupport.md) | <span data-ttu-id="41ce6-162">Valida se um sistema de arquivos pode dar suporte a um disco rígido virtual com reservas persistentes habilitadas.</span><span class="sxs-lookup"><span data-stu-id="41ce6-162">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="41ce6-163">**ValidateVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="41ce6-163">**ValidateVirtualHardDisk**</span></span>](validatevirtualharddisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="41ce6-164">Valida se uma imagem de disco virtual pode ser aberta no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="41ce6-164">Validates whether a virtual disk image can be opened in read-only mode.</span></span><br/>                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="41ce6-165">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41ce6-165">Properties</span></span>

<span data-ttu-id="41ce6-166">A classe **Msvm \_ imagens** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="41ce6-166">The **Msvm\_ImageManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41ce6-167">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="41ce6-167">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-168">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41ce6-168">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-170">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="41ce6-170">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="41ce6-171">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="41ce6-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-172">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="41ce6-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-175">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="41ce6-175">A short description of the object.</span></span> <span data-ttu-id="41ce6-176">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de gerenciamento de imagens do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="41ce6-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-177">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="41ce6-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-178">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41ce6-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-180">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="41ce6-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="41ce6-181">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="41ce6-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="41ce6-182">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41ce6-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="41ce6-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="41ce6-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="41ce6-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="41ce6-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="41ce6-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="41ce6-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="41ce6-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="41ce6-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="41ce6-190">)</span><span class="sxs-lookup"><span data-stu-id="41ce6-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41ce6-191">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="41ce6-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-194">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="41ce6-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="41ce6-195">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ imagens".</span><span class="sxs-lookup"><span data-stu-id="41ce6-195">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ImageManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-196">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="41ce6-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-199">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="41ce6-199">A description of the object.</span></span> <span data-ttu-id="41ce6-200">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "fornece serviço de gerenciamento de imagens para o Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="41ce6-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Image Management servicing for Hyper-V".</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="41ce6-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-202">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41ce6-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-204">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="41ce6-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="41ce6-205">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="41ce6-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="41ce6-206">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41ce6-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="41ce6-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="41ce6-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="41ce6-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="41ce6-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="41ce6-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="41ce6-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="41ce6-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="41ce6-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="41ce6-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="41ce6-215">)</span><span class="sxs-lookup"><span data-stu-id="41ce6-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41ce6-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="41ce6-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-219">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="41ce6-219">A display name for the object.</span></span> <span data-ttu-id="41ce6-220">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de gerenciamento de imagens do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="41ce6-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-221">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="41ce6-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-222">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41ce6-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-224">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="41ce6-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="41ce6-225">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="41ce6-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-226">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="41ce6-226">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-227">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41ce6-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-229">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="41ce6-229">The enabled and disabled states of an element.</span></span> <span data-ttu-id="41ce6-230">Ele também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="41ce6-230">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="41ce6-231">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="41ce6-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-232">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="41ce6-232">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-233">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41ce6-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-235">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="41ce6-235">The current health of the element.</span></span> <span data-ttu-id="41ce6-236">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="41ce6-236">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="41ce6-237">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="41ce6-237">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="41ce6-238">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5.</span><span class="sxs-lookup"><span data-stu-id="41ce6-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="41ce6-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-240">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="41ce6-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-242">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="41ce6-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="41ce6-243">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41ce6-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="41ce6-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-245">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-247">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="41ce6-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-248">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="41ce6-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="41ce6-249">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="41ce6-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-250">**Nome**</span><span class="sxs-lookup"><span data-stu-id="41ce6-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-253">Qualificadores: **Key**, **override** ("Name"), **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="41ce6-253">Qualifiers: **Key**, **Override** ("Name"), **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-254">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="41ce6-254">The label by which the object is known.</span></span> <span data-ttu-id="41ce6-255">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "vhdsvc".</span><span class="sxs-lookup"><span data-stu-id="41ce6-255">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "vhdsvc".</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-256">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="41ce6-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-257">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41ce6-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-259">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="41ce6-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="41ce6-260">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="41ce6-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="41ce6-261">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41ce6-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="41ce6-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="41ce6-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="41ce6-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="41ce6-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="41ce6-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="41ce6-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="41ce6-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="41ce6-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="41ce6-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="41ce6-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="41ce6-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="41ce6-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="41ce6-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="41ce6-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="41ce6-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="41ce6-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="41ce6-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="41ce6-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="41ce6-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="41ce6-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="41ce6-281">)</span><span class="sxs-lookup"><span data-stu-id="41ce6-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41ce6-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="41ce6-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-283">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41ce6-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-285">O status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="41ce6-285">The current status of the object.</span></span> <span data-ttu-id="41ce6-286">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="41ce6-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-287">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="41ce6-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-290">O estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="41ce6-290">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="41ce6-291">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="41ce6-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="41ce6-292">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="41ce6-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-293">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="41ce6-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-294">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-296">Uma cadeia de caracteres que fornece informações sobre como o proprietário principal do serviço pode ser alcançado (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="41ce6-296">A string that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="41ce6-297">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="41ce6-297">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-298">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="41ce6-298">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-299">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-301">O nome do proprietário principal do serviço, se um estiver definido.</span><span class="sxs-lookup"><span data-stu-id="41ce6-301">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="41ce6-302">O proprietário principal é o contato de suporte inicial para o serviço.</span><span class="sxs-lookup"><span data-stu-id="41ce6-302">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="41ce6-303">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="41ce6-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-304">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="41ce6-304">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-305">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41ce6-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-307">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="41ce6-307">Provides high level status information.</span></span> <span data-ttu-id="41ce6-308">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="41ce6-308">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="41ce6-309">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="41ce6-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="41ce6-310">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41ce6-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="41ce6-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="41ce6-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-312"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="41ce6-312"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="41ce6-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="41ce6-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="41ce6-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="41ce6-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="41ce6-317">)</span><span class="sxs-lookup"><span data-stu-id="41ce6-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41ce6-318">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="41ce6-318">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-319">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41ce6-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-321">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="41ce6-321">The last requested or desired state for the element.</span></span> <span data-ttu-id="41ce6-322">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="41ce6-322">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="41ce6-323">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="41ce6-323">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="41ce6-324">Uma instância específica do **EnabledLogicalElement** pode não dar suporte A **RequestedStateChange**.</span><span class="sxs-lookup"><span data-stu-id="41ce6-324">A particular instance of **EnabledLogicalElement** might not support **RequestedStateChange**.</span></span> <span data-ttu-id="41ce6-325">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="41ce6-325">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="41ce6-326">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="41ce6-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-327">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="41ce6-327">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-328">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="41ce6-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-330">Indica se o serviço foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="41ce6-330">Indicates whether the service has been started.</span></span> <span data-ttu-id="41ce6-331">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="41ce6-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-332">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="41ce6-332">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-333">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-335">Um valor de cadeia de caracteres que indica se o serviço é iniciado automaticamente por um sistema, um sistema operacional ou é iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="41ce6-335">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="41ce6-336">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="41ce6-336">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-337">**Status**</span><span class="sxs-lookup"><span data-stu-id="41ce6-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-338">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-340">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="41ce6-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-341">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="41ce6-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-342">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-344">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="41ce6-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="41ce6-345">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="41ce6-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-346">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="41ce6-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-347">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-349">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="41ce6-349">The scoping system's creation class name.</span></span> <span data-ttu-id="41ce6-350">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="41ce6-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-351">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="41ce6-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="41ce6-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-354">O nome do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="41ce6-354">The name of the hosting computer system.</span></span> <span data-ttu-id="41ce6-355">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="41ce6-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-356">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="41ce6-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-357">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="41ce6-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-359">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="41ce6-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="41ce6-360">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="41ce6-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="41ce6-361">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="41ce6-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41ce6-362">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41ce6-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41ce6-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ce6-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41ce6-364">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="41ce6-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="41ce6-365">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="41ce6-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41ce6-366">Comentários</span><span class="sxs-lookup"><span data-stu-id="41ce6-366">Remarks</span></span>

<span data-ttu-id="41ce6-367">O acesso à classe **Msvm \_ imagens** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="41ce6-367">Access to the **Msvm\_ImageManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="41ce6-368">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="41ce6-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="41ce6-369">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41ce6-369">Requirements</span></span>



| <span data-ttu-id="41ce6-370">Requisito</span><span class="sxs-lookup"><span data-stu-id="41ce6-370">Requirement</span></span> | <span data-ttu-id="41ce6-371">Valor</span><span class="sxs-lookup"><span data-stu-id="41ce6-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41ce6-372">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41ce6-372">Minimum supported client</span></span><br/> | <span data-ttu-id="41ce6-373">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="41ce6-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="41ce6-374">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41ce6-374">Minimum supported server</span></span><br/> | <span data-ttu-id="41ce6-375">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="41ce6-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41ce6-376">Namespace</span><span class="sxs-lookup"><span data-stu-id="41ce6-376">Namespace</span></span><br/>                | <span data-ttu-id="41ce6-377">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="41ce6-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="41ce6-378">MOF</span><span class="sxs-lookup"><span data-stu-id="41ce6-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41ce6-379"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41ce6-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41ce6-380">DLL</span><span class="sxs-lookup"><span data-stu-id="41ce6-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41ce6-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41ce6-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="41ce6-382">Confira também</span><span class="sxs-lookup"><span data-stu-id="41ce6-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41ce6-383">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="41ce6-383">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="41ce6-384">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="41ce6-384">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> <dt>

[<span data-ttu-id="41ce6-385">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="41ce6-385">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


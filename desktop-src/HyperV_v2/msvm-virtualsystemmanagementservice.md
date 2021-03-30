---
description: Representa o serviço de virtualização presente em um único sistema de host.
ms.assetid: 7f4bd9e0-b034-4882-ad01-f7df740939ae
title: Classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService
- Msvm_VirtualSystemManagementService.InstanceID
- Msvm_VirtualSystemManagementService.Caption
- Msvm_VirtualSystemManagementService.Description
- Msvm_VirtualSystemManagementService.ElementName
- Msvm_VirtualSystemManagementService.InstallDate
- Msvm_VirtualSystemManagementService.Name
- Msvm_VirtualSystemManagementService.OperationalStatus
- Msvm_VirtualSystemManagementService.StatusDescriptions
- Msvm_VirtualSystemManagementService.Status
- Msvm_VirtualSystemManagementService.HealthState
- Msvm_VirtualSystemManagementService.CommunicationStatus
- Msvm_VirtualSystemManagementService.DetailedStatus
- Msvm_VirtualSystemManagementService.OperatingStatus
- Msvm_VirtualSystemManagementService.PrimaryStatus
- Msvm_VirtualSystemManagementService.EnabledState
- Msvm_VirtualSystemManagementService.OtherEnabledState
- Msvm_VirtualSystemManagementService.RequestedState
- Msvm_VirtualSystemManagementService.EnabledDefault
- Msvm_VirtualSystemManagementService.TimeOfLastStateChange
- Msvm_VirtualSystemManagementService.AvailableRequestedStates
- Msvm_VirtualSystemManagementService.TransitioningToState
- Msvm_VirtualSystemManagementService.SystemCreationClassName
- Msvm_VirtualSystemManagementService.SystemName
- Msvm_VirtualSystemManagementService.CreationClassName
- Msvm_VirtualSystemManagementService.PrimaryOwnerName
- Msvm_VirtualSystemManagementService.PrimaryOwnerContact
- Msvm_VirtualSystemManagementService.StartMode
- Msvm_VirtualSystemManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ee79b9690f1eacdf7dc57a2ebfc2133091a1d55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646817"
---
# <a name="msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="dec7c-103">\_Classe Msvm VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="dec7c-103">Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="dec7c-104">Representa o serviço de virtualização presente em um único sistema de host.</span><span class="sxs-lookup"><span data-stu-id="dec7c-104">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="dec7c-105">**Msvm \_ VirtualSystemManagementService** é usado para controlar a definição, modificação e exclusão de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="dec7c-105">**Msvm\_VirtualSystemManagementService** is used to control the definition, modification, and deletion of virtual machines.</span></span> <span data-ttu-id="dec7c-106">Ele também tem métodos para executar operações em máquinas virtuais, como clonagem, instantâneo e importação ou exportação de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="dec7c-106">It also has methods for performing operations on virtual machines, such as cloning, snapshotting, and the importing or exporting of virtual machines.</span></span> <span data-ttu-id="dec7c-107">Para recuperar informações por máquina virtual, use o [**Msvm \_ ComputerSystem**](msvm-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="dec7c-107">To retrieve per-virtual machine information, use [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="dec7c-108">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="dec7c-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec7c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dec7c-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual System Management Service";
  string   Description = "Service for creating, manipulating, and managing virtual machines";
  string   ElementName = "Hyper-V Virtual System Management Service";
  datetime InstallDate;
  string   Name = "vmms";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
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
  string   CreationClassName = "Msvm_VirtualSystemManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="dec7c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="dec7c-110">Members</span></span>

<span data-ttu-id="dec7c-111">A classe **Msvm \_ VirtualSystemManagementService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dec7c-111">The **Msvm\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="dec7c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="dec7c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="dec7c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dec7c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dec7c-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="dec7c-114">Methods</span></span>

<span data-ttu-id="dec7c-115">A classe **Msvm \_ VirtualSystemManagementService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="dec7c-115">The **Msvm\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="dec7c-116">Método</span><span class="sxs-lookup"><span data-stu-id="dec7c-116">Method</span></span>                                                                                                                 | <span data-ttu-id="dec7c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="dec7c-117">Description</span></span>                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dec7c-118">**AddBootSourceSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-118">**AddBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)                             | <span data-ttu-id="dec7c-119">Adiciona fontes de inicialização a uma configuração de sistema virtual quando aplicada a uma configuração de sistema virtual "State".</span><span class="sxs-lookup"><span data-stu-id="dec7c-119">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="dec7c-120">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-120">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualsystemmanagementservice.md)                                   | <span data-ttu-id="dec7c-121">Adiciona configurações de recurso Ethernet à configuração de uma conexão Ethernet de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-121">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="dec7c-122">**AddFibreChannelChap**</span><span class="sxs-lookup"><span data-stu-id="dec7c-122">**AddFibreChannelChap**</span></span>](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="dec7c-123">Adiciona parâmetros DH-CHAP a uma porta de Fibre Channel sintética em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-123">Adds DH-CHAP parameters to a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="dec7c-124">**AddGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-124">**AddGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-addguestservicesettings.md)                         | <span data-ttu-id="dec7c-125">Adiciona configurações de serviço de convidado a uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-125">Adds guest service settings to a virtual system configuration.</span></span><br/> <span data-ttu-id="dec7c-126">Quando aplicado a partes de uma configuração de sistema virtual "atual", como um efeito colateral, os serviços convidados do sistema virtual ativo podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="dec7c-126">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>              |
| [<span data-ttu-id="dec7c-127">**AddKvpItems**</span><span class="sxs-lookup"><span data-stu-id="dec7c-127">**AddKvpItems**</span></span>](addkvpitems-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="dec7c-128">Adiciona pares de chave-valor a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-128">Adds key-value pairs to a virtual machine.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="dec7c-129">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-129">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="dec7c-130">Adiciona recursos a uma configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-130">Adds resources to a virtual machine configuration.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="dec7c-131">**AddSystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-131">**AddSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)                   | <span data-ttu-id="dec7c-132">Adiciona configurações genéricas a uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-132">Adds generic settings to a virtual system configuration.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="dec7c-133">**DefinePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="dec7c-133">**DefinePlannedSystem**</span></span>](msvm-virtualsystemmanagementservice-defineplannedsystem.md)                                 | <span data-ttu-id="dec7c-134">Define um sistema virtual planejado.</span><span class="sxs-lookup"><span data-stu-id="dec7c-134">Defines a planned virtual system.</span></span><br/> <span data-ttu-id="dec7c-135">A entrada que não está completamente especificada pode ser preenchida com valores padrão.</span><span class="sxs-lookup"><span data-stu-id="dec7c-135">Input that is not completely specified may be filled out with default values.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="dec7c-136">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="dec7c-136">**DefineSystem**</span></span>](definesystem-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="dec7c-137">Cria uma nova definição de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-137">Creates a new virtual machine definition.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="dec7c-138">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="dec7c-138">**DestroySystem**</span></span>](destroysystem-msvm-virtualsystemmanagementservice.md)                                             | <span data-ttu-id="dec7c-139">Exclui uma definição de máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="dec7c-139">Deletes an existing virtual machine definition.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="dec7c-140">**DiagnoseNetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="dec7c-140">**DiagnoseNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)                     | <span data-ttu-id="dec7c-141">Diagnostica a conectividade de rede de uma VM em um ambiente de virtualização de rede do Windows.</span><span class="sxs-lookup"><span data-stu-id="dec7c-141">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="dec7c-142">**ExportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="dec7c-142">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="dec7c-143">Exporta uma máquina virtual, ou um instantâneo de uma máquina virtual, para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="dec7c-143">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="dec7c-144">**FormatError**</span><span class="sxs-lookup"><span data-stu-id="dec7c-144">**FormatError**</span></span>](formaterror-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="dec7c-145">Retorna uma cadeia de caracteres de mensagem de erro formatada para a matriz especificada de instâncias de [**\_ erro Msvm**](msvm-error.md) inseridas.</span><span class="sxs-lookup"><span data-stu-id="dec7c-145">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="dec7c-146">**GenerateWwpn**</span><span class="sxs-lookup"><span data-stu-id="dec7c-146">**GenerateWwpn**</span></span>](generatewwpn-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="dec7c-147">Gera um conjunto de WWNs (World Wide Port Names).</span><span class="sxs-lookup"><span data-stu-id="dec7c-147">Generates a set of World Wide Port Names (WWPNs).</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="dec7c-148">**GetCurrentWwpnFromGenerator**</span><span class="sxs-lookup"><span data-stu-id="dec7c-148">**GetCurrentWwpnFromGenerator**</span></span>](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)                 | <span data-ttu-id="dec7c-149">Fornece a capacidade de visualizar o WWPN (World Wide Port Name) atual sem o WWPN sendo reservado.</span><span class="sxs-lookup"><span data-stu-id="dec7c-149">Provides the ability to preview the current World Wide Port Name (WWPN) without the WWPN being reserved.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="dec7c-150">**GetDefinitionFileSummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="dec7c-150">**GetDefinitionFileSummaryInformation**</span></span>](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="dec7c-151">Retorna informações de resumo da máquina virtual para os arquivos de definição de máquina virtual especificados.</span><span class="sxs-lookup"><span data-stu-id="dec7c-151">Returns virtual machine summary information for the specified virtual machine definition files.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="dec7c-152">**GetSizeOfSystemFiles**</span><span class="sxs-lookup"><span data-stu-id="dec7c-152">**GetSizeOfSystemFiles**</span></span>](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="dec7c-153">Recupera o tamanho total dos arquivos do sistema da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-153">Retrieves the total size of the system files of virtual machine.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="dec7c-154">**GetSummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="dec7c-154">**GetSummaryInformation**</span></span>](getsummaryinformation-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="dec7c-155">Retorna informações de resumo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-155">Returns virtual machine summary information.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="dec7c-156">**GetVirtualSystemThumbnailImage**</span><span class="sxs-lookup"><span data-stu-id="dec7c-156">**GetVirtualSystemThumbnailImage**</span></span>](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)           | <span data-ttu-id="dec7c-157">Recupera uma imagem em miniatura de uma máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="dec7c-157">Retrieves a thumbnail image of an existing virtual machine.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="dec7c-158">**ImportSnapshotDefinitions**</span><span class="sxs-lookup"><span data-stu-id="dec7c-158">**ImportSnapshotDefinitions**</span></span>](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)                     | <span data-ttu-id="dec7c-159">Pesquisa a pasta especificada em busca de quaisquer arquivos de definição de instantâneo associados ao sistema de computador planejado especificado e cria um novo instantâneo no sistema de computador planejado para cada arquivo de definição associado neste local.</span><span class="sxs-lookup"><span data-stu-id="dec7c-159">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span><br/> |
| [<span data-ttu-id="dec7c-160">**ImportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="dec7c-160">**ImportSystemDefinition**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="dec7c-161">Cria um novo sistema de computador planejado com base na definição de máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="dec7c-161">Creates a new planned computer system based on the specified virtual machine definition.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="dec7c-162">**ModifyDiskMergeSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-162">**ModifyDiskMergeSettings**</span></span>](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)                         | <span data-ttu-id="dec7c-163">Modifica os dados de configuração de mesclagem de disco.</span><span class="sxs-lookup"><span data-stu-id="dec7c-163">Modifies the disk merge setting data.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="dec7c-164">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-164">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="dec7c-165">Modifica as configurações de recurso atuais de uma conexão Ethernet de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-165">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="dec7c-166">**ModifyGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-166">**ModifyGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)                   | <span data-ttu-id="dec7c-167">Modifica as configurações do serviço convidado.</span><span class="sxs-lookup"><span data-stu-id="dec7c-167">Modifies guest service settings.</span></span><br/> <span data-ttu-id="dec7c-168">Quando aplicado a partes de uma configuração de sistema virtual "atual", como um efeito colateral, os serviços convidados do sistema virtual ativo podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="dec7c-168">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>                                            |
| [<span data-ttu-id="dec7c-169">**ModifyKvpItems**</span><span class="sxs-lookup"><span data-stu-id="dec7c-169">**ModifyKvpItems**</span></span>](modifykvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="dec7c-170">Modifica os pares de chave-valor existentes em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-170">Modifies existing key-value pairs on a virtual machine.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="dec7c-171">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-171">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="dec7c-172">Modifica as configurações de recursos virtuais.</span><span class="sxs-lookup"><span data-stu-id="dec7c-172">Modifies virtual resource settings.</span></span><br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="dec7c-173">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-173">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="dec7c-174">Modifica os dados de configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="dec7c-174">Modifies the service's setting data.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="dec7c-175">**ModifySystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-175">**ModifySystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)             | <span data-ttu-id="dec7c-176">Modifica as configurações genéricas do componente do sistema.</span><span class="sxs-lookup"><span data-stu-id="dec7c-176">Modifies generic system component settings.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="dec7c-177">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-177">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="dec7c-178">Modifica as configurações da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-178">Modifies virtual machine settings.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="dec7c-179">**RealizePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="dec7c-179">**RealizePlannedSystem**</span></span>](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="dec7c-180">Valida a configuração de uma máquina virtual planejada e a converte em uma máquina virtual realizada.</span><span class="sxs-lookup"><span data-stu-id="dec7c-180">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="dec7c-181">**RemoveBootSourceSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-181">**RemoveBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)                       | <span data-ttu-id="dec7c-182">Remove as configurações de recursos virtuais de uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-182">Removes virtual resource settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="dec7c-183">Quando aplicado a partes de uma configuração de sistema virtual "atual", como os recursos de efeito colateral do sistema virtual ativo podem ser removidos.</span><span class="sxs-lookup"><span data-stu-id="dec7c-183">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span><br/>            |
| [<span data-ttu-id="dec7c-184">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-184">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="dec7c-185">Remove as configurações de recurso de uma conexão Ethernet de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-185">Removes feature settings from a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="dec7c-186">**RemoveFibreChannelChap**</span><span class="sxs-lookup"><span data-stu-id="dec7c-186">**RemoveFibreChannelChap**</span></span>](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="dec7c-187">Remove os parâmetros DH-CHAP de uma porta de Fibre Channel sintética em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-187">Removes DH-CHAP parameters from a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="dec7c-188">**RemoveGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-188">**RemoveGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)                   | <span data-ttu-id="dec7c-189">Remove as configurações de serviço de convidado de uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-189">Removes guest service settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="dec7c-190">Quando aplicado a partes de uma configuração de sistema virtual "atual", como um efeito colateral, os serviços convidados do sistema virtual ativo podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="dec7c-190">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>         |
| [<span data-ttu-id="dec7c-191">**RemoveKvpItems**</span><span class="sxs-lookup"><span data-stu-id="dec7c-191">**RemoveKvpItems**</span></span>](removekvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="dec7c-192">Remove os pares de chave-valor existentes de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-192">Removes existing key-value pairs from a virtual machine.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="dec7c-193">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-193">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="dec7c-194">Remove as configurações de recursos virtuais de uma configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-194">Removes virtual resource settings from a virtual machine configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="dec7c-195">**RemoveSystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="dec7c-195">**RemoveSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)             | <span data-ttu-id="dec7c-196">Remove as configurações de componente genérico de uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-196">Removes generic component settings from a virtual system configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="dec7c-197">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="dec7c-197">**RequestStateChange**</span></span>](msvm-virtualsystemmanagementservice-requeststatechange.md)                                   | <span data-ttu-id="dec7c-198">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="dec7c-198">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="dec7c-199">**SetGuestNetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="dec7c-199">**SetGuestNetworkAdapterConfiguration**</span></span>](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="dec7c-200">Configura os adaptadores de rede no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="dec7c-200">Configures the network adapters within the guest operating system.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="dec7c-201">**SetInitialMachineConfigurationData**</span><span class="sxs-lookup"><span data-stu-id="dec7c-201">**SetInitialMachineConfigurationData**</span></span>](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)   | <span data-ttu-id="dec7c-202">Define os dados de configuração inicial da máquina VM.</span><span class="sxs-lookup"><span data-stu-id="dec7c-202">Sets a VM's initial machine configuration data.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="dec7c-203">**StartService**</span><span class="sxs-lookup"><span data-stu-id="dec7c-203">**StartService**</span></span>](msvm-virtualsystemmanagementservice-startservice.md)                                               | <span data-ttu-id="dec7c-204">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="dec7c-204">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="dec7c-205">**StopService**</span><span class="sxs-lookup"><span data-stu-id="dec7c-205">**StopService**</span></span>](msvm-virtualsystemmanagementservice-stopservice.md)                                                 | <span data-ttu-id="dec7c-206">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="dec7c-206">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="dec7c-207">**TestNetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="dec7c-207">**TestNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-testnetworkconnection.md)                             | <span data-ttu-id="dec7c-208">Testa a conectividade de rede de uma VM em um ambiente de virtualização de rede do Windows.</span><span class="sxs-lookup"><span data-stu-id="dec7c-208">Tests the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="dec7c-209">**UpgradeSystemVersion**</span><span class="sxs-lookup"><span data-stu-id="dec7c-209">**UpgradeSystemVersion**</span></span>](msvm-virtualsystemmanagementservice-upgradesystemversion.md)                               | <span data-ttu-id="dec7c-210">Atualiza o sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="dec7c-210">Upgrades the virtual system.</span></span><br/> <span data-ttu-id="dec7c-211">Quando aplicado às configurações do sistema de uma configuração de sistema virtual "atual"</span><span class="sxs-lookup"><span data-stu-id="dec7c-211">When applied to the system settings of a "current" virtual system configuration</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="dec7c-212">**ValidatePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="dec7c-212">**ValidatePlannedSystem**</span></span>](validateplannedsystem-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="dec7c-213">Valida o sistema planejado especificado.</span><span class="sxs-lookup"><span data-stu-id="dec7c-213">Validates the specified planned system.</span></span><br/>                                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="dec7c-214">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dec7c-214">Properties</span></span>

<span data-ttu-id="dec7c-215">A classe **Msvm \_ VirtualSystemManagementService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dec7c-215">The **Msvm\_VirtualSystemManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dec7c-216">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="dec7c-216">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-217">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dec7c-217">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-219">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="dec7c-219">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="dec7c-220">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dec7c-220">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-221">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="dec7c-221">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-224">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="dec7c-224">A short description of the object.</span></span> <span data-ttu-id="dec7c-225">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de gerenciamento de sistema virtual do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="dec7c-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-226">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="dec7c-226">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-227">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dec7c-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-229">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="dec7c-229">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="dec7c-230">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="dec7c-230">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dec7c-231">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dec7c-231">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dec7c-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="dec7c-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="dec7c-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="dec7c-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="dec7c-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="dec7c-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dec7c-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dec7c-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dec7c-239">)</span><span class="sxs-lookup"><span data-stu-id="dec7c-239">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dec7c-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dec7c-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-241">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-243">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="dec7c-243">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-244">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="dec7c-244">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="dec7c-245">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ VirtualSystemManagementService".</span><span class="sxs-lookup"><span data-stu-id="dec7c-245">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-246">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dec7c-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-249">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="dec7c-249">A description of the object.</span></span> <span data-ttu-id="dec7c-250">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço para criar, manipular e gerenciar máquinas virtuais".</span><span class="sxs-lookup"><span data-stu-id="dec7c-250">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, manipulating, and managing virtual machines".</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-251">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="dec7c-251">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-252">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dec7c-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-254">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="dec7c-254">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="dec7c-255">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="dec7c-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dec7c-256">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dec7c-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dec7c-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="dec7c-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="dec7c-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="dec7c-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="dec7c-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="dec7c-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="dec7c-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dec7c-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dec7c-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dec7c-265">)</span><span class="sxs-lookup"><span data-stu-id="dec7c-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dec7c-266">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dec7c-266">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-267">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-269">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="dec7c-269">A display name for the object.</span></span> <span data-ttu-id="dec7c-270">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de gerenciamento de sistema virtual do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="dec7c-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-271">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="dec7c-271">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-272">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dec7c-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-274">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="dec7c-274">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="dec7c-275">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="dec7c-275">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="dec7c-276">Valor</span><span class="sxs-lookup"><span data-stu-id="dec7c-276">Value</span></span>                                                                        | <span data-ttu-id="dec7c-277">Significado</span><span class="sxs-lookup"><span data-stu-id="dec7c-277">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="dec7c-278"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dec7c-278"><dt>2</dt></span></span> </dl> | <span data-ttu-id="dec7c-279">habilitado</span><span class="sxs-lookup"><span data-stu-id="dec7c-279">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dec7c-280">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="dec7c-280">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-281">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dec7c-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-283">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="dec7c-283">The enabled and disabled states of an element.</span></span> <span data-ttu-id="dec7c-284">Essa propriedade também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="dec7c-284">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="dec7c-285">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="dec7c-285">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="dec7c-286">Valor</span><span class="sxs-lookup"><span data-stu-id="dec7c-286">Value</span></span>                                                                        | <span data-ttu-id="dec7c-287">Significado</span><span class="sxs-lookup"><span data-stu-id="dec7c-287">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="dec7c-288"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dec7c-288"><dt>2</dt></span></span> </dl> | <span data-ttu-id="dec7c-289">habilitado</span><span class="sxs-lookup"><span data-stu-id="dec7c-289">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dec7c-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="dec7c-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-291">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dec7c-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-293">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="dec7c-293">The current health of the element.</span></span> <span data-ttu-id="dec7c-294">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="dec7c-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="dec7c-295">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="dec7c-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="dec7c-296">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="dec7c-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="dec7c-297">Valor</span><span class="sxs-lookup"><span data-stu-id="dec7c-297">Value</span></span>                                                                        | <span data-ttu-id="dec7c-298">Significado</span><span class="sxs-lookup"><span data-stu-id="dec7c-298">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="dec7c-299"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="dec7c-299"><dt>5</dt></span></span> </dl> | <span data-ttu-id="dec7c-300">O status de integridade é normal.</span><span class="sxs-lookup"><span data-stu-id="dec7c-300">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dec7c-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dec7c-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-302">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dec7c-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-304">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="dec7c-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="dec7c-305">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dec7c-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dec7c-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-309">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="dec7c-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-310">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="dec7c-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="dec7c-311">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dec7c-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-312">**Nome**</span><span class="sxs-lookup"><span data-stu-id="dec7c-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-315">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="dec7c-315">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-316">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="dec7c-316">The label by which the object is known.</span></span> <span data-ttu-id="dec7c-317">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "VMMS".</span><span class="sxs-lookup"><span data-stu-id="dec7c-317">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-318">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="dec7c-318">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-319">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dec7c-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-321">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="dec7c-321">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="dec7c-322">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="dec7c-322">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dec7c-323">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dec7c-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dec7c-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="dec7c-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="dec7c-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="dec7c-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="dec7c-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="dec7c-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="dec7c-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="dec7c-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="dec7c-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="dec7c-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="dec7c-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="dec7c-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="dec7c-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="dec7c-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="dec7c-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="dec7c-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="dec7c-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="dec7c-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dec7c-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dec7c-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dec7c-343">)</span><span class="sxs-lookup"><span data-stu-id="dec7c-343">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dec7c-344">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="dec7c-344">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-345">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dec7c-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-347">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="dec7c-347">The current statuses of the object.</span></span> <span data-ttu-id="dec7c-348">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="dec7c-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-349">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="dec7c-349">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-350">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-352">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="dec7c-352">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="dec7c-353">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="dec7c-353">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="dec7c-354">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dec7c-354">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-355">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="dec7c-355">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-356">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-358">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="dec7c-358">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-359">Todas as informações sobre como o proprietário principal do serviço podem ser atingidas (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="dec7c-359">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="dec7c-360">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="dec7c-360">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-361">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="dec7c-361">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-362">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-364">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="dec7c-364">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-365">O nome do proprietário principal do serviço, se um estiver definido.</span><span class="sxs-lookup"><span data-stu-id="dec7c-365">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="dec7c-366">O proprietário principal é o contato de suporte inicial para o serviço.</span><span class="sxs-lookup"><span data-stu-id="dec7c-366">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="dec7c-367">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="dec7c-367">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-368">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="dec7c-368">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-369">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dec7c-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-371">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="dec7c-371">Provides high level status information.</span></span> <span data-ttu-id="dec7c-372">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="dec7c-372">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="dec7c-373">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="dec7c-373">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dec7c-374">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dec7c-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dec7c-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="dec7c-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-376"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="dec7c-376"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="dec7c-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="dec7c-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dec7c-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dec7c-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dec7c-381">)</span><span class="sxs-lookup"><span data-stu-id="dec7c-381">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dec7c-382">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="dec7c-382">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-383">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dec7c-383">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-385">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="dec7c-385">The last requested or desired state for the element.</span></span> <span data-ttu-id="dec7c-386">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="dec7c-386">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="dec7c-387">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais para um elemento.</span><span class="sxs-lookup"><span data-stu-id="dec7c-387">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="dec7c-388">Uma instância específica da classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não oferecer suporte à propriedade **requestedstate** .</span><span class="sxs-lookup"><span data-stu-id="dec7c-388">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="dec7c-389">Se isso ocorrer, o valor 12 ("não aplicável") será usado.</span><span class="sxs-lookup"><span data-stu-id="dec7c-389">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="dec7c-390">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement** e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="dec7c-390">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="dec7c-391">Valor</span><span class="sxs-lookup"><span data-stu-id="dec7c-391">Value</span></span>                                                                         | <span data-ttu-id="dec7c-392">Significado</span><span class="sxs-lookup"><span data-stu-id="dec7c-392">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="dec7c-393"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="dec7c-393"><dt>12</dt></span></span> </dl> | <span data-ttu-id="dec7c-394">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="dec7c-394">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dec7c-395">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="dec7c-395">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-396">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="dec7c-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-398">Indica se o serviço está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="dec7c-398">Indicates whether the service is currently running.</span></span> <span data-ttu-id="dec7c-399">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="dec7c-399">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-400">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="dec7c-400">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-401">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-403">Qualificadores: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="dec7c-403">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-404">Um valor de cadeia de caracteres que indica se o serviço é iniciado automaticamente por um sistema, um sistema operacional ou é iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="dec7c-404">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="dec7c-405">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="dec7c-405">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-406">**Status**</span><span class="sxs-lookup"><span data-stu-id="dec7c-406">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-407">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-409">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="dec7c-409">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-410">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="dec7c-410">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-411">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-411">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-412">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-413">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="dec7c-413">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="dec7c-414">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), e cada elemento da matriz é sempre definido como "o serviço está sendo executado normalmente".</span><span class="sxs-lookup"><span data-stu-id="dec7c-414">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-415">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dec7c-415">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-416">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-417">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-418">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="dec7c-418">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-419">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="dec7c-419">The scoping system's creation class name.</span></span> <span data-ttu-id="dec7c-420">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="dec7c-420">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-421">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dec7c-421">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-422">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dec7c-422">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-423">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-424">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="dec7c-424">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-425">O nome NetBIOS do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="dec7c-425">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="dec7c-426">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="dec7c-426">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-427">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="dec7c-427">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-428">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dec7c-428">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-430">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="dec7c-430">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="dec7c-431">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dec7c-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="dec7c-432">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="dec7c-432">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec7c-433">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dec7c-433">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-434">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dec7c-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dec7c-435">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="dec7c-435">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="dec7c-436">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dec7c-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dec7c-437">Comentários</span><span class="sxs-lookup"><span data-stu-id="dec7c-437">Remarks</span></span>

<span data-ttu-id="dec7c-438">O acesso à classe **Msvm \_ VirtualSystemManagementService** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="dec7c-438">Access to the **Msvm\_VirtualSystemManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dec7c-439">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dec7c-439">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dec7c-440">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dec7c-440">Requirements</span></span>



| <span data-ttu-id="dec7c-441">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec7c-441">Requirement</span></span> | <span data-ttu-id="dec7c-442">Valor</span><span class="sxs-lookup"><span data-stu-id="dec7c-442">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec7c-443">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dec7c-443">Minimum supported client</span></span><br/> | <span data-ttu-id="dec7c-444">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dec7c-444">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dec7c-445">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dec7c-445">Minimum supported server</span></span><br/> | <span data-ttu-id="dec7c-446">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dec7c-446">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dec7c-447">Namespace</span><span class="sxs-lookup"><span data-stu-id="dec7c-447">Namespace</span></span><br/>                | <span data-ttu-id="dec7c-448">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dec7c-448">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dec7c-449">MOF</span><span class="sxs-lookup"><span data-stu-id="dec7c-449">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dec7c-450"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dec7c-450"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dec7c-451">DLL</span><span class="sxs-lookup"><span data-stu-id="dec7c-451">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dec7c-452"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dec7c-452"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dec7c-453">Confira também</span><span class="sxs-lookup"><span data-stu-id="dec7c-453">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec7c-454">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="dec7c-454">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="dec7c-455">[**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**](/previous-versions//cc136952(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dec7c-455">[**CIM\_VirtualSystemManagementService**](/previous-versions//cc136952(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="dec7c-456">[**Msvm \_ VirtualSystemManagementService (v1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dec7c-456">[**Msvm\_VirtualSystemManagementService (V1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dec7c-457">Classes de gerenciamento do sistema virtual</span><span class="sxs-lookup"><span data-stu-id="dec7c-457">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 


---
description: Representa uma coleção que fornece recursos de computação e consiste em \_ objetos CIM ManagedSystemElement.
ms.assetid: 410be43f-3368-4109-8b29-7b7cc2a3ec1b
title: Classe CIM_ComputerSystem (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.NameFormat
- CIM_ComputerSystem.Dedicated
- CIM_ComputerSystem.OtherDedicatedDescriptions
- CIM_ComputerSystem.ResetCapability
- CIM_ComputerSystem.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00a53d0c514113175c3c6ffb7ea40f8ef4e730d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759254"
---
# <a name="cim_computersystem-class-hyper-v-management"></a><span data-ttu-id="06982-103">Classe CIM_ComputerSystem (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="06982-103">CIM_ComputerSystem class (Hyper-V management)</span></span>

<span data-ttu-id="06982-104">Representa uma coleção que fornece recursos de computação e consiste em objetos [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="06982-104">Represents a collection that provides computing capabilities and consists of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="06982-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06982-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string NameFormat;
  uint16 Dedicated[];
  string OtherDedicatedDescriptions[];
  uint16 ResetCapability;
  uint16 PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="06982-106">Membros</span><span class="sxs-lookup"><span data-stu-id="06982-106">Members</span></span>

<span data-ttu-id="06982-107">A classe de **\_ sistema CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="06982-107">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="06982-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="06982-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="06982-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="06982-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="06982-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="06982-110">Methods</span></span>

<span data-ttu-id="06982-111">A classe de **\_ ComputerSystem de CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="06982-111">The **CIM\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="06982-112">Método</span><span class="sxs-lookup"><span data-stu-id="06982-112">Method</span></span>                                                    | <span data-ttu-id="06982-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="06982-113">Description</span></span>                                                                                                                                                                                                          |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06982-114">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="06982-114">**SetPowerState**</span></span>](cim-computersystem-setpowerstate.md) | <span data-ttu-id="06982-115">Esse método é preterido.</span><span class="sxs-lookup"><span data-stu-id="06982-115">This method is deprecated.</span></span> <span data-ttu-id="06982-116">Em vez disso, use o método **RequestPowerStateChange** na classe **CIM \_ PowerManagementService** .</span><span class="sxs-lookup"><span data-stu-id="06982-116">Instead, use the **RequestPowerStateChange** method in the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="06982-117">**Descrição preterida:** Define o estado de energia do computador.</span><span class="sxs-lookup"><span data-stu-id="06982-117">**Deprecated description:** Sets the power state of the computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="06982-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="06982-118">Properties</span></span>

<span data-ttu-id="06982-119">A classe de **\_ ComputerSystem de CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="06982-119">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06982-120">**Dedicado**</span><span class="sxs-lookup"><span data-stu-id="06982-120">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06982-121">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06982-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06982-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06982-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06982-123">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \| Serviços deMIB-II.sysIETF "," FC-GS. INCITS-T11 \| Platform \| platformtype "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ComputerSystem**.**OtherDedicatedDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="06982-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.sysServices", "FC-GS.INCITS-T11 \| Platform \| PlatformType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**OtherDedicatedDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="06982-124">A finalidade e os recursos do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="06982-124">The purpose and features of the computer system.</span></span> <span data-ttu-id="06982-125">Por exemplo, um sistema dedicado à impressão poderia especificar "11" (impressão).</span><span class="sxs-lookup"><span data-stu-id="06982-125">For example, a system dedicated to printing could specify "11" (Print).</span></span> <span data-ttu-id="06982-126">Um sistema de uso geral com recursos de impressão pode ser definido como "0" (não dedicado) e "11" (impressão).</span><span class="sxs-lookup"><span data-stu-id="06982-126">A general purpose system with printing capabilities can be set to "0" (Not Dedicated) and "11" (Print).</span></span>

<dt>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>

<span data-ttu-id="06982-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Não dedicado** (0)</span><span class="sxs-lookup"><span data-stu-id="06982-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Not Dedicated** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06982-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (1)</span><span class="sxs-lookup"><span data-stu-id="06982-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06982-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (2)</span><span class="sxs-lookup"><span data-stu-id="06982-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="06982-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Armazenamento** (3)</span><span class="sxs-lookup"><span data-stu-id="06982-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>

<span data-ttu-id="06982-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Roteador** (4)</span><span class="sxs-lookup"><span data-stu-id="06982-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Router** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="06982-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Opção** (5)</span><span class="sxs-lookup"><span data-stu-id="06982-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>

<span data-ttu-id="06982-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Comutador de camada 3** (6)</span><span class="sxs-lookup"><span data-stu-id="06982-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Layer 3 Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>

<span data-ttu-id="06982-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Comutador central do Office** (7)</span><span class="sxs-lookup"><span data-stu-id="06982-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Central Office Switch** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>

<span data-ttu-id="06982-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)</span><span class="sxs-lookup"><span data-stu-id="06982-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>

<span data-ttu-id="06982-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Servidor de acesso** (9)</span><span class="sxs-lookup"><span data-stu-id="06982-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Access Server** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>

<span data-ttu-id="06982-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)</span><span class="sxs-lookup"><span data-stu-id="06982-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="06982-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Imprimir** (11)</span><span class="sxs-lookup"><span data-stu-id="06982-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Print** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O"></span><span id="i_o"></span>

<span data-ttu-id="06982-139"><span id="I_O"></span><span id="i_o"></span>**E/s** (12)</span><span class="sxs-lookup"><span data-stu-id="06982-139"><span id="I_O"></span><span id="i_o"></span>**I/O** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>

<span data-ttu-id="06982-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Cache da Web** (13)</span><span class="sxs-lookup"><span data-stu-id="06982-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Web Caching** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>

<span data-ttu-id="06982-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Gerenciamento** (14)</span><span class="sxs-lookup"><span data-stu-id="06982-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Management** (14)</span></span>


</dt> <dd>

<span data-ttu-id="06982-142">Esta instância é dedicada à hospedagem do software de gerenciamento do sistema</span><span class="sxs-lookup"><span data-stu-id="06982-142">This instance is dedicated to hosting system management software</span></span>

</dd> <dt>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>

<span data-ttu-id="06982-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Servidor de blocos** (15)</span><span class="sxs-lookup"><span data-stu-id="06982-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Block Server** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>

<span data-ttu-id="06982-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**Servidor de arquivos** (16)</span><span class="sxs-lookup"><span data-stu-id="06982-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**File Server** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>

<span data-ttu-id="06982-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Dispositivo de usuário móvel** (17)</span><span class="sxs-lookup"><span data-stu-id="06982-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Mobile User Device** (17)</span></span>


</dt> <dd>

<span data-ttu-id="06982-146">Um exemplo de um dispositivo de usuário dedicado é um telefone celular ou um scanner de código de barras em um repositório que se comunica via radiofrequência.</span><span class="sxs-lookup"><span data-stu-id="06982-146">An example of a dedicated user device is a mobile phone or a barcode scanner in a store that communicates via radio frequency.</span></span> <span data-ttu-id="06982-147">Esses sistemas são bastante limitados em funcionalidade e programação e não são considerados plataformas de computação de "finalidade geral".</span><span class="sxs-lookup"><span data-stu-id="06982-147">These systems are quite limited in functionality and programmability, and are not considered 'general purpose' computing platforms.</span></span> <span data-ttu-id="06982-148">Como alternativa, um exemplo de um sistema móvel que é ' finalidade geral ' (ou seja, não é dedicado) é um computador de bolso.</span><span class="sxs-lookup"><span data-stu-id="06982-148">Alternately, an example of a mobile system that is 'general purpose' (i.e., is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="06982-149">Embora limitado em sua programação, o novo software pode ser baixado e sua funcionalidade expandida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="06982-149">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span>

</dd> <dt>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>

<span data-ttu-id="06982-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)</span><span class="sxs-lookup"><span data-stu-id="06982-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>

<span data-ttu-id="06982-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Ponte/extensor** (19)</span><span class="sxs-lookup"><span data-stu-id="06982-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Bridge/Extender** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>

<span data-ttu-id="06982-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Gateway** (20)</span><span class="sxs-lookup"><span data-stu-id="06982-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Gateway** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>

<span data-ttu-id="06982-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Virtualização de armazenamento** (21)</span><span class="sxs-lookup"><span data-stu-id="06982-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Storage Virtualizer** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>

<span data-ttu-id="06982-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Biblioteca de mídia** (22)</span><span class="sxs-lookup"><span data-stu-id="06982-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Media Library** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>

<span data-ttu-id="06982-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)</span><span class="sxs-lookup"><span data-stu-id="06982-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>

<span data-ttu-id="06982-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**Cabeçalho do nas** (24)</span><span class="sxs-lookup"><span data-stu-id="06982-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**NAS Head** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>

<span data-ttu-id="06982-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**Nas** independente (25)</span><span class="sxs-lookup"><span data-stu-id="06982-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**Self-contained NAS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="UPS"></span><span id="ups"></span>

<span data-ttu-id="06982-158"><span id="UPS"></span><span id="ups"></span>**Ups** (26)</span><span class="sxs-lookup"><span data-stu-id="06982-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>

<span data-ttu-id="06982-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**Telefone IP** (27)</span><span class="sxs-lookup"><span data-stu-id="06982-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**IP Phone** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>

<span data-ttu-id="06982-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Controlador de gerenciamento** (28)</span><span class="sxs-lookup"><span data-stu-id="06982-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Management Controller** (28)</span></span>


</dt> <dd>

<span data-ttu-id="06982-161">Essa instância representa um hardware especializado dedicado ao gerenciamento de sistemas (ou seja, um controlador BMC ou processador de serviço).</span><span class="sxs-lookup"><span data-stu-id="06982-161">This instance represents specialized hardware dedicated to systems management (i.e., a Baseboard Management Controller (BMC) or service processor).</span></span>

<span data-ttu-id="06982-162">O escopo de gerenciamento de um "controlador de gerenciamento" é normalmente um único sistema gerenciado no qual ele está contido.</span><span class="sxs-lookup"><span data-stu-id="06982-162">The management scope of a "Management Controller" is typically a single managed system in which it is contained.</span></span>

</dd> <dt>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>

<span data-ttu-id="06982-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Gerente do chassi** (29)</span><span class="sxs-lookup"><span data-stu-id="06982-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Chassis Manager** (29)</span></span>


</dt> <dd>

<span data-ttu-id="06982-164">Essa instância representa um sistema dedicado ao gerenciamento de um chassi de folha e seus dispositivos independentes.</span><span class="sxs-lookup"><span data-stu-id="06982-164">This instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="06982-165">Esse valor seria usado para representar um controlador de prateleira.</span><span class="sxs-lookup"><span data-stu-id="06982-165">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="06982-166">Um "Gerenciador de chassis" é um ponto de agregação para gerenciamento e pode depender de controladores de gerenciamento subordinados para o gerenciamento de partes constituintes.</span><span class="sxs-lookup"><span data-stu-id="06982-166">A "Chassis Manager" is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span>

</dd> <dt>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>

<span data-ttu-id="06982-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Controlador RAID baseado em host** (30)</span><span class="sxs-lookup"><span data-stu-id="06982-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Host-based RAID controller** (30)</span></span>


</dt> <dd>

<span data-ttu-id="06982-168">Essa instância representa um controlador de armazenamento RAID contido em um computador host.</span><span class="sxs-lookup"><span data-stu-id="06982-168">This instance represents a RAID storage controller contained within a host computer.</span></span>

</dd> <dt>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>

<span data-ttu-id="06982-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Compartimento de dispositivo de armazenamento** (31)</span><span class="sxs-lookup"><span data-stu-id="06982-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Storage Device Enclosure** (31)</span></span>


</dt> <dd>

<span data-ttu-id="06982-170">Essa instância representa um compartimento que contém dispositivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="06982-170">This instance represents an enclosure that contains storage devices.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="06982-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Área de trabalho** (32)</span><span class="sxs-lookup"><span data-stu-id="06982-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="06982-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (33)</span><span class="sxs-lookup"><span data-stu-id="06982-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>

<span data-ttu-id="06982-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Biblioteca de fitas virtuais** (34)</span><span class="sxs-lookup"><span data-stu-id="06982-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Virtual Tape Library** (34)</span></span>


</dt> <dd>

<span data-ttu-id="06982-174">A emulação de uma biblioteca de fitas por um sistema de biblioteca virtual.</span><span class="sxs-lookup"><span data-stu-id="06982-174">The emulation of a tape library by a Virtual Library System.</span></span>

</dd> <dt>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>

<span data-ttu-id="06982-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Sistema de biblioteca virtual** (35)</span><span class="sxs-lookup"><span data-stu-id="06982-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Virtual Library System** (35)</span></span>


</dt> <dd>

<span data-ttu-id="06982-176">Usa o armazenamento em disco para emular bibliotecas de fitas</span><span class="sxs-lookup"><span data-stu-id="06982-176">Uses disk storage to emulate tape libraries</span></span>

</dd> <dt>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>

<span data-ttu-id="06982-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**PC de rede/cliente fino** (36)</span><span class="sxs-lookup"><span data-stu-id="06982-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**Network PC/Thin Client** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>

<span data-ttu-id="06982-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**Comutador FC** (37)</span><span class="sxs-lookup"><span data-stu-id="06982-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**FC Switch** (37)</span></span>


</dt> <dd>

<span data-ttu-id="06982-179">Dedicado a alternar quadros de Fibre Channel de camada 2.</span><span class="sxs-lookup"><span data-stu-id="06982-179">Dedicated to switching layer 2 fibre channel frames.</span></span>

</dd> <dt>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>

<span data-ttu-id="06982-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Comutador Ethernet** (38)</span><span class="sxs-lookup"><span data-stu-id="06982-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Ethernet Switch** (38)</span></span>


</dt> <dd>

<span data-ttu-id="06982-181">Dedicado a alternar quadros de Ethernet de camada 2</span><span class="sxs-lookup"><span data-stu-id="06982-181">Dedicated to switching layer 2 ethernet frames</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="06982-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="06982-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="06982-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32568.. 65535)</span><span class="sxs-lookup"><span data-stu-id="06982-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32568..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06982-184">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="06982-184">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06982-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="06982-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06982-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06982-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06982-187">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="06982-187">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="06982-188">O formato do nome do sistema do computador.</span><span class="sxs-lookup"><span data-stu-id="06982-188">The format of the computer system name.</span></span>

<dt>



 <span data-ttu-id="06982-189">("Outros")</span><span class="sxs-lookup"><span data-stu-id="06982-189">("Other")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-190">("IP")</span><span class="sxs-lookup"><span data-stu-id="06982-190">("IP")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-191">("Discar")</span><span class="sxs-lookup"><span data-stu-id="06982-191">("Dial")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-192">("HID")</span><span class="sxs-lookup"><span data-stu-id="06982-192">("HID")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-193">("NWA")</span><span class="sxs-lookup"><span data-stu-id="06982-193">("NWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-194">("HWA")</span><span class="sxs-lookup"><span data-stu-id="06982-194">("HWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-195">("X25")</span><span class="sxs-lookup"><span data-stu-id="06982-195">("X25")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-196">("ISDN")</span><span class="sxs-lookup"><span data-stu-id="06982-196">("ISDN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-197">("IPX")</span><span class="sxs-lookup"><span data-stu-id="06982-197">("IPX")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-198">("DCC")</span><span class="sxs-lookup"><span data-stu-id="06982-198">("DCC")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-199">("ICD")</span><span class="sxs-lookup"><span data-stu-id="06982-199">("ICD")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-200">("E. 164")</span><span class="sxs-lookup"><span data-stu-id="06982-200">("E.164")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-201">("SNA")</span><span class="sxs-lookup"><span data-stu-id="06982-201">("SNA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-202">("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="06982-202">("OID/OSI")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-203">("WWN")</span><span class="sxs-lookup"><span data-stu-id="06982-203">("WWN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="06982-204">("NAA")</span><span class="sxs-lookup"><span data-stu-id="06982-204">("NAA")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06982-205">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="06982-205">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06982-206">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="06982-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06982-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06982-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06982-208">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM ComputerSystem**.**Dedicado**")</span><span class="sxs-lookup"><span data-stu-id="06982-208">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**Dedicated**")</span></span>
</dt> </dl>

<span data-ttu-id="06982-209">Descreve como ou por que o sistema é dedicado quando a matriz **dedicada** inclui o valor 2 (outro).</span><span class="sxs-lookup"><span data-stu-id="06982-209">Describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="06982-210">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="06982-210">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06982-211">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06982-211">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06982-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06982-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06982-213">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities. PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controles de energia do sistema DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="06982-213">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="06982-214">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="06982-214">This property is deprecated.</span></span> <span data-ttu-id="06982-215">Em vez disso, use o método **PowerChangeCapabilities** na classe **CIM \_ PowerManagementCapabilitiesCIM \_ PowerManagementService** .</span><span class="sxs-lookup"><span data-stu-id="06982-215">Instead, use the **PowerChangeCapabilities** method in the **CIM\_PowerManagementCapabilitiesCIM\_PowerManagementService** class.</span></span>

<span data-ttu-id="06982-216">**Descrição preterida:** Os recursos de gerenciamento de energia do sistema.</span><span class="sxs-lookup"><span data-stu-id="06982-216">**Deprecated description:** The power management capabilities of the system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06982-217">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="06982-217">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="06982-218">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="06982-218">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="06982-219">**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="06982-219">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="06982-220">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="06982-220">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="06982-221">**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="06982-221">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="06982-222">**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="06982-222">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="06982-223">**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="06982-223">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="06982-224">**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="06982-224">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06982-225">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="06982-225">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06982-226">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06982-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06982-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06982-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06982-228">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Segurança de hardware do sistema DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="06982-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="06982-229">Indica se o sistema dá suporte à operação de redefinição de hardware.</span><span class="sxs-lookup"><span data-stu-id="06982-229">Indicates whether the system supports the hardware reset operation.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06982-230">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="06982-230">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06982-231">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="06982-231">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="06982-232">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="06982-232">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="06982-233">**Habilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="06982-233">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="06982-234">**Não implementado** (5)</span><span class="sxs-lookup"><span data-stu-id="06982-234">**Not Implemented** (5)</span></span>


<span data-ttu-id="06982-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="06982-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="06982-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06982-236">Requirements</span></span>



| <span data-ttu-id="06982-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="06982-237">Requirement</span></span> | <span data-ttu-id="06982-238">Valor</span><span class="sxs-lookup"><span data-stu-id="06982-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06982-239">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06982-239">Minimum supported client</span></span><br/> | <span data-ttu-id="06982-240">Windows 8</span><span class="sxs-lookup"><span data-stu-id="06982-240">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="06982-241">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06982-241">Minimum supported server</span></span><br/> | <span data-ttu-id="06982-242">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06982-242">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="06982-243">Namespace</span><span class="sxs-lookup"><span data-stu-id="06982-243">Namespace</span></span><br/>                | <span data-ttu-id="06982-244">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="06982-244">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="06982-245">MOF</span><span class="sxs-lookup"><span data-stu-id="06982-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06982-246"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06982-246"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06982-247">DLL</span><span class="sxs-lookup"><span data-stu-id="06982-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06982-248"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06982-248"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06982-249">Confira também</span><span class="sxs-lookup"><span data-stu-id="06982-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06982-250">**\_Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="06982-250">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 


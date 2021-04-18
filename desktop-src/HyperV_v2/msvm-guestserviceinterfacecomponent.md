---
description: Representa o estado do componente de interface do serviço de convidado, que fornece um mecanismo para interagir com a máquina virtual a partir das interfaces de gerenciamento no sistema host.
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Classe Msvm_GuestServiceInterfaceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent
- Msvm_GuestServiceInterfaceComponent.Availability
- Msvm_GuestServiceInterfaceComponent.Caption
- Msvm_GuestServiceInterfaceComponent.ConfigManagerErrorCode
- Msvm_GuestServiceInterfaceComponent.ConfigManagerUserConfig
- Msvm_GuestServiceInterfaceComponent.CreationClassName
- Msvm_GuestServiceInterfaceComponent.Description
- Msvm_GuestServiceInterfaceComponent.DeviceID
- Msvm_GuestServiceInterfaceComponent.ErrorCleared
- Msvm_GuestServiceInterfaceComponent.ErrorDescription
- Msvm_GuestServiceInterfaceComponent.InstallDate
- Msvm_GuestServiceInterfaceComponent.LastErrorCode
- Msvm_GuestServiceInterfaceComponent.Name
- Msvm_GuestServiceInterfaceComponent.PNPDeviceID
- Msvm_GuestServiceInterfaceComponent.PowerManagementCapabilities
- Msvm_GuestServiceInterfaceComponent.PowerManagementSupported
- Msvm_GuestServiceInterfaceComponent.Status
- Msvm_GuestServiceInterfaceComponent.StatusInfo
- Msvm_GuestServiceInterfaceComponent.SystemCreationClassName
- Msvm_GuestServiceInterfaceComponent.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4c55417edeee6d9a9fb15c474ba4ee9ca2dd93f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789803"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a><span data-ttu-id="20d50-103">\_Classe Msvm GuestServiceInterfaceComponent</span><span class="sxs-lookup"><span data-stu-id="20d50-103">Msvm\_GuestServiceInterfaceComponent class</span></span>

<span data-ttu-id="20d50-104">Representa o estado do componente de interface do serviço de convidado, que fornece um mecanismo para interagir com a máquina virtual a partir das interfaces de gerenciamento no sistema host.</span><span class="sxs-lookup"><span data-stu-id="20d50-104">Represents the state of the guest service interface component, which provides a mechanism to interact with the virtual machine from the management interfaces on the host system.</span></span> <span data-ttu-id="20d50-105">Essa classe deriva da classe [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .</span><span class="sxs-lookup"><span data-stu-id="20d50-105">This class derives from the [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) class.</span></span>

<span data-ttu-id="20d50-106">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="20d50-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="20d50-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20d50-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponent : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="20d50-108">Membros</span><span class="sxs-lookup"><span data-stu-id="20d50-108">Members</span></span>

<span data-ttu-id="20d50-109">A classe **Msvm \_ GuestServiceInterfaceComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="20d50-109">The **Msvm\_GuestServiceInterfaceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="20d50-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="20d50-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="20d50-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20d50-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="20d50-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="20d50-112">Methods</span></span>

<span data-ttu-id="20d50-113">A classe **Msvm \_ GuestServiceInterfaceComponent** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="20d50-113">The **Msvm\_GuestServiceInterfaceComponent** class has these methods.</span></span>



| <span data-ttu-id="20d50-114">Método</span><span class="sxs-lookup"><span data-stu-id="20d50-114">Method</span></span>                                                                               | <span data-ttu-id="20d50-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="20d50-115">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20d50-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="20d50-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestserviceinterfacecomponent.md) | <span data-ttu-id="20d50-117">Solicita que o estado do componente de interface do serviço de convidado seja alterado para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="20d50-117">Requests that the state of the guest service interface component be changed to the specified value.</span></span><br/>                           |
| [<span data-ttu-id="20d50-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="20d50-118">**Reset**</span></span>](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | <span data-ttu-id="20d50-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="20d50-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="20d50-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="20d50-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="20d50-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="20d50-121">**SetPowerState**</span></span>](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | <span data-ttu-id="20d50-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="20d50-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="20d50-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="20d50-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="20d50-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20d50-124">Properties</span></span>

<span data-ttu-id="20d50-125">A classe **Msvm \_ GuestServiceInterfaceComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="20d50-125">The **Msvm\_GuestServiceInterfaceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20d50-126">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="20d50-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20d50-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-129">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20d50-129">Availability and status of the device.</span></span>



| <span data-ttu-id="20d50-130">Valor</span><span class="sxs-lookup"><span data-stu-id="20d50-130">Value</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="20d50-131">Significado</span><span class="sxs-lookup"><span data-stu-id="20d50-131">Meaning</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="20d50-132"><dt>**Outros**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-132"><dt>**Other**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="20d50-133"><dt>**Desconhecido**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-133"><dt>**Unknown**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <span data-ttu-id="20d50-134"><dt>**Execução/energia completa**</dt> <dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-134"><dt>**Running/Full Power**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <span data-ttu-id="20d50-135"><dt>**Aviso**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-135"><dt>**Warning**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="20d50-136"><dt>**No teste**</dt> <dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-136"><dt>**In Test**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="20d50-137"><dt>**Não aplicável**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-137"><dt>**Not Applicable**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <span data-ttu-id="20d50-138"><dt>**Desligar**</dt> o <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-138"><dt>**Power Off**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <span data-ttu-id="20d50-139"><dt>**Off line**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-139"><dt>**Off Line**</dt> <dt>8 (0x8)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <span data-ttu-id="20d50-140"><dt>**Fora do imposto**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-140"><dt>**Off Duty**</dt> <dt>9 (0x9)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="20d50-141"><dt>**Degradado**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-141"><dt>**Degraded**</dt> <dt>10 (0xA)</dt></span></span> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <span data-ttu-id="20d50-142"><dt>**Não instalado**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-142"><dt>**Not Installed**</dt> <dt>11 (0xB)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <span data-ttu-id="20d50-143"><dt>**Erro de instalação**</dt> <dt>12 (0xc)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-143"><dt>**Install Error**</dt> <dt>12 (0xC)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <span data-ttu-id="20d50-144">Economia <dt>**de energia-**</dt> <dt>13 (0xD)</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="20d50-144"><dt>**Power Save - Unknown**</dt> <dt>13 (0xD)</dt></span></span> </dl>                             | <span data-ttu-id="20d50-145">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="20d50-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span><br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> <span data-ttu-id="20d50-146">Economia <dt>**de energia-modo de baixa energia**</dt> <dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-146"><dt>**Power Save - Low Power Mode**</dt> <dt>14 (0xE)</dt></span></span> </dl> | <span data-ttu-id="20d50-147">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="20d50-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span><br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <span data-ttu-id="20d50-148">Economia <dt>**de energia-em espera**</dt> <dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-148"><dt>**Power Save - Standby**</dt> <dt>15 (0xF)</dt></span></span> </dl>                             | <span data-ttu-id="20d50-149">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="20d50-149">The device is not functioning but could be brought to full power quickly.</span></span><br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <span data-ttu-id="20d50-150"><dt>**Ciclo de energia**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-150"><dt>**Power Cycle**</dt> <dt>16 (0x10)</dt></span></span> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> <span data-ttu-id="20d50-151">Economia <dt>**de energia-aviso**</dt> <dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-151"><dt>**Power Save - Warning**</dt> <dt>17 (0x11)</dt></span></span> </dl>                            | <span data-ttu-id="20d50-152">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="20d50-152">The device is in a warning state, though also in a power save mode.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="20d50-153">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="20d50-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d50-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-156">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="20d50-156">Short textual description of the object.</span></span> <span data-ttu-id="20d50-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="20d50-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="20d50-158">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="20d50-158">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-159">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20d50-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-161">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="20d50-161">Win32 Configuration Manager error code.</span></span>



| <span data-ttu-id="20d50-162">Valor</span><span class="sxs-lookup"><span data-stu-id="20d50-162">Value</span></span>                                                                                | <span data-ttu-id="20d50-163">Significado</span><span class="sxs-lookup"><span data-stu-id="20d50-163">Meaning</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20d50-164"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-164"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="20d50-165">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="20d50-165">Device is working properly.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="20d50-166"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-166"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="20d50-167">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="20d50-167">Device is not configured correctly.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="20d50-168"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-168"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="20d50-169">O Windows não pode carregar o driver para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20d50-169">Windows cannot load the driver for this device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="20d50-170"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-170"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="20d50-171">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="20d50-171">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span><br/>                             |
| <dl> <span data-ttu-id="20d50-172"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-172"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="20d50-173">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="20d50-173">Device is not working properly.</span></span> <span data-ttu-id="20d50-174">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="20d50-174">One of its drivers or the registry might be corrupted.</span></span><br/>                                        |
| <dl> <span data-ttu-id="20d50-175"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-175"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="20d50-176">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="20d50-176">Driver for the device requires a resource that Windows cannot manage.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="20d50-177"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-177"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="20d50-178">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="20d50-178">Boot configuration for the device conflicts with other devices.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="20d50-179"><dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-179"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="20d50-180">Não é possível filtrar.</span><span class="sxs-lookup"><span data-stu-id="20d50-180">Cannot filter.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="20d50-181"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-181"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="20d50-182">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="20d50-182">Driver loader for the device is missing.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="20d50-183"><dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-183"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="20d50-184">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20d50-184">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span><br/>               |
| <dl> <span data-ttu-id="20d50-185"><dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-185"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="20d50-186">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20d50-186">Device cannot start.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="20d50-187"><dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-187"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="20d50-188">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20d50-188">Device failed.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="20d50-189"><dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-189"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="20d50-190">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="20d50-190">Device cannot find enough free resources to use.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="20d50-191"><dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-191"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="20d50-192">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20d50-192">Windows cannot verify the device's resources.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="20d50-193"><dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-193"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="20d50-194">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="20d50-194">Device cannot work properly until the computer is restarted.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="20d50-195"><dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-195"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="20d50-196">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="20d50-196">Device is not working properly due to a possible re-enumeration problem.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="20d50-197"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-197"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="20d50-198">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="20d50-198">Windows cannot identify all of the resources that the device uses.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="20d50-199"><dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-199"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="20d50-200">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="20d50-200">Device is requesting an unknown resource type.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="20d50-201"><dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-201"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="20d50-202">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="20d50-202">Device drivers must be reinstalled.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="20d50-203"><dt>19 (0x13)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-203"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="20d50-204">Falha ao usar o carregador VxD.</span><span class="sxs-lookup"><span data-stu-id="20d50-204">Failure using the VxD loader.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="20d50-205"><dt>20 (0x14)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-205"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="20d50-206">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="20d50-206">Registry might be corrupted.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="20d50-207"><dt>21 (0x15)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-207"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="20d50-208">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="20d50-208">System failure.</span></span> <span data-ttu-id="20d50-209">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="20d50-209">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="20d50-210">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20d50-210">Windows is removing the device.</span></span><br/> |
| <dl> <span data-ttu-id="20d50-211"><dt>22 (0x16)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-211"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="20d50-212">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="20d50-212">Device is disabled.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="20d50-213"><dt>23 (0x17)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-213"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="20d50-214">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="20d50-214">System failure.</span></span> <span data-ttu-id="20d50-215">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="20d50-215">If changing the device driver is ineffective, see the hardware documentation.</span></span><br/>                                 |
| <dl> <span data-ttu-id="20d50-216"><dt>24 (0x18)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-216"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="20d50-217">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="20d50-217">Device is not present, not working properly, or does not have all of its drivers installed.</span></span><br/>                                   |
| <dl> <span data-ttu-id="20d50-218"><dt>25 (0x19)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-218"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="20d50-219">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20d50-219">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="20d50-220"><dt>26 (0x1A)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-220"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="20d50-221">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20d50-221">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="20d50-222"><dt>27 (0x1B)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-222"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="20d50-223">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="20d50-223">Device does not have valid log configuration.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="20d50-224"><dt>28 (0x1C)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-224"><dt>28 (0x1C)</dt></span></span> </dl> | <span data-ttu-id="20d50-225">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="20d50-225">Device drivers are not installed.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="20d50-226"><dt>29 (0x1D)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-226"><dt>29 (0x1D)</dt></span></span> </dl> | <span data-ttu-id="20d50-227">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="20d50-227">Device is disabled; the device firmware did not provide the required resources.</span></span><br/>                                               |
| <dl> <span data-ttu-id="20d50-228"><dt>30 (0x1E)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-228"><dt>30 (0x1E)</dt></span></span> </dl> | <span data-ttu-id="20d50-229">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="20d50-229">Device is using an IRQ resource that another device is using.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="20d50-230"><dt>31 (0x1F)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-230"><dt>31 (0x1F)</dt></span></span> </dl> | <span data-ttu-id="20d50-231">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="20d50-231">Device is not working properly; Windows cannot load the required device drivers.</span></span><br/>                                              |



 

</dd> <dt>

<span data-ttu-id="20d50-232">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="20d50-232">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-233">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="20d50-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-235">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="20d50-235">If **TRUE**, the device is using a user-defined configuration.</span></span>

</dd> <dt>

<span data-ttu-id="20d50-236">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="20d50-236">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d50-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-239">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="20d50-239">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="20d50-240">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="20d50-240">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="20d50-241">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="20d50-241">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d50-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-244">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="20d50-244">Textual description of the object.</span></span> <span data-ttu-id="20d50-245">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="20d50-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="20d50-246">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="20d50-246">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d50-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-249">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="20d50-249">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="20d50-250">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="20d50-250">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-251">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="20d50-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-253">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="20d50-253">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

</dd> <dt>

<span data-ttu-id="20d50-254">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="20d50-254">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-255">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d50-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-257">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="20d50-257">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

</dd> <dt>

<span data-ttu-id="20d50-258">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="20d50-258">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-259">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="20d50-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-261">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="20d50-261">Date and time the object was installed.</span></span> <span data-ttu-id="20d50-262">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="20d50-262">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="20d50-263">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="20d50-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="20d50-264">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="20d50-264">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-265">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20d50-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-267">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="20d50-267">Last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="20d50-268">**Nome**</span><span class="sxs-lookup"><span data-stu-id="20d50-268">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-269">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d50-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-271">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="20d50-271">Label by which the object is known.</span></span> <span data-ttu-id="20d50-272">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="20d50-272">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="20d50-273">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="20d50-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="20d50-274">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="20d50-274">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-275">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d50-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-277">Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="20d50-277">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="20d50-278">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="20d50-278">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="20d50-279">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="20d50-279">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-280">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20d50-280">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="20d50-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-282">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="20d50-282">Array of the specific power-related capabilities of a logical device.</span></span> <span data-ttu-id="20d50-283">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="20d50-283">This property is inherited from **CIM\_LogicalDevice**.</span></span>



| <span data-ttu-id="20d50-284">Valor</span><span class="sxs-lookup"><span data-stu-id="20d50-284">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="20d50-285">Significado</span><span class="sxs-lookup"><span data-stu-id="20d50-285">Meaning</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="20d50-286"><dt>**Desconhecido**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-286"><dt>**Unknown**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="20d50-287"><dt>**Sem suporte**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-287"><dt>**Not Supported**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="20d50-288"><dt>**Desabilitado**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-288"><dt>**Disabled**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="20d50-289"><dt>**Habilitado**</dt> <dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-289"><dt>**Enabled**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                                                                                                                     | <span data-ttu-id="20d50-290">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="20d50-290">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span><br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <span data-ttu-id="20d50-291"><dt>**Modos de economia de energia inseridos automaticamente**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-291"><dt>**Power Saving Modes Entered Automatically**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="20d50-292">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="20d50-292">The device can change its power state based on usage or other criteria.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <span data-ttu-id="20d50-293"><dt>**Estado de energia settable**</dt> <dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-293"><dt>**Power State Settable**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                 | <span data-ttu-id="20d50-294">Há suporte para o método [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) .</span><span class="sxs-lookup"><span data-stu-id="20d50-294">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method is supported.</span></span> <span data-ttu-id="20d50-295">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="20d50-295">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="20d50-296">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="20d50-296">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span><br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <span data-ttu-id="20d50-297"><dt>**Ciclo de energia com suporte**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-297"><dt>**Power Cycling Supported**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                                     | <span data-ttu-id="20d50-298">O método [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="20d50-298">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span><br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <span data-ttu-id="20d50-299"><dt>**Tempo de ativação com suporte de**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-299"><dt>**Timed Power On Supported**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                 | <span data-ttu-id="20d50-300">O método [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="20d50-300">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and *Time* set to a specific date and time, or interval, for power-on.</span></span><br/>                                                                                       |



 

</dd> <dt>

<span data-ttu-id="20d50-301">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="20d50-301">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-302">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="20d50-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-304">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="20d50-304">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="20d50-305">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="20d50-305">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="20d50-306">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="20d50-306">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="20d50-307">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="20d50-307">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="20d50-308">**Status**</span><span class="sxs-lookup"><span data-stu-id="20d50-308">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d50-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-311">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="20d50-311">Current status of the object.</span></span> <span data-ttu-id="20d50-312">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="20d50-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="20d50-313">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="20d50-313">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="20d50-314">**PROBLEMAS**</span><span class="sxs-lookup"><span data-stu-id="20d50-314">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="20d50-315">**Ao**</span><span class="sxs-lookup"><span data-stu-id="20d50-315">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="20d50-316">**Degradado**</span><span class="sxs-lookup"><span data-stu-id="20d50-316">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="20d50-317">**Conhecidos**</span><span class="sxs-lookup"><span data-stu-id="20d50-317">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="20d50-318">**"Falha de Pred"**</span><span class="sxs-lookup"><span data-stu-id="20d50-318">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="20d50-319">**Comece**</span><span class="sxs-lookup"><span data-stu-id="20d50-319">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="20d50-320">**Impedir**</span><span class="sxs-lookup"><span data-stu-id="20d50-320">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="20d50-321">**Serviço**</span><span class="sxs-lookup"><span data-stu-id="20d50-321">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="20d50-322">**Analisa**</span><span class="sxs-lookup"><span data-stu-id="20d50-322">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="20d50-323">**"Não recuperar"**</span><span class="sxs-lookup"><span data-stu-id="20d50-323">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="20d50-324">**"Sem contato"**</span><span class="sxs-lookup"><span data-stu-id="20d50-324">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="20d50-325">**"Perda de comunicação"**</span><span class="sxs-lookup"><span data-stu-id="20d50-325">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="20d50-326">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="20d50-326">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-327">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20d50-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-329">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="20d50-329">State of the logical device.</span></span> <span data-ttu-id="20d50-330">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="20d50-330">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span> <span data-ttu-id="20d50-331">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="20d50-331">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

<dl> <dt>

<span data-ttu-id="20d50-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="20d50-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1 (0x1))</span></span>
</dt> <dt>

<span data-ttu-id="20d50-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="20d50-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2 (0x2))</span></span>
</dt> <dt>

<span data-ttu-id="20d50-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="20d50-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3 (0x3))</span></span>
</dt> <dt>

<span data-ttu-id="20d50-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="20d50-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (4 (0x4))</span></span>
</dt> <dt>

<span data-ttu-id="20d50-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="20d50-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5 (0x5))</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="20d50-337">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="20d50-337">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-338">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d50-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-340">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="20d50-340">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="20d50-341">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="20d50-341">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d50-342">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d50-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d50-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d50-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20d50-344">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="20d50-344">Scoping system's name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20d50-345">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20d50-345">Requirements</span></span>



| <span data-ttu-id="20d50-346">Requisito</span><span class="sxs-lookup"><span data-stu-id="20d50-346">Requirement</span></span> | <span data-ttu-id="20d50-347">Valor</span><span class="sxs-lookup"><span data-stu-id="20d50-347">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d50-348">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20d50-348">Minimum supported client</span></span><br/> | <span data-ttu-id="20d50-349">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="20d50-349">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="20d50-350">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20d50-350">Minimum supported server</span></span><br/> | <span data-ttu-id="20d50-351">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="20d50-351">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="20d50-352">Namespace</span><span class="sxs-lookup"><span data-stu-id="20d50-352">Namespace</span></span><br/>                | <span data-ttu-id="20d50-353">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="20d50-353">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="20d50-354">MOF</span><span class="sxs-lookup"><span data-stu-id="20d50-354">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20d50-355"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-355"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20d50-356">DLL</span><span class="sxs-lookup"><span data-stu-id="20d50-356">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20d50-357"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20d50-357"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="20d50-358">Confira também</span><span class="sxs-lookup"><span data-stu-id="20d50-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20d50-359">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="20d50-359">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="20d50-360">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="20d50-360">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 


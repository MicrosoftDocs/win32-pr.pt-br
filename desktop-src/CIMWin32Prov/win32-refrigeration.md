---
description: A \_ refrigeração Win32 &\# 32; A classe WMI representa as propriedades de um dispositivo de refrigeração.
ms.assetid: d67ce648-5659-49e5-9427-7c4dbcdfda8c
ms.tgt_platform: multiple
title: Classe Win32_Refrigeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Refrigeration
- Win32_Refrigeration.Reset
- Win32_Refrigeration.SetPowerState
- Win32_Refrigeration.ActiveCooling
- Win32_Refrigeration.Availability
- Win32_Refrigeration.Caption
- Win32_Refrigeration.ConfigManagerErrorCode
- Win32_Refrigeration.ConfigManagerUserConfig
- Win32_Refrigeration.CreationClassName
- Win32_Refrigeration.Description
- Win32_Refrigeration.DeviceID
- Win32_Refrigeration.ErrorCleared
- Win32_Refrigeration.ErrorDescription
- Win32_Refrigeration.InstallDate
- Win32_Refrigeration.LastErrorCode
- Win32_Refrigeration.Name
- Win32_Refrigeration.PNPDeviceID
- Win32_Refrigeration.PowerManagementCapabilities
- Win32_Refrigeration.PowerManagementSupported
- Win32_Refrigeration.Status
- Win32_Refrigeration.StatusInfo
- Win32_Refrigeration.SystemCreationClassName
- Win32_Refrigeration.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23db1490d184cbfe38d6c5b65fa7190273ad2a87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920205"
---
# <a name="win32_refrigeration-class"></a><span data-ttu-id="07585-103">\_Classe de refrigeração Win32</span><span class="sxs-lookup"><span data-stu-id="07585-103">Win32\_Refrigeration class</span></span>

<span data-ttu-id="07585-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ refrigeração do Win32** representa as propriedades de um dispositivo de refrigeração.</span><span class="sxs-lookup"><span data-stu-id="07585-104">The **Win32\_Refrigeration** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a refrigeration device.</span></span>

<span data-ttu-id="07585-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="07585-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="07585-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="07585-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="07585-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07585-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB6-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_Refrigeration : CIM_Refrigeration
{
  boolean  ActiveCooling;
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

## <a name="members"></a><span data-ttu-id="07585-108">Membros</span><span class="sxs-lookup"><span data-stu-id="07585-108">Members</span></span>

<span data-ttu-id="07585-109">A classe de **\_ refrigeração Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="07585-109">The **Win32\_Refrigeration** class has these types of members:</span></span>

-   [<span data-ttu-id="07585-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="07585-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="07585-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="07585-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="07585-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="07585-112">Methods</span></span>

<span data-ttu-id="07585-113">A classe de **\_ refrigeração Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="07585-113">The **Win32\_Refrigeration** class has these methods.</span></span>



| <span data-ttu-id="07585-114">Método</span><span class="sxs-lookup"><span data-stu-id="07585-114">Method</span></span>            | <span data-ttu-id="07585-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="07585-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07585-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="07585-116">**Reset**</span></span>         | <span data-ttu-id="07585-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="07585-117">Not implemented.</span></span> <span data-ttu-id="07585-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) na [**\_ refrigeração CIM**](cim-refrigeration.md).</span><span class="sxs-lookup"><span data-stu-id="07585-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Refrigeration**](cim-refrigeration.md).</span></span><br/>                 |
| <span data-ttu-id="07585-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="07585-119">**SetPowerState**</span></span> | <span data-ttu-id="07585-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="07585-120">Not implemented.</span></span> <span data-ttu-id="07585-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) na [**\_ refrigeração CIM**](cim-refrigeration.md).</span><span class="sxs-lookup"><span data-stu-id="07585-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Refrigeration**](cim-refrigeration.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="07585-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="07585-122">Properties</span></span>

<span data-ttu-id="07585-123">A classe de **\_ refrigeração Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="07585-123">The **Win32\_Refrigeration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07585-124">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="07585-124">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-125">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="07585-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07585-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07585-127">Se **for verdadeiro**, o dispositivo de resfriamento fornece resfriamento ativo — não resfriamento passivo.</span><span class="sxs-lookup"><span data-stu-id="07585-127">If **TRUE**, the cooling device provides active cooling—not passive cooling.</span></span>

<span data-ttu-id="07585-128">Essa propriedade é herdada do [**CIM \_ CoolingDevice**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-128">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-129">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="07585-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07585-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07585-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-132">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="07585-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="07585-133">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07585-133">Availability and status of the device.</span></span>

<span data-ttu-id="07585-134">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="07585-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="07585-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07585-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="07585-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="07585-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="07585-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="07585-138">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="07585-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="07585-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="07585-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="07585-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="07585-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="07585-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="07585-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="07585-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="07585-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="07585-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="07585-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="07585-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="07585-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="07585-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="07585-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="07585-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="07585-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="07585-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="07585-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="07585-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="07585-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="07585-149">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="07585-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="07585-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="07585-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="07585-151">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="07585-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="07585-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="07585-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="07585-153">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="07585-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="07585-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="07585-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="07585-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="07585-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="07585-156">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="07585-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="07585-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="07585-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="07585-158">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="07585-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="07585-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="07585-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="07585-160">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="07585-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="07585-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="07585-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="07585-162">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="07585-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="07585-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="07585-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="07585-164">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="07585-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="07585-165">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="07585-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07585-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07585-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-168">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="07585-168">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="07585-169">Breve descrição do objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="07585-169">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="07585-170">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07585-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-171">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="07585-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-172">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07585-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07585-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-174">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="07585-174">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="07585-175">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="07585-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="07585-176">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="07585-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="07585-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="07585-178"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="07585-178">(0)</span></span>


</dt> <dd>

<span data-ttu-id="07585-179">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="07585-179">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="07585-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="07585-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="07585-181">(1)</span><span class="sxs-lookup"><span data-stu-id="07585-181">(1)</span></span>


</dt> <dd>

<span data-ttu-id="07585-182">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="07585-182">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="07585-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="07585-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="07585-184">(2)</span><span class="sxs-lookup"><span data-stu-id="07585-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="07585-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="07585-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="07585-186">(3)</span><span class="sxs-lookup"><span data-stu-id="07585-186">(3)</span></span>


</dt> <dd>

<span data-ttu-id="07585-187">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="07585-187">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="07585-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="07585-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="07585-189">(4)</span><span class="sxs-lookup"><span data-stu-id="07585-189">(4)</span></span>


</dt> <dd>

<span data-ttu-id="07585-190">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="07585-190">Device is not working properly.</span></span> <span data-ttu-id="07585-191">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="07585-191">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="07585-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="07585-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="07585-193">(5)</span><span class="sxs-lookup"><span data-stu-id="07585-193">(5)</span></span>


</dt> <dd>

<span data-ttu-id="07585-194">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="07585-194">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="07585-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="07585-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="07585-196"> (6)</span><span class="sxs-lookup"><span data-stu-id="07585-196">(6)</span></span>


</dt> <dd>

<span data-ttu-id="07585-197">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="07585-197">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="07585-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="07585-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="07585-199">(7)</span><span class="sxs-lookup"><span data-stu-id="07585-199">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="07585-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="07585-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="07585-201">(8)</span><span class="sxs-lookup"><span data-stu-id="07585-201">(8)</span></span>


</dt> <dd>

<span data-ttu-id="07585-202">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="07585-202">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="07585-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="07585-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="07585-204">(9)</span><span class="sxs-lookup"><span data-stu-id="07585-204">(9)</span></span>


</dt> <dd>

<span data-ttu-id="07585-205">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="07585-205">Device is not working properly.</span></span> <span data-ttu-id="07585-206">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07585-206">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="07585-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="07585-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="07585-208">(10)</span><span class="sxs-lookup"><span data-stu-id="07585-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="07585-209">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07585-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="07585-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="07585-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="07585-211">(11)</span><span class="sxs-lookup"><span data-stu-id="07585-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="07585-212">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07585-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="07585-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="07585-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="07585-214">12</span><span class="sxs-lookup"><span data-stu-id="07585-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="07585-215">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="07585-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="07585-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="07585-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="07585-217">(13)</span><span class="sxs-lookup"><span data-stu-id="07585-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="07585-218">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07585-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="07585-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="07585-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="07585-220">(14)</span><span class="sxs-lookup"><span data-stu-id="07585-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="07585-221">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="07585-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="07585-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="07585-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="07585-223">(15)</span><span class="sxs-lookup"><span data-stu-id="07585-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="07585-224">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="07585-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="07585-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="07585-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="07585-226">(16)</span><span class="sxs-lookup"><span data-stu-id="07585-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="07585-227">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="07585-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="07585-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="07585-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="07585-229">(17)</span><span class="sxs-lookup"><span data-stu-id="07585-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="07585-230">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="07585-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="07585-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="07585-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="07585-232">(18)</span><span class="sxs-lookup"><span data-stu-id="07585-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="07585-233">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="07585-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="07585-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="07585-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="07585-235">(19)</span><span class="sxs-lookup"><span data-stu-id="07585-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="07585-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="07585-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="07585-237">(20)</span><span class="sxs-lookup"><span data-stu-id="07585-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="07585-238">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="07585-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="07585-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="07585-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="07585-240">(21)</span><span class="sxs-lookup"><span data-stu-id="07585-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="07585-241">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="07585-241">System failure.</span></span> <span data-ttu-id="07585-242">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="07585-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="07585-243">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07585-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="07585-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="07585-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="07585-245">(22)</span><span class="sxs-lookup"><span data-stu-id="07585-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="07585-246">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="07585-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="07585-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="07585-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="07585-248">(23)</span><span class="sxs-lookup"><span data-stu-id="07585-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="07585-249">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="07585-249">System failure.</span></span> <span data-ttu-id="07585-250">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="07585-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="07585-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="07585-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="07585-252">(24)</span><span class="sxs-lookup"><span data-stu-id="07585-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="07585-253">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="07585-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="07585-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="07585-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="07585-255">(25)</span><span class="sxs-lookup"><span data-stu-id="07585-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="07585-256">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07585-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="07585-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="07585-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="07585-258">(26)</span><span class="sxs-lookup"><span data-stu-id="07585-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="07585-259">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07585-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="07585-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="07585-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="07585-261">(27)</span><span class="sxs-lookup"><span data-stu-id="07585-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="07585-262">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="07585-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="07585-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="07585-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="07585-264">(28)</span><span class="sxs-lookup"><span data-stu-id="07585-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="07585-265">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="07585-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="07585-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="07585-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="07585-267">(29)</span><span class="sxs-lookup"><span data-stu-id="07585-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="07585-268">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="07585-268">Device is disabled.</span></span> <span data-ttu-id="07585-269">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="07585-269">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="07585-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="07585-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="07585-271">(30)</span><span class="sxs-lookup"><span data-stu-id="07585-271">(30)</span></span>


</dt> <dd>

<span data-ttu-id="07585-272">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="07585-272">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="07585-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="07585-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="07585-274">(31)</span><span class="sxs-lookup"><span data-stu-id="07585-274">(31)</span></span>


</dt> <dd>

<span data-ttu-id="07585-275">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="07585-275">Device is not working properly.</span></span> <span data-ttu-id="07585-276">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="07585-276">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="07585-277">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="07585-277">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-278">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="07585-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07585-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-280">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="07585-280">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="07585-281">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="07585-281">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="07585-282">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="07585-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-284">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07585-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07585-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-286">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="07585-286">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="07585-287">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="07585-287">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="07585-288">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="07585-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="07585-289">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-290">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="07585-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-291">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07585-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07585-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-293">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="07585-293">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="07585-294">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="07585-294">Description of the object.</span></span>

<span data-ttu-id="07585-295">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07585-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="07585-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07585-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07585-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-299">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="07585-299">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="07585-300">Identificador exclusivo do dispositivo de refrigeração.</span><span class="sxs-lookup"><span data-stu-id="07585-300">Unique identifier of the refrigeration device.</span></span>

<span data-ttu-id="07585-301">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-302">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="07585-302">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-303">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="07585-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07585-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07585-305">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="07585-305">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="07585-306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-307">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="07585-307">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07585-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07585-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07585-310">Mais informações sobre o erro registrado em **LastErrorCode** e as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="07585-310">More information about the error recorded in **LastErrorCode**, and any corrective actions that may be taken.</span></span>

<span data-ttu-id="07585-311">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-312">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="07585-312">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-313">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="07585-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="07585-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-315">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="07585-315">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="07585-316">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="07585-316">Date and time the object was installed.</span></span> <span data-ttu-id="07585-317">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="07585-317">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="07585-318">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07585-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-319">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="07585-319">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-320">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07585-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07585-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07585-322">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="07585-322">Last error code reported by the logical device.</span></span>

<span data-ttu-id="07585-323">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-324">**Nome**</span><span class="sxs-lookup"><span data-stu-id="07585-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07585-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07585-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-327">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="07585-327">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="07585-328">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="07585-328">Label by which the object is known.</span></span> <span data-ttu-id="07585-329">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="07585-329">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="07585-330">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07585-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-331">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="07585-331">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-332">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07585-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07585-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-334">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="07585-334">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="07585-335">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="07585-335">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="07585-336">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="07585-337">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="07585-337">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="07585-338">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="07585-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-339">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07585-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="07585-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07585-341">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="07585-341">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="07585-342">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="07585-342">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07585-343"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="07585-343"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="07585-344"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="07585-344"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="07585-345">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07585-345">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="07585-346"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="07585-346"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="07585-347"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="07585-347"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="07585-348">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="07585-348">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="07585-349"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="07585-349"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="07585-350">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="07585-350">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="07585-351"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="07585-351"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="07585-352">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="07585-352">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="07585-353">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="07585-353">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="07585-354">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="07585-354">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="07585-355"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="07585-355"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="07585-356">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="07585-356">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="07585-357"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="07585-357"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="07585-358">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="07585-358">Timed Power-On Supported</span></span>

<span data-ttu-id="07585-359">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="07585-359">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="07585-360">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="07585-360">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-361">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="07585-361">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07585-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07585-363">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="07585-363">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="07585-364">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="07585-364">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="07585-365">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-366">**Status**</span><span class="sxs-lookup"><span data-stu-id="07585-366">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-367">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07585-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07585-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-369">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="07585-369">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="07585-370">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="07585-370">Current status of the object.</span></span> <span data-ttu-id="07585-371">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="07585-371">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="07585-372">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="07585-372">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="07585-373">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="07585-373">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="07585-374">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="07585-374">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="07585-375">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="07585-375">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="07585-376">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07585-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="07585-377">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="07585-377">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="07585-378">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="07585-378">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="07585-379">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="07585-379">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="07585-380">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="07585-380">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07585-381">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="07585-381">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="07585-382">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="07585-382">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="07585-383">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="07585-383">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="07585-384">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="07585-384">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="07585-385">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="07585-385">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="07585-386">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="07585-386">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="07585-387">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="07585-387">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="07585-388">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="07585-388">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="07585-389">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="07585-389">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07585-390">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="07585-390">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-391">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07585-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07585-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-393">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="07585-393">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="07585-394">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="07585-394">State of the logical device.</span></span> <span data-ttu-id="07585-395">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="07585-395">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="07585-396">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="07585-397">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="07585-397">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07585-398">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="07585-398">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="07585-399">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="07585-399">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="07585-400">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="07585-400">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="07585-401">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="07585-401">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07585-402">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="07585-402">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07585-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07585-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-405">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="07585-405">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="07585-406">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="07585-406">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="07585-407">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-407">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07585-408">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="07585-408">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07585-409">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="07585-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07585-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07585-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07585-411">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="07585-411">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="07585-412">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="07585-412">Name of the scoping system.</span></span>

<span data-ttu-id="07585-413">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="07585-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07585-414">Comentários</span><span class="sxs-lookup"><span data-stu-id="07585-414">Remarks</span></span>

<span data-ttu-id="07585-415">A classe de **\_ refrigeração Win32** é derivada [**da \_ refrigeração CIM**](cim-refrigeration.md).</span><span class="sxs-lookup"><span data-stu-id="07585-415">The **Win32\_Refrigeration** class is derived from [**CIM\_Refrigeration**](cim-refrigeration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07585-416">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07585-416">Requirements</span></span>



| <span data-ttu-id="07585-417">Requisito</span><span class="sxs-lookup"><span data-stu-id="07585-417">Requirement</span></span> | <span data-ttu-id="07585-418">Valor</span><span class="sxs-lookup"><span data-stu-id="07585-418">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07585-419">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07585-419">Minimum supported client</span></span><br/> | <span data-ttu-id="07585-420">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07585-420">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07585-421">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07585-421">Minimum supported server</span></span><br/> | <span data-ttu-id="07585-422">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07585-422">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07585-423">Namespace</span><span class="sxs-lookup"><span data-stu-id="07585-423">Namespace</span></span><br/>                | <span data-ttu-id="07585-424">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="07585-424">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07585-425">MOF</span><span class="sxs-lookup"><span data-stu-id="07585-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07585-426"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07585-426"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07585-427">DLL</span><span class="sxs-lookup"><span data-stu-id="07585-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07585-428"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07585-428"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07585-429">Confira também</span><span class="sxs-lookup"><span data-stu-id="07585-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07585-430">**\_Refrigeração CIM**</span><span class="sxs-lookup"><span data-stu-id="07585-430">**CIM\_Refrigeration**</span></span>](cim-refrigeration.md)
</dt> <dt>

[<span data-ttu-id="07585-431">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="07585-431">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

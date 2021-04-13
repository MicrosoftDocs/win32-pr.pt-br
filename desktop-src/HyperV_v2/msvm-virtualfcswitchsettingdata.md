---
description: Representa a configuração de um comutador Fibre Channel virtual.
ms.assetid: da2918a9-6e7f-4fee-9c13-7e75bbc6821f
title: Classe Msvm_VirtualFcSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitchSettingData
- Msvm_VirtualFcSwitchSettingData.InstanceID
- Msvm_VirtualFcSwitchSettingData.Caption
- Msvm_VirtualFcSwitchSettingData.Description
- Msvm_VirtualFcSwitchSettingData.ElementName
- Msvm_VirtualFcSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualFcSwitchSettingData.VirtualSystemType
- Msvm_VirtualFcSwitchSettingData.Notes
- Msvm_VirtualFcSwitchSettingData.CreationTime
- Msvm_VirtualFcSwitchSettingData.ConfigurationID
- Msvm_VirtualFcSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualFcSwitchSettingData.ConfigurationFile
- Msvm_VirtualFcSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualFcSwitchSettingData.SuspendDataRoot
- Msvm_VirtualFcSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualFcSwitchSettingData.LogDataRoot
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualFcSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualFcSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualFcSwitchSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67b6008ba1f5ba9849d6fcd9127c1a55c1da8290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501377"
---
# <a name="msvm_virtualfcswitchsettingdata-class"></a><span data-ttu-id="c7126-103">\_Classe Msvm VirtualFcSwitchSettingData</span><span class="sxs-lookup"><span data-stu-id="c7126-103">Msvm\_VirtualFcSwitchSettingData class</span></span>

<span data-ttu-id="c7126-104">Representa a configuração de um comutador Fibre Channel virtual.</span><span class="sxs-lookup"><span data-stu-id="c7126-104">Represents the configuration of a virtual Fibre Channel switch.</span></span>

<span data-ttu-id="c7126-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c7126-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7126-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7126-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitchSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a><span data-ttu-id="c7126-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c7126-107">Members</span></span>

<span data-ttu-id="c7126-108">A classe **Msvm \_ VirtualFcSwitchSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c7126-108">The **Msvm\_VirtualFcSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c7126-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7126-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7126-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c7126-110">Properties</span></span>

<span data-ttu-id="c7126-111">A classe **Msvm \_ VirtualFcSwitchSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c7126-111">The **Msvm\_VirtualFcSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7126-112">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="c7126-112">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-113">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7126-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-115">Ação a ser tomada para a máquina virtual quando o software executado pela máquina virtual falha.</span><span class="sxs-lookup"><span data-stu-id="c7126-115">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="c7126-116">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c7126-116">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7126-117">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="c7126-117">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-118">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7126-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-120">Ação a ser tomada para a máquina virtual quando o host for desligado.</span><span class="sxs-lookup"><span data-stu-id="c7126-120">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="c7126-121">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c7126-121">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7126-122">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="c7126-122">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-123">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7126-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-125">Ação a ser tomada para a máquina virtual quando o host for iniciado.</span><span class="sxs-lookup"><span data-stu-id="c7126-125">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="c7126-126">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c7126-126">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7126-127">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="c7126-127">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-128">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c7126-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-130">O tempo de atraso antes que a máquina virtual seja iniciada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c7126-130">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="c7126-131">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c7126-131">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7126-132">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="c7126-132">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-133">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7126-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-135">Um número que indica a sequência relativa de ativação da máquina virtual quando o sistema host é iniciado.</span><span class="sxs-lookup"><span data-stu-id="c7126-135">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="c7126-136">Um número mais baixo indica ativação anterior.</span><span class="sxs-lookup"><span data-stu-id="c7126-136">A lower number indicates earlier activation.</span></span> <span data-ttu-id="c7126-137">Se uma ou mais configurações mostrarem o mesmo valor, a sequência será dependente da implementação.</span><span class="sxs-lookup"><span data-stu-id="c7126-137">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="c7126-138">Um valor de 0 indica que a sequência é dependente de implementação.</span><span class="sxs-lookup"><span data-stu-id="c7126-138">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="c7126-139">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c7126-139">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7126-140">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c7126-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-143">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c7126-143">A short description of the object.</span></span> <span data-ttu-id="c7126-144">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c7126-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7126-145">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="c7126-145">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-148">O caminho de um diretório em que as informações sobre a configuração da máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="c7126-148">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="c7126-149">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7126-149">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7126-150">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="c7126-150">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-153">O caminho relativo e o nome de arquivo de um arquivo em que as informações sobre a configuração da máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="c7126-153">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="c7126-154">Esse caminho é relativo à propriedade **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="c7126-154">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="c7126-155">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7126-155">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7126-156">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="c7126-156">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-159">O identificador exclusivo da configuração.</span><span class="sxs-lookup"><span data-stu-id="c7126-159">The unique identifier of the configuration.</span></span> <span data-ttu-id="c7126-160">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7126-160">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7126-161">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="c7126-161">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-162">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c7126-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-164">A data e a hora em que as configurações foram criadas.</span><span class="sxs-lookup"><span data-stu-id="c7126-164">The date and time at which the settings were created.</span></span> <span data-ttu-id="c7126-165">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7126-165">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="c7126-166">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7126-166">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7126-167">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c7126-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-170">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="c7126-170">A description of the object.</span></span> <span data-ttu-id="c7126-171">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c7126-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c7126-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c7126-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-175">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="c7126-175">A display name for the object.</span></span> <span data-ttu-id="c7126-176">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7126-176">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7126-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c7126-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7126-180">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="c7126-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c7126-181">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="c7126-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c7126-182">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7126-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7126-183">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="c7126-183">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-186">O caminho de um diretório em que as informações de log para a máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="c7126-186">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="c7126-187">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c7126-187">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7126-188">**Observações**</span><span class="sxs-lookup"><span data-stu-id="c7126-188">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-189">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c7126-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-191">Notas fornecidas pelo usuário que estão relacionadas à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c7126-191">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="c7126-192">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7126-192">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7126-193">**Recuperação de**</span><span class="sxs-lookup"><span data-stu-id="c7126-193">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-196">O caminho completo de um arquivo em que as informações relacionadas à recuperação para a máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="c7126-196">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="c7126-197">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c7126-197">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7126-198">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="c7126-198">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-201">O caminho de um diretório em que as informações sobre os instantâneos de máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="c7126-201">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="c7126-202">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7126-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7126-203">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="c7126-203">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-204">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-206">O caminho de um diretório em que informações sobre as informações relacionadas à suspensão da máquina virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="c7126-206">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="c7126-207">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7126-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7126-208">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="c7126-208">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-209">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-211">O caminho de um diretório em que os arquivos de permuta para a máquina virtual são armazenados.</span><span class="sxs-lookup"><span data-stu-id="c7126-211">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="c7126-212">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="c7126-212">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c7126-213">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="c7126-213">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-216">O nome do objeto [**de \_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de dados CIM ao qual esses dados de configuração pertencem.</span><span class="sxs-lookup"><span data-stu-id="c7126-216">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="c7126-217">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7126-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c7126-218">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="c7126-218">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7126-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7126-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7126-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c7126-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7126-221">Especifica o tipo de máquina virtual que os dados de configuração representam.</span><span class="sxs-lookup"><span data-stu-id="c7126-221">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="c7126-222">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7126-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7126-223">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7126-223">Requirements</span></span>



| <span data-ttu-id="c7126-224">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7126-224">Requirement</span></span> | <span data-ttu-id="c7126-225">Valor</span><span class="sxs-lookup"><span data-stu-id="c7126-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7126-226">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7126-226">Minimum supported client</span></span><br/> | <span data-ttu-id="c7126-227">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c7126-227">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c7126-228">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7126-228">Minimum supported server</span></span><br/> | <span data-ttu-id="c7126-229">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c7126-229">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7126-230">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7126-230">Namespace</span></span><br/>                | <span data-ttu-id="c7126-231">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c7126-231">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c7126-232">MOF</span><span class="sxs-lookup"><span data-stu-id="c7126-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7126-233"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7126-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7126-234">DLL</span><span class="sxs-lookup"><span data-stu-id="c7126-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7126-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7126-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


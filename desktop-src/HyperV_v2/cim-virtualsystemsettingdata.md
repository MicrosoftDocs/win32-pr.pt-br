---
description: Descreve os aspectos virtuais de um sistema virtual por meio de um conjunto de propriedades específicas de virtualização. \_O CIM VirtualSystemSettingData também é usado como a classe de nível superior das configurações do sistema virtual.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: Classe CIM_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff2c9725c8469b3e2c29d2e98a708d27e80378f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756933"
---
# <a name="cim_virtualsystemsettingdata-class"></a><span data-ttu-id="cd1b5-104">\_Classe CIM VirtualSystemSettingData</span><span class="sxs-lookup"><span data-stu-id="cd1b5-104">CIM\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="cd1b5-105">Descreve os aspectos virtuais de um sistema virtual por meio de um conjunto de propriedades específicas de virtualização.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-105">Describes the virtual aspects of a virtual system through a set of virtualization specific properties.</span></span> <span data-ttu-id="cd1b5-106">**CIM \_ O VirtualSystemSettingData** também é usado como a classe de nível superior das configurações do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-106">**CIM\_VirtualSystemSettingData** is also used as the top level class of virtual system configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd1b5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd1b5-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
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

## <a name="members"></a><span data-ttu-id="cd1b5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cd1b5-108">Members</span></span>

<span data-ttu-id="cd1b5-109">A classe **CIM \_ VirtualSystemSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cd1b5-109">The **CIM\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="cd1b5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd1b5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd1b5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cd1b5-111">Properties</span></span>

<span data-ttu-id="cd1b5-112">A classe **CIM \_ VirtualSystemSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-112">The **CIM\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd1b5-113">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-113">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-116">A ação a ser tomada para o sistema virtual quando o software executado pelo sistema virtual falha.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-116">The action to take for the virtual system when the software executed by the virtual system fails.</span></span> <span data-ttu-id="cd1b5-117">As falhas abordadas por essa propriedade incluem apenas aquelas que podem ser detectadas pela plataforma de host, como uma condição de estado de espera não passível de interrupção.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-117">The failures addressed by this property only include those that are detectable by the host platform, such as a non-interruptible wait state condition.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="cd1b5-118">**Nenhum** (2)</span><span class="sxs-lookup"><span data-stu-id="cd1b5-118">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="cd1b5-119">**Reiniciar** (3)</span><span class="sxs-lookup"><span data-stu-id="cd1b5-119">**Restart** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

<span data-ttu-id="cd1b5-120">**Reverter para instantâneo** (4)</span><span class="sxs-lookup"><span data-stu-id="cd1b5-120">**Revert to snapshot** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cd1b5-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="cd1b5-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd1b5-122">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-122">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-123">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-125">A ação a ser tomada para o sistema virtual quando o host é desligado.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-125">The action to take for the virtual system when the host is shut down.</span></span>

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

<span data-ttu-id="cd1b5-126">**Desligar (2** )</span><span class="sxs-lookup"><span data-stu-id="cd1b5-126">**Turn Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

<span data-ttu-id="cd1b5-127">**Salvar estado** (3)</span><span class="sxs-lookup"><span data-stu-id="cd1b5-127">**Save state** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

<span data-ttu-id="cd1b5-128">**Desligamento** (4)</span><span class="sxs-lookup"><span data-stu-id="cd1b5-128">**Shutdown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cd1b5-129">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="cd1b5-129">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd1b5-130">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-130">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-131">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-133">A ação a ser tomada no sistema virtual quando o host é iniciado.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-133">The action to take on the virtual system when the host is started.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="cd1b5-134">**Nenhum** (2)</span><span class="sxs-lookup"><span data-stu-id="cd1b5-134">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

<span data-ttu-id="cd1b5-135">**Reiniciar se anteriormente ativo** (3)</span><span class="sxs-lookup"><span data-stu-id="cd1b5-135">**Restart if previously active** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

<span data-ttu-id="cd1b5-136">**Sempre inicialização** (4)</span><span class="sxs-lookup"><span data-stu-id="cd1b5-136">**Always startup** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="cd1b5-137">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="cd1b5-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cd1b5-138">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-138">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-139">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-141">O atraso para a ação de inicialização.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-141">The delay for the startup action.</span></span> <span data-ttu-id="cd1b5-142">Esse valor é uma variante de intervalo do tipo de dados **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="cd1b5-142">This value is an interval variant of the **datetime** data type.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b5-143">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-143">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-144">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-146">O número de sequência para ativação do sistema virtual quando o sistema host é iniciado.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-146">The sequence number for virtual system activation when the host system is started.</span></span> <span data-ttu-id="cd1b5-147">Um número mais baixo indica ativação anterior.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-147">A lower number indicates earlier activation.</span></span> <span data-ttu-id="cd1b5-148">Se uma ou mais configurações mostrarem o mesmo valor, a sequência será dependente da implementação.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-148">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="cd1b5-149">Um valor de "0" indica que a sequência é dependente de implementação.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-149">A value of "0" indicates that the sequence is implementation dependent.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b5-150">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-150">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-153">O caminho do arquivo do diretório em que as informações sobre a configuração do sistema virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-153">The file path of the directory where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="cd1b5-154">O formato dessa propriedade é um URI baseado em RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-154">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b5-155">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-155">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-158">O caminho relativo do arquivo em que as informações sobre a configuração do sistema virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-158">The relative path of the file where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="cd1b5-159">O caminho relativo é acrescentado ao valor da propriedade **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="cd1b5-159">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="cd1b5-160">O formato dessa propriedade é um URI baseado em RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-160">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b5-161">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-161">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-164">A ID exclusiva da configuração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-164">The unique id of the virtual system configuration.</span></span>

> [!Note]  
> <span data-ttu-id="cd1b5-165">**ConfigurationId** é diferente da **InstanceId** e é atribuída pela implementação a um sistema virtual ou a uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-165">**ConfigurationID** is different from the **InstanceID**, and is assigned by the implementation to a virtual system or a virtual system configuration.</span></span> <span data-ttu-id="cd1b5-166">**ConfigurationId** não é uma chave e o mesmo valor pode ocorrer para mais de uma instância.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-166">**ConfigurationID** is not a key, and the same value may occur for more than one instance.</span></span>

 

</dd> <dt>

<span data-ttu-id="cd1b5-167">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-167">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-168">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-170">A data e a hora em que a configuração do sistema virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-170">The date and time when the virtual system configuration was created.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b5-171">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-171">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-174">O caminho de arquivo relativo do diretório onde as informações de log para o sistema virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-174">The relative file path of the directory where log information for the virtual system is stored.</span></span> <span data-ttu-id="cd1b5-175">O caminho relativo é acrescentado ao valor da propriedade **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="cd1b5-175">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="cd1b5-176">O formato dessa propriedade é um URI baseado em RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-176">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b5-177">**Observações**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-177">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-178">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-178">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-180">Uma matriz que contém notas fornecidas pelo usuário que estão relacionadas ao sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-180">An array that contains user supplied notes that are related to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b5-181">**Recuperação de**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-181">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-184">O caminho do arquivo em que as informações relacionadas à recuperação do sistema virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-184">The path of the file where recovery related information of the virtual system is stored.</span></span> <span data-ttu-id="cd1b5-185">O formato dessa propriedade é um URI baseado em RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-185">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b5-186">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-186">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-189">O caminho relativo do diretório em que as informações sobre instantâneos do sistema virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-189">The relative path of the directory where information about virtual system snapshots is stored.</span></span> <span data-ttu-id="cd1b5-190">O caminho relativo é acrescentado ao valor da propriedade **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="cd1b5-190">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="cd1b5-191">O formato dessa propriedade é um URI baseado em RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-191">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b5-192">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-192">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-195">O caminho relativo do diretório em que as informações relacionadas à suspensão do sistema virtual são armazenadas.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-195">The relative path of the directory where suspend related information about the virtual system is stored.</span></span> <span data-ttu-id="cd1b5-196">O caminho relativo é acrescentado ao valor da propriedade **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="cd1b5-196">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="cd1b5-197">O formato dessa propriedade é um URI baseado em RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-197">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b5-198">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-198">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-201">O caminho de arquivo relativo do diretório em que os arquivos de permuta do sistema virtual são armazenados.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-201">The relative file path of the directory where swap files of the virtual system are stored.</span></span> <span data-ttu-id="cd1b5-202">O caminho relativo é acrescentado ao valor da propriedade **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="cd1b5-202">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="cd1b5-203">O formato dessa propriedade é um URI baseado em RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-203">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b5-204">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-204">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-205">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-207">O nome exclusivo do sistema na plataforma de virtualização.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-207">The unique name for the system within the virtualization platform.</span></span> <span data-ttu-id="cd1b5-208">**VirtualSystemIdentifier** não é o nome do host atribuído à instância do sistema operacional em execução no sistema virtual, nem é um endereço IP ou endereço MAC atribuído a qualquer uma de suas portas de rede.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-208">**VirtualSystemIdentifier** is not the hostname assigned to the operating system instance running within the virtual system, nor is it an IP address or MAC address assigned to any of its network ports.</span></span>

<span data-ttu-id="cd1b5-209">O **VirtualSystemIdentifier** pode conter regras específicas de implementação, como padrões simples ou uma expressão regular que pode ser interpretada pela implementação ao definir **VirtualSystemIdentifier**.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-209">The **VirtualSystemIdentifier** may contain implementation specific rules, like simple patterns or a regular expression that may be interpreted by the implementation when setting **VirtualSystemIdentifier**.</span></span>

</dd> <dt>

<span data-ttu-id="cd1b5-210">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-210">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd1b5-211">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd1b5-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cd1b5-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd1b5-213">O tipo do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-213">The type of the virtual system.</span></span>

> [!Note]  
> <span data-ttu-id="cd1b5-214">Se o tipo de sistema virtual for desconhecido, esse valor deverá ser definido como "DMTF: Unknown".</span><span class="sxs-lookup"><span data-stu-id="cd1b5-214">If the virtual system type is unknown, this value must be set to "DMTF:unknown".</span></span>

 

<span data-ttu-id="cd1b5-215">Essa propriedade é formatada usando o seguinte formato de ABNF (Backus Naur Form):</span><span class="sxs-lookup"><span data-stu-id="cd1b5-215">This property is formatted using the following Augmented Backus Naur Form (ABNF) format:</span></span>

<span data-ttu-id="cd1b5-216">vs-tipo = DMTF-valor/outros-org-Value/herdado-Value; DMTF-Value = "DMTF:" definindo-org ":" org-vs-Type; Other-org-Value = definindo-org ":" org-vs-Type;</span><span class="sxs-lookup"><span data-stu-id="cd1b5-216">vs-type = dmtf-value / other-org-value / legacy-value; dmtf-value = "DMTF:" defining-org ":" org-vs-type; other-org-value = defining-org ":" org-vs-type;</span></span>

<span data-ttu-id="cd1b5-217">O valor do formato ABNF acima é:</span><span class="sxs-lookup"><span data-stu-id="cd1b5-217">The value of the above ABNF format are:</span></span>

-   <span data-ttu-id="cd1b5-218">*DMTF-valor*   um valor de propriedade definido pela DMTF e é definido na descrição dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-218">*dmtf-value*   a property value defined by DMTF and is defined in the description of this property.</span></span>
-   <span data-ttu-id="cd1b5-219">*outro-org-Value*   é um valor de propriedade definido por uma entidade comercial diferente de DMTF e não é definido na descrição dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-219">*other-org-value*   is a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span>
-   <span data-ttu-id="cd1b5-220">*Legacy-valor*   um valor de propriedade definido por uma entidade comercial diferente de DMTF e não é definido na descrição dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-220">*legacy-value*   a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span> <span data-ttu-id="cd1b5-221">Esses valores são permitidos, mas recomendamos que sejam preteridos ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-221">These values are permitted but recommended to be deprecated over time.</span></span>
-   <span data-ttu-id="cd1b5-222">*definindo-org*   um identificador para a entidade de negócios que define o tipo de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-222">*defining-org*   an identifier for the business entity that defines the virtual system type.</span></span> <span data-ttu-id="cd1b5-223">Ele deve incluir um nome de direitos autorais, com marcas registradas ou exclusivo de propriedade da entidade de negócios.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-223">It should include a copyrighted, trademarked, or a unique name that is owned by the business entity.</span></span> <span data-ttu-id="cd1b5-224">Não deveria ser "DMTF" e não deve conter dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-224">It should not be "DMTF" and shall not contain a colon.</span></span>
-   <span data-ttu-id="cd1b5-225">*org-vs-digite*   um identificador para o tipo de sistema virtual dentro da entidade de definição de negócio.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-225">*org-vs-type*   an identifier for the virtual system type within the defining business entity.</span></span> <span data-ttu-id="cd1b5-226">Ele deve ser exclusivo na definição-org. org-vs-Type pode usar qualquer caractere permitido para cadeias de caracteres CIM, exceto os seguintes: U0000-U001F (controles Unicode C0), U0020 (espaço), U007F (controles Unicode C0) ou U0080-U009F (controles Unicode C1).</span><span class="sxs-lookup"><span data-stu-id="cd1b5-226">It should be unique within defining-org. org-vs-type may use any character allowed for CIM strings, except the following: U0000-U001F (Unicode C0 controls), U0020 (space), U007F (Unicode C0 controls), or U0080-U009F (Unicode C1 controls).</span></span>
-   <span data-ttu-id="cd1b5-227">Se houver a necessidade de estruturar o valor em segmentos, os segmentos deverão ser separados por dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-227">If there is a need to structure the value into segments, the segments should be separated with a single colon.</span></span>
-   <span data-ttu-id="cd1b5-228">Os valores dessa propriedade devem ser processados com diferenciação de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-228">The values of this property should be processed case sensitively.</span></span> <span data-ttu-id="cd1b5-229">Eles devem ser processados programaticamente, em vez de serem um nome de exibição e deve ser curto.</span><span class="sxs-lookup"><span data-stu-id="cd1b5-229">They are intended to be processed programmatically, instead of being a display name, and should be short.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd1b5-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd1b5-230">Requirements</span></span>



| <span data-ttu-id="cd1b5-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd1b5-231">Requirement</span></span> | <span data-ttu-id="cd1b5-232">Valor</span><span class="sxs-lookup"><span data-stu-id="cd1b5-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd1b5-233">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd1b5-233">Minimum supported client</span></span><br/> | <span data-ttu-id="cd1b5-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cd1b5-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="cd1b5-235">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd1b5-235">Minimum supported server</span></span><br/> | <span data-ttu-id="cd1b5-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd1b5-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="cd1b5-237">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd1b5-237">Namespace</span></span><br/>                | <span data-ttu-id="cd1b5-238">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="cd1b5-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cd1b5-239">MOF</span><span class="sxs-lookup"><span data-stu-id="cd1b5-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd1b5-240"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd1b5-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd1b5-241">DLL</span><span class="sxs-lookup"><span data-stu-id="cd1b5-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd1b5-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd1b5-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd1b5-243">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd1b5-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd1b5-244">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="cd1b5-244">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 





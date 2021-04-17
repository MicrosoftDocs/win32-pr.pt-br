---
title: Métodos de propriedade IADsService (IADs. h)
description: Leia e grave as propriedades descritas neste tópico.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsService
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e0d8b09618c7346280697843281ca74536c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762801"
---
# <a name="iadsservice-property-methods"></a><span data-ttu-id="83a09-104">Métodos de propriedade IADsService</span><span class="sxs-lookup"><span data-stu-id="83a09-104">IADsService Property Methods</span></span>

<span data-ttu-id="83a09-105">Os métodos de propriedade da interface [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) lêem e gravam as propriedades descritas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="83a09-105">The property methods of the [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="83a09-106">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="83a09-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="83a09-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="83a09-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="83a09-108">**Dependências**</span><span class="sxs-lookup"><span data-stu-id="83a09-108">**Dependencies**</span></span>
<span data-ttu-id="83a09-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a09-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a09-110">Matriz de nomes **BSTR** de serviços ou grupos de carregamento que devem ser carregados para que esse serviço seja carregado.</span><span class="sxs-lookup"><span data-stu-id="83a09-110">Array of **BSTR** names of services or load groups that must be loaded for this service to load.</span></span> <span data-ttu-id="83a09-111">A sintaxe da entrada é "serviço:" seguida do nome do serviço ou "Grupo:" seguido pelo nome do grupo de carregamento.</span><span class="sxs-lookup"><span data-stu-id="83a09-111">The syntax for the entry is "Service:" followed by the service name or "Group:" followed by the load group name.</span></span>

<dt>

<span data-ttu-id="83a09-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83a09-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a09-113">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="83a09-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="83a09-114">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="83a09-114">**DisplayName**</span></span>
<span data-ttu-id="83a09-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a09-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a09-116">O nome amigável do serviço.</span><span class="sxs-lookup"><span data-stu-id="83a09-116">The friendly name of the service.</span></span>

<dt>

<span data-ttu-id="83a09-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83a09-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a09-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="83a09-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="83a09-119">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="83a09-119">**ErrorControl**</span></span>
<span data-ttu-id="83a09-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a09-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a09-121">A ação a ser executada se esse serviço falhar na inicialização.</span><span class="sxs-lookup"><span data-stu-id="83a09-121">The action to be performed if this service fails on startup.</span></span> <span data-ttu-id="83a09-122">Veja a seguir os valores válidos para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="83a09-122">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="83a09-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>erro de serviço do ADS \_ \_ \_ ignorar \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="83a09-123"><span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_IGNORE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="83a09-124">O programa de inicialização registra o erro, mas continua a operação de inicialização.</span><span class="sxs-lookup"><span data-stu-id="83a09-124">The startup program logs the error, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="83a09-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\_erro de serviço ADS \_ \_ normal \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="83a09-125"><span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_NORMAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="83a09-126">O programa de inicialização registra o erro e apresenta uma caixa de mensagem, mas continua a operação de inicialização.</span><span class="sxs-lookup"><span data-stu-id="83a09-126">The startup program logs the error and presents a message box, but continues the startup operation.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="83a09-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\_erro de serviço ADS \_ \_ grave \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="83a09-127"><span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_SEVERE\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="83a09-128">O programa de inicialização registra o erro.</span><span class="sxs-lookup"><span data-stu-id="83a09-128">The startup program logs the error.</span></span> <span data-ttu-id="83a09-129">Se a última configuração válida for iniciada, a operação de inicialização continuará.</span><span class="sxs-lookup"><span data-stu-id="83a09-129">If the last-known-good configuration is started, the startup operation continues.</span></span> <span data-ttu-id="83a09-130">Caso contrário, o sistema será reiniciado com a última configuração válida.</span><span class="sxs-lookup"><span data-stu-id="83a09-130">Otherwise, the system is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="83a09-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\_erro crítico do serviço ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="83a09-131"><span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\*\*\*\*ADS\_SERVICE\_ERROR\_CRITICAL\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="83a09-132">O programa de inicialização registra o erro, se possível.</span><span class="sxs-lookup"><span data-stu-id="83a09-132">The startup program logs the error, if possible.</span></span> <span data-ttu-id="83a09-133">Se a última configuração válida estiver sendo iniciada, a operação de inicialização falhará.</span><span class="sxs-lookup"><span data-stu-id="83a09-133">If the last-known-good configuration is being started, the startup operation fails.</span></span> <span data-ttu-id="83a09-134">Caso contrário, o sistema será reiniciado com a última configuração válida conhecida.</span><span class="sxs-lookup"><span data-stu-id="83a09-134">Otherwise, the system is restarted with the last-known good configuration.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="83a09-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83a09-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a09-136">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="83a09-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="83a09-137">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="83a09-137">**HostComputer**</span></span>
<span data-ttu-id="83a09-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a09-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a09-139">A cadeia de caracteres ADsPath do host deste serviço.</span><span class="sxs-lookup"><span data-stu-id="83a09-139">The ADsPath string of the host of this service.</span></span>

<dt>

<span data-ttu-id="83a09-140">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83a09-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a09-141">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="83a09-141">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="83a09-142">**LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="83a09-142">**LoadOrderGroup**</span></span>
<span data-ttu-id="83a09-143"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a09-143"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a09-144">Nome do grupo de ordem de carregamento do qual este serviço é membro.</span><span class="sxs-lookup"><span data-stu-id="83a09-144">Name of the load order group that this service is a member.</span></span>

<dt>

<span data-ttu-id="83a09-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83a09-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a09-146">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="83a09-146">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="83a09-147">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="83a09-147">**Path**</span></span>
<span data-ttu-id="83a09-148"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a09-148"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a09-149">Caminho e nome de arquivo para o executável deste serviço.</span><span class="sxs-lookup"><span data-stu-id="83a09-149">Path and filename to the executable of this service.</span></span>

<dt>

<span data-ttu-id="83a09-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83a09-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a09-151">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="83a09-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="83a09-152">**ServiceAccountName**</span><span class="sxs-lookup"><span data-stu-id="83a09-152">**ServiceAccountName**</span></span>
<span data-ttu-id="83a09-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a09-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a09-154">Nome da conta que esse serviço usa para se autenticar na inicialização.</span><span class="sxs-lookup"><span data-stu-id="83a09-154">Name of the account that this service uses to authenticate itself on startup.</span></span>

<dt>

<span data-ttu-id="83a09-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83a09-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a09-156">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="83a09-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="83a09-157">**ServiceAccountPath**</span><span class="sxs-lookup"><span data-stu-id="83a09-157">**ServiceAccountPath**</span></span>
<span data-ttu-id="83a09-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a09-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a09-159">Caminho da conta especificada pela propriedade **ServiceAccountPath** .</span><span class="sxs-lookup"><span data-stu-id="83a09-159">Path of the account specified by the **ServiceAccountPath** property.</span></span>

<dt>

<span data-ttu-id="83a09-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83a09-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a09-161">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="83a09-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="83a09-162">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="83a09-162">**ServiceType**</span></span>
<span data-ttu-id="83a09-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a09-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a09-164">A descrição de como um serviço se apresenta no computador host.</span><span class="sxs-lookup"><span data-stu-id="83a09-164">The description of how a service presents itself on the host computer.</span></span> <span data-ttu-id="83a09-165">Essa propriedade pode ser zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="83a09-165">This property can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="83a09-166">Driver de kernel de serviço do ADS \* \* \* \* \_ \_ \_ (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="83a09-166">\*\*\*\*ADS\_SERVICE\_KERNEL\_DRIVER\*\*\*\* (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="83a09-167">Driver do sistema de arquivos do serviço ADS \* \* \* \* \_ \_ \_ \_ (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="83a09-167">\*\*\*\*ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER\*\*\*\* (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="83a09-168">Processo próprio de serviço do ADS \* \* \* \* \_ \_ \_ (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="83a09-168">\*\*\*\*ADS\_SERVICE\_OWN\_PROCESS\*\*\*\* (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="83a09-169">\_Processo de \_ compartilhamento do serviço ADS \_ \* \* \* \* (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="83a09-169">\*\*\*\*ADS\_SERVICE\_SHARE\_PROCESS\*\*\*\* (0x00000020)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="83a09-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83a09-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a09-171">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="83a09-171">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="83a09-172">**StartType**</span><span class="sxs-lookup"><span data-stu-id="83a09-172">**StartType**</span></span>
<span data-ttu-id="83a09-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a09-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a09-174">Determina como iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="83a09-174">Determines how to start the service.</span></span> <span data-ttu-id="83a09-175">Veja a seguir os valores válidos para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="83a09-175">The following are valid values for this property.</span></span>

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="83a09-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\_início da inicialização do serviço ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="83a09-176"><span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>\*\*\*\*ADS\_SERVICE\_BOOT\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="83a09-177">O serviço é um driver de dispositivo iniciado pelo carregador do sistema.</span><span class="sxs-lookup"><span data-stu-id="83a09-177">The service is a device driver started by the system loader.</span></span> <span data-ttu-id="83a09-178">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="83a09-178">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="83a09-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\_início do sistema de serviço ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="83a09-179"><span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>\*\*\*\*ADS\_SERVICE\_SYSTEM\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="83a09-180">O serviço é um driver de dispositivo iniciado pela função **IoInitSystem** .</span><span class="sxs-lookup"><span data-stu-id="83a09-180">The service is a device driver started by the **IoInitSystem** function.</span></span> <span data-ttu-id="83a09-181">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="83a09-181">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="83a09-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\_início automático do serviço ADS \* \* \* \_ \_ \*</span><span class="sxs-lookup"><span data-stu-id="83a09-182"><span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>\*\*\*\*ADS\_SERVICE\_AUTO\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="83a09-183">O serviço será iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="83a09-183">The service will be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="83a09-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\_início da demanda de serviço ADS \_ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="83a09-184"><span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>\*\*\*\*ADS\_SERVICE\_DEMAND\_START\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="83a09-185">O serviço será iniciado pelo Gerenciador de controle de serviço quando um processo chamar a função [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) .</span><span class="sxs-lookup"><span data-stu-id="83a09-185">The service will be started by the service control manager when a process calls the [**StartService**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) function.</span></span>

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="83a09-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\_serviço ADS \_ desabilitado \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="83a09-186"><span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>\*\*\*\*ADS\_SERVICE\_DISABLED\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="83a09-187">Não é possível iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="83a09-187">The service cannot be started.</span></span> <span data-ttu-id="83a09-188">As tentativas de iniciar o serviço resultam no código de erro **serviço de erro \_ \_ desabilitado**.</span><span class="sxs-lookup"><span data-stu-id="83a09-188">Attempts to start the service result in the error code **ERROR\_SERVICE\_DISABLED**.</span></span>

</dd> </dl> <dt>

<span data-ttu-id="83a09-189">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83a09-189">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a09-190">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="83a09-190">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="83a09-191">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="83a09-191">**StartupParameters**</span></span>
<span data-ttu-id="83a09-192"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a09-192"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a09-193">Parâmetros passados para o serviço na inicialização.</span><span class="sxs-lookup"><span data-stu-id="83a09-193">Parameters passed to the service at startup.</span></span>

<dt>

<span data-ttu-id="83a09-194">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83a09-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a09-195">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="83a09-195">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="83a09-196">**Versão**</span><span class="sxs-lookup"><span data-stu-id="83a09-196">**Version**</span></span>
<span data-ttu-id="83a09-197"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="83a09-197"></dt> <dd> <dl></span></span>

<span data-ttu-id="83a09-198">Versão do serviço.</span><span class="sxs-lookup"><span data-stu-id="83a09-198">Version of the service.</span></span>

<dt>

<span data-ttu-id="83a09-199">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="83a09-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="83a09-200">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="83a09-200">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="83a09-201">Exemplos</span><span class="sxs-lookup"><span data-stu-id="83a09-201">Examples</span></span>

<span data-ttu-id="83a09-202">O exemplo de código a seguir mostra como listar todos os serviços do sistema disponíveis em execução no computador host, "mymachine", junto com o local para encontrar os executáveis dos serviços.</span><span class="sxs-lookup"><span data-stu-id="83a09-202">The following code example shows how to list all the available system services running on the host computer, "myMachine", together with the location to find the executables of the services.</span></span>


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a><span data-ttu-id="83a09-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83a09-203">Requirements</span></span>



| <span data-ttu-id="83a09-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="83a09-204">Requirement</span></span> | <span data-ttu-id="83a09-205">Valor</span><span class="sxs-lookup"><span data-stu-id="83a09-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83a09-206">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83a09-206">Minimum supported client</span></span><br/> | <span data-ttu-id="83a09-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83a09-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83a09-208">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83a09-208">Minimum supported server</span></span><br/> | <span data-ttu-id="83a09-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83a09-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83a09-210">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83a09-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="83a09-211"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="83a09-211"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="83a09-212">DLL</span><span class="sxs-lookup"><span data-stu-id="83a09-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83a09-213"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83a09-213"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="83a09-214">IID</span><span class="sxs-lookup"><span data-stu-id="83a09-214">IID</span></span><br/>                      | <span data-ttu-id="83a09-215">IID \_ IADsService é definido como 68AF66E0-31CA-11CF-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="83a09-215">IID\_IADsService is defined as 68AF66E0-31CA-11CF-A98A-00AA006BC149</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="83a09-216">Confira também</span><span class="sxs-lookup"><span data-stu-id="83a09-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a09-217">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="83a09-217">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="83a09-218">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="83a09-218">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 


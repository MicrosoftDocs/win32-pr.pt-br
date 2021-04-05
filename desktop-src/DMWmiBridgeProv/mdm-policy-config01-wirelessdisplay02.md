---
title: Classe MDM_Policy_Config01_WirelessDisplay02
description: A \_ classe MDM Policy \_ Config01 \_ WirelessDisplay02 representa as políticas de exibição sem fio disponíveis.
ms.assetid: 24b72ed9-cc14-4318-a9d1-597976083242
keywords:
- Classe MDM_Policy_Config01_WirelessDisplay02
- Classe MDM_Policy_Config01_WirelessDisplay02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WirelessDisplay02
- MDM_Policy_Config01_WirelessDisplay02.InstanceID
- MDM_Policy_Config01_WirelessDisplay02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b99183f8fdf599df8b5c1b4e82b9b536f47019
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918513"
---
# <a name="mdm_policy_config01_wirelessdisplay02-class"></a><span data-ttu-id="c357b-105">\_Classe MDM \_ Config01 \_ WirelessDisplay02</span><span class="sxs-lookup"><span data-stu-id="c357b-105">MDM\_Policy\_Config01\_WirelessDisplay02 class</span></span>

<span data-ttu-id="c357b-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="c357b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c357b-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="c357b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c357b-108">A classe **MDM \_ Policy \_ Config01 \_ WirelessDisplay02** representa as políticas de exibição sem fio disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c357b-108">The **MDM\_Policy\_Config01\_WirelessDisplay02** class represents the wireless display policies available.</span></span>

<span data-ttu-id="c357b-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c357b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c357b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c357b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WirelessDisplay02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMdnsDiscovery;
  sint32 AllowMdnsAdvertisement;
  sint32 AllowProjectionFromPCOverInfrastructure;
  sint32 AllowProjectionFromPC;
  sint32 AllowProjectionToPC;
  sint32 AllowProjectionToPCOverInfrastructure;
  sint32 AllowUserInputFromWirelessDisplayReceiver;
  sint32 RequirePinForPairing;
};
```

## <a name="members"></a><span data-ttu-id="c357b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="c357b-111">Members</span></span>

<span data-ttu-id="c357b-112">A **classe \_ \_ Config01 \_ WirelessDisplay02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c357b-112">The **MDM\_Policy\_Config01\_WirelessDisplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="c357b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c357b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c357b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c357b-114">Properties</span></span>

<span data-ttu-id="c357b-115">A **classe \_ \_ Config01 \_ WirelessDisplay02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c357b-115">The **MDM\_Policy\_Config01\_WirelessDisplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c357b-116">AllowMdnsAdvertisement</span><span class="sxs-lookup"><span data-stu-id="c357b-116">AllowMdnsAdvertisement</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsadvertisement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c357b-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c357b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c357b-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c357b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c357b-119">AllowMdnsDiscovery</span><span class="sxs-lookup"><span data-stu-id="c357b-119">AllowMdnsDiscovery</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsdiscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c357b-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c357b-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c357b-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c357b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c357b-122">AllowProjectionFromPC</span><span class="sxs-lookup"><span data-stu-id="c357b-122">AllowProjectionFromPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c357b-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c357b-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c357b-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c357b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c357b-125">AllowProjectionFromPCOverInfrastructure</span><span class="sxs-lookup"><span data-stu-id="c357b-125">AllowProjectionFromPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c357b-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c357b-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c357b-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c357b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c357b-128">AllowProjectionToPC</span><span class="sxs-lookup"><span data-stu-id="c357b-128">AllowProjectionToPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c357b-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c357b-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c357b-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c357b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c357b-131">AllowProjectionToPCOverInfrastructure</span><span class="sxs-lookup"><span data-stu-id="c357b-131">AllowProjectionToPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c357b-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c357b-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c357b-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c357b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c357b-134">AllowUserInputFromWirelessDisplayReceiver</span><span class="sxs-lookup"><span data-stu-id="c357b-134">AllowUserInputFromWirelessDisplayReceiver</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowuserinputfromwirelessdisplayreceiver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c357b-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c357b-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c357b-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c357b-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c357b-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c357b-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c357b-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c357b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c357b-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c357b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c357b-140">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c357b-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c357b-141">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="c357b-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="c357b-142">Para essa classe, a cadeia de caracteres é "WirelessDisplay".</span><span class="sxs-lookup"><span data-stu-id="c357b-142">For this class, the string is "WirelessDisplay".</span></span>

</dd> <dt>

<span data-ttu-id="c357b-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c357b-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c357b-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c357b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c357b-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c357b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c357b-146">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c357b-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c357b-147">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="c357b-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="c357b-148">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="c357b-148">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="c357b-149">RequirePinForPairing</span><span class="sxs-lookup"><span data-stu-id="c357b-149">RequirePinForPairing</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-requirepinforpairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c357b-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c357b-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c357b-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c357b-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c357b-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c357b-152">Requirements</span></span>



| <span data-ttu-id="c357b-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="c357b-153">Requirement</span></span> | <span data-ttu-id="c357b-154">Valor</span><span class="sxs-lookup"><span data-stu-id="c357b-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c357b-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c357b-155">Minimum supported client</span></span><br/> | <span data-ttu-id="c357b-156">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c357b-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c357b-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c357b-157">Minimum supported server</span></span><br/> | <span data-ttu-id="c357b-158">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c357b-158">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="c357b-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="c357b-159">Namespace</span></span><br/>                | <span data-ttu-id="c357b-160">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c357b-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="c357b-161">MOF</span><span class="sxs-lookup"><span data-stu-id="c357b-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c357b-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c357b-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="c357b-163">DLL</span><span class="sxs-lookup"><span data-stu-id="c357b-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c357b-164"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="c357b-164"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 


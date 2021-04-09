---
title: Classe MDM_Policy_Result01_WirelessDisplay02
description: A \_ classe MDM Policy \_ Result01 \_ WirelessDisplay02 representa as políticas de exibição sem fio disponíveis.
ms.assetid: fbdfa785-8747-47b4-9802-da1c245ca222
keywords:
- Classe MDM_Policy_Result01_WirelessDisplay02
- Classe MDM_Policy_Result01_WirelessDisplay02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WirelessDisplay02
- MDM_Policy_Result01_WirelessDisplay02.InstanceID
- MDM_Policy_Result01_WirelessDisplay02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90f4e309d1c54f12d99dfbeaa0b80807249e61fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008909"
---
# <a name="mdm_policy_result01_wirelessdisplay02-class"></a><span data-ttu-id="edac3-105">\_Classe MDM \_ Result01 \_ WirelessDisplay02</span><span class="sxs-lookup"><span data-stu-id="edac3-105">MDM\_Policy\_Result01\_WirelessDisplay02 class</span></span>

<span data-ttu-id="edac3-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="edac3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="edac3-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="edac3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="edac3-108">A classe **MDM \_ Policy \_ Result01 \_ WirelessDisplay02** representa as políticas de exibição sem fio disponíveis.</span><span class="sxs-lookup"><span data-stu-id="edac3-108">The **MDM\_Policy\_Result01\_WirelessDisplay02** class represents the wireless display policies available.</span></span>

<span data-ttu-id="edac3-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="edac3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="edac3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edac3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WirelessDisplay02
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

## <a name="members"></a><span data-ttu-id="edac3-111">Membros</span><span class="sxs-lookup"><span data-stu-id="edac3-111">Members</span></span>

<span data-ttu-id="edac3-112">A **classe \_ \_ Result01 \_ WirelessDisplay02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="edac3-112">The **MDM\_Policy\_Result01\_WirelessDisplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="edac3-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="edac3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="edac3-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="edac3-114">Properties</span></span>

<span data-ttu-id="edac3-115">A **classe \_ \_ Result01 \_ WirelessDisplay02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="edac3-115">The **MDM\_Policy\_Result01\_WirelessDisplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="edac3-116">AllowMdnsAdvertisement</span><span class="sxs-lookup"><span data-stu-id="edac3-116">AllowMdnsAdvertisement</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsadvertisement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edac3-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="edac3-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edac3-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="edac3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edac3-119">AllowMdnsDiscovery</span><span class="sxs-lookup"><span data-stu-id="edac3-119">AllowMdnsDiscovery</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsdiscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edac3-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="edac3-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edac3-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="edac3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edac3-122">AllowProjectionFromPC</span><span class="sxs-lookup"><span data-stu-id="edac3-122">AllowProjectionFromPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edac3-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="edac3-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edac3-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="edac3-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edac3-125">AllowProjectionFromPCOverInfrastructure</span><span class="sxs-lookup"><span data-stu-id="edac3-125">AllowProjectionFromPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edac3-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="edac3-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edac3-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="edac3-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edac3-128">AllowProjectionToPC</span><span class="sxs-lookup"><span data-stu-id="edac3-128">AllowProjectionToPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edac3-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="edac3-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edac3-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="edac3-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edac3-131">AllowProjectionToPCOverInfrastructure</span><span class="sxs-lookup"><span data-stu-id="edac3-131">AllowProjectionToPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edac3-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="edac3-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edac3-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="edac3-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="edac3-134">AllowUserInputFromWirelessDisplayReceiver</span><span class="sxs-lookup"><span data-stu-id="edac3-134">AllowUserInputFromWirelessDisplayReceiver</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowuserinputfromwirelessdisplayreceiver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edac3-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="edac3-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edac3-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="edac3-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="edac3-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="edac3-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edac3-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="edac3-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="edac3-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="edac3-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="edac3-140">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="edac3-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="edac3-141">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="edac3-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="edac3-142">Para essa classe, a cadeia de caracteres é "WirelessDisplay".</span><span class="sxs-lookup"><span data-stu-id="edac3-142">For this class, the string is "WirelessDisplay".</span></span>

</dd> <dt>

<span data-ttu-id="edac3-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="edac3-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edac3-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="edac3-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="edac3-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="edac3-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="edac3-146">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="edac3-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="edac3-147">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="edac3-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="edac3-148">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="edac3-148">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="edac3-149">RequirePinForPairing</span><span class="sxs-lookup"><span data-stu-id="edac3-149">RequirePinForPairing</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-requirepinforpairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="edac3-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="edac3-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="edac3-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="edac3-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="edac3-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edac3-152">Requirements</span></span>



| <span data-ttu-id="edac3-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="edac3-153">Requirement</span></span> | <span data-ttu-id="edac3-154">Valor</span><span class="sxs-lookup"><span data-stu-id="edac3-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edac3-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edac3-155">Minimum supported client</span></span><br/> | <span data-ttu-id="edac3-156">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="edac3-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="edac3-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edac3-157">Minimum supported server</span></span><br/> | <span data-ttu-id="edac3-158">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="edac3-158">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="edac3-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="edac3-159">Namespace</span></span><br/>                | <span data-ttu-id="edac3-160">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="edac3-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="edac3-161">MOF</span><span class="sxs-lookup"><span data-stu-id="edac3-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edac3-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="edac3-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="edac3-163">DLL</span><span class="sxs-lookup"><span data-stu-id="edac3-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edac3-164"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="edac3-164"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 


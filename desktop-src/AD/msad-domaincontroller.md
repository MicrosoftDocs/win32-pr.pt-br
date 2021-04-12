---
title: Classe MSAD_DomainController
description: Representa o controlador de domínio (DC) no qual o provedor WMI está em execução.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- Classe de MSAD_DomainController Active Directory
- Active Directory de MSAD_DomainController classe, descrita
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455190"
---
# <a name="msad_domaincontroller-class"></a><span data-ttu-id="844d5-105">\_Classe DOMAINCONTROLLER MSAD</span><span class="sxs-lookup"><span data-stu-id="844d5-105">MSAD\_DomainController class</span></span>

<span data-ttu-id="844d5-106">Representa o controlador de domínio (DC) no qual o provedor WMI está em execução.</span><span class="sxs-lookup"><span data-stu-id="844d5-106">Represents the domain controller (DC) on which the WMI provider is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="844d5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="844d5-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="844d5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="844d5-108">Members</span></span>

<span data-ttu-id="844d5-109">A **classe \_ DomainController MSAD** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="844d5-109">The **MSAD\_DomainController** class has these types of members:</span></span>

-   [<span data-ttu-id="844d5-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="844d5-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="844d5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="844d5-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="844d5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="844d5-112">Methods</span></span>

<span data-ttu-id="844d5-113">A **classe \_ DomainController MSAD** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="844d5-113">The **MSAD\_DomainController** class has these methods.</span></span>



| <span data-ttu-id="844d5-114">Método</span><span class="sxs-lookup"><span data-stu-id="844d5-114">Method</span></span>                                                 | <span data-ttu-id="844d5-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="844d5-115">Description</span></span>                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="844d5-116">**ExecuteKCC**</span><span class="sxs-lookup"><span data-stu-id="844d5-116">**ExecuteKCC**</span></span>](executekcc-msad-domaincontroller.md) | <span data-ttu-id="844d5-117">Invoca o Knowledge Consistency Checker para verificar a topologia de replicação.</span><span class="sxs-lookup"><span data-stu-id="844d5-117">Invokes the Knowledge Consistency Checker to verify the replication topology.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="844d5-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="844d5-118">Properties</span></span>

<span data-ttu-id="844d5-119">A **classe \_ DomainController MSAD** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="844d5-119">The **MSAD\_DomainController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="844d5-120">**CommonName**</span><span class="sxs-lookup"><span data-stu-id="844d5-120">**CommonName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="844d5-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-123">Obtém o nome comum do objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="844d5-123">Gets the common name of the server object.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-124">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="844d5-124">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="844d5-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="844d5-127">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="844d5-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="844d5-128">Obtém o caminho X. 500 do objeto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) .</span><span class="sxs-lookup"><span data-stu-id="844d5-128">Gets the X.500 path of the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-129">**IsAdvertisingToLocator**</span><span class="sxs-lookup"><span data-stu-id="844d5-129">**IsAdvertisingToLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-130">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="844d5-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-132">Obtém o valor que indica se o serviço localizador no controlador de domínio está anunciando corretamente.</span><span class="sxs-lookup"><span data-stu-id="844d5-132">Gets the value that indicates whether the locator service on the DC is advertising correctly.</span></span> <span data-ttu-id="844d5-133">**True** se o serviço localizador no controlador de domínio estiver anunciando corretamente; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="844d5-133">**TRUE** if the locator service on the DC is advertising correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-134">**IsGC**</span><span class="sxs-lookup"><span data-stu-id="844d5-134">**IsGC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-135">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="844d5-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-137">Obtém o valor que indica se o DC é um servidor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="844d5-137">Gets the value that indicates whether the DC is a Global Catalog server.</span></span> <span data-ttu-id="844d5-138">**True** se o DC for um servidor de catálogo global; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="844d5-138">**TRUE** if the DC is a Global Catalog server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-139">**IsNextRIDPoolAvailable**</span><span class="sxs-lookup"><span data-stu-id="844d5-139">**IsNextRIDPoolAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-140">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="844d5-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-142">Obtém o valor que indica se o controlador de domínio obteve outro pool de RIDs.</span><span class="sxs-lookup"><span data-stu-id="844d5-142">Gets the value that indicates whether the DC has obtained another RID pool.</span></span> <span data-ttu-id="844d5-143">**True** se o controlador de domínio tiver obtido outro pool de RID e a alocação de RIDs nesse controlador de domínio poderá continuar mesmo se o pool atual de RIDs for esgotado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="844d5-143">**TRUE** if the DC has obtained another RID pool and allocation of RIDs on this DC can continue even if the current pool of RIDs is exhausted; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-144">**IsRegisteredInDNS**</span><span class="sxs-lookup"><span data-stu-id="844d5-144">**IsRegisteredInDNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-145">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="844d5-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-147">Obtém o valor que indica se o DC está registrado corretamente no DNS.</span><span class="sxs-lookup"><span data-stu-id="844d5-147">Gets the value that indicates whether the DC is registered correctly in DNS.</span></span> <span data-ttu-id="844d5-148">**True** se o controlador de domínio estiver registrado corretamente no DNS; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="844d5-148">**TRUE** if the DC is registered correctly in DNS; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-149">**IsSysVolReady**</span><span class="sxs-lookup"><span data-stu-id="844d5-149">**IsSysVolReady**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-150">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="844d5-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-152">Obtém o valor que indica se o SysVol foi publicado corretamente.</span><span class="sxs-lookup"><span data-stu-id="844d5-152">Gets the value that indicates whether the SysVol has published correctly.</span></span> <span data-ttu-id="844d5-153">**True** se o SYSVOL tiver sido publicado corretamente; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="844d5-153">**TRUE** if the SysVol has published correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-154">**NTDsaGUID**</span><span class="sxs-lookup"><span data-stu-id="844d5-154">**NTDsaGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="844d5-155">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-157">Obtém o GUID que está associado ao objeto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) no contêiner de configuração.</span><span class="sxs-lookup"><span data-stu-id="844d5-157">Gets the GUID that is associated with the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object in the configuration container.</span></span> <span data-ttu-id="844d5-158">O objeto **NTDS-DSA** representa o domínio do Active Directory processo DSA do serviço no servidor.</span><span class="sxs-lookup"><span data-stu-id="844d5-158">The **NTDS-DSA** object represents the Active Directory Domain Service DSA process on the server.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-159">**PercentOfRIDsLeft**</span><span class="sxs-lookup"><span data-stu-id="844d5-159">**PercentOfRIDsLeft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-160">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="844d5-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-162">Obtém a porcentagem de RIDs que são deixados no pool RID atual neste controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="844d5-162">Gets the percentage of RIDs that are left in the current RID pool on this DC.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-163">**SiteName**</span><span class="sxs-lookup"><span data-stu-id="844d5-163">**SiteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="844d5-164">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-166">Obtém o site no qual o DC existe.</span><span class="sxs-lookup"><span data-stu-id="844d5-166">Gets the site in which the DC exists.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-167">**TimeOfOldestReplAdd**</span><span class="sxs-lookup"><span data-stu-id="844d5-167">**TimeOfOldestReplAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-168">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="844d5-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-170">Obtém o carimbo de data/hora da operação de adição de replicação mais antiga que ainda está na fila neste controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="844d5-170">Gets the timestamp of the oldest replication add operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-171">**TimeOfOldestReplDel**</span><span class="sxs-lookup"><span data-stu-id="844d5-171">**TimeOfOldestReplDel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-172">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="844d5-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-174">Obtém o carimbo de data/hora da operação de exclusão de replicação mais antiga que ainda está na fila neste controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="844d5-174">Gets the timestamp of the oldest replication delete operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-175">**TimeOfOldestReplMod**</span><span class="sxs-lookup"><span data-stu-id="844d5-175">**TimeOfOldestReplMod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-176">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="844d5-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-178">Obtém o carimbo de data/hora da operação de modificação de replicação mais antiga que ainda está na fila neste controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="844d5-178">Gets the timestamp of the oldest replication modify operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-179">**TimeOfOldestReplSync**</span><span class="sxs-lookup"><span data-stu-id="844d5-179">**TimeOfOldestReplSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-180">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="844d5-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-182">Obtém o carimbo de data/hora da operação de sincronização de replicação mais antiga que ainda está na fila neste controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="844d5-182">Gets the timestamp of the oldest replication sync operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="844d5-183">**TimeOfOldestReplUpdRefs**</span><span class="sxs-lookup"><span data-stu-id="844d5-183">**TimeOfOldestReplUpdRefs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844d5-184">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="844d5-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="844d5-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="844d5-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844d5-186">Obtém o carimbo de data/hora da operação de atualização de replicação mais antiga que ainda está na fila neste controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="844d5-186">Gets the timestamp of the oldest replication update operation that is still in the queue on this domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="844d5-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="844d5-187">Requirements</span></span>



| <span data-ttu-id="844d5-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="844d5-188">Requirement</span></span> | <span data-ttu-id="844d5-189">Valor</span><span class="sxs-lookup"><span data-stu-id="844d5-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="844d5-190">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="844d5-190">Minimum supported client</span></span><br/> | <span data-ttu-id="844d5-191">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="844d5-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="844d5-192">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="844d5-192">Minimum supported server</span></span><br/> | <span data-ttu-id="844d5-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="844d5-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="844d5-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="844d5-194">Namespace</span></span><br/>                | <span data-ttu-id="844d5-195">\\MicrosoftActiveDirectory raiz</span><span class="sxs-lookup"><span data-stu-id="844d5-195">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="844d5-196">MOF</span><span class="sxs-lookup"><span data-stu-id="844d5-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="844d5-197"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="844d5-197"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="844d5-198">DLL</span><span class="sxs-lookup"><span data-stu-id="844d5-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="844d5-199"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="844d5-199"><dt>Replprov.dll</dt></span></span> </dl> |



 


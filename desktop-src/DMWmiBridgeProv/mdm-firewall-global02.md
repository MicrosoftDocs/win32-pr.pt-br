---
title: Classe MDM_Firewall_Global02
description: A \_ classe Global02 do MDM firewall \_ é usada para definir as configurações do Windows Defender firewall.
ms.assetid: 387a60c6-6dc9-4710-a1e3-0468ac004395
keywords:
- Classe MDM_Firewall_Global02
- Classe MDM_Firewall_Global02, descrita
topic_type:
- apiref
api_name:
- MDM_Firewall_Global02
- MDM_Firewall_Global02.InstanceID
- MDM_Firewall_Global02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cef2a8b11585848ac10035528db176b78d2e66b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163588"
---
# <a name="mdm_firewall_global02-class"></a><span data-ttu-id="7285a-105">\_ \_ Classe GLOBAL02 do MDM firewall</span><span class="sxs-lookup"><span data-stu-id="7285a-105">MDM\_Firewall\_Global02 class</span></span>

<span data-ttu-id="7285a-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="7285a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7285a-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="7285a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7285a-108">A \_ classe Global02 do MDM firewall \_ é usada para definir as configurações do Windows Defender firewall.</span><span class="sxs-lookup"><span data-stu-id="7285a-108">The MDM\_Firewall\_Global02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="7285a-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7285a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7285a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7285a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Global02
{
  string  InstanceID;
  string  ParentID;
  sint32  PolicyVersionSupported;
  sint32  CurrentProfiles;
  boolean DisableStatefulFtp;
  sint32  SaIdleTime;
  sint32  PresharedKeyEncoding;
  sint32  IPsecExempt;
  sint32  CRLcheck;
  string  PolicyVersion;
  string  BinaryVersionSupported;
  boolean OpportunisticallyMatchAuthSetPerKM;
  sint32  EnablePacketQueue;
};
```

## <a name="members"></a><span data-ttu-id="7285a-111">Membros</span><span class="sxs-lookup"><span data-stu-id="7285a-111">Members</span></span>

<span data-ttu-id="7285a-112">A **classe \_ \_ Global02 do MDM firewall** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7285a-112">The **MDM\_Firewall\_Global02** class has these types of members:</span></span>

-   [<span data-ttu-id="7285a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7285a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7285a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7285a-114">Properties</span></span>

<span data-ttu-id="7285a-115">A **classe \_ \_ Global02 do MDM firewall** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7285a-115">The **MDM\_Firewall\_Global02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7285a-116">BinaryVersionSupported</span><span class="sxs-lookup"><span data-stu-id="7285a-116">BinaryVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#binaryversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7285a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7285a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7285a-119">CRLcheck</span><span class="sxs-lookup"><span data-stu-id="7285a-119">CRLcheck</span></span>](/windows/client-management/mdm/firewall-csp#crlcheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7285a-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7285a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7285a-122">CurrentProfiles</span><span class="sxs-lookup"><span data-stu-id="7285a-122">CurrentProfiles</span></span>](/windows/client-management/mdm/firewall-csp#currentprofiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7285a-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7285a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7285a-125">DisableStatefulFtp</span><span class="sxs-lookup"><span data-stu-id="7285a-125">DisableStatefulFtp</span></span>](/windows/client-management/mdm/firewall-csp#disablestatefulftp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-126">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7285a-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7285a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7285a-128">EnablePacketQueue</span><span class="sxs-lookup"><span data-stu-id="7285a-128">EnablePacketQueue</span></span>](/windows/client-management/mdm/firewall-csp#enablepacketqueue)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7285a-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7285a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7285a-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7285a-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7285a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7285a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7285a-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7285a-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7285a-135">IPsecExempt</span><span class="sxs-lookup"><span data-stu-id="7285a-135">IPsecExempt</span></span>](/windows/client-management/mdm/firewall-csp#ipsecexempt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-136">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7285a-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7285a-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7285a-138">OpportunisticallyMatchAuthSetPerKM</span><span class="sxs-lookup"><span data-stu-id="7285a-138">OpportunisticallyMatchAuthSetPerKM</span></span>](/windows/client-management/mdm/firewall-csp#opportunisticallymatchauthsetperkm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-139">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7285a-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-140">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7285a-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7285a-141">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7285a-141">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7285a-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7285a-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7285a-144">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7285a-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7285a-145">PolicyVersion</span><span class="sxs-lookup"><span data-stu-id="7285a-145">PolicyVersion</span></span>](/windows/client-management/mdm/firewall-csp#policyversion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7285a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-147">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7285a-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7285a-148">PolicyVersionSupported</span><span class="sxs-lookup"><span data-stu-id="7285a-148">PolicyVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#policyversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-149">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7285a-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7285a-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7285a-151">PresharedKeyEncoding</span><span class="sxs-lookup"><span data-stu-id="7285a-151">PresharedKeyEncoding</span></span>](/windows/client-management/mdm/firewall-csp#presharedkeyencoding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-152">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7285a-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7285a-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7285a-154">SaIdleTime</span><span class="sxs-lookup"><span data-stu-id="7285a-154">SaIdleTime</span></span>](/windows/client-management/mdm/firewall-csp#saidletime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7285a-155">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7285a-155">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7285a-156">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7285a-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7285a-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7285a-157">Requirements</span></span>



| <span data-ttu-id="7285a-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="7285a-158">Requirement</span></span> | <span data-ttu-id="7285a-159">Valor</span><span class="sxs-lookup"><span data-stu-id="7285a-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7285a-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7285a-160">Minimum supported client</span></span><br/> | <span data-ttu-id="7285a-161">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7285a-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7285a-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7285a-162">Minimum supported server</span></span><br/> | <span data-ttu-id="7285a-163">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7285a-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="7285a-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="7285a-164">Namespace</span></span><br/>                | <span data-ttu-id="7285a-165">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="7285a-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="7285a-166">MOF</span><span class="sxs-lookup"><span data-stu-id="7285a-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7285a-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7285a-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="7285a-168">DLL</span><span class="sxs-lookup"><span data-stu-id="7285a-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7285a-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7285a-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 


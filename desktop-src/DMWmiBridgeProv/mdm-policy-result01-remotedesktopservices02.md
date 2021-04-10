---
title: Classe MDM_Policy_Result01_RemoteDesktopServices02
description: A \_ classe MDM Policy \_ Result01 \_ RemoteDesktopServices02 representa as políticas de serviços de área de trabalho remota.
ms.assetid: 015fe30d-2b76-4df5-a81f-65e488db3526
keywords:
- Classe MDM_Policy_Result01_RemoteDesktopServices02
- Classe MDM_Policy_Result01_RemoteDesktopServices02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteDesktopServices02
- MDM_Policy_Result01_RemoteDesktopServices02.InstanceID
- MDM_Policy_Result01_RemoteDesktopServices02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0488308a557f1b872de299bda12487287e1081c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918024"
---
# <a name="mdm_policy_result01_remotedesktopservices02-class"></a><span data-ttu-id="01e13-105">\_Classe MDM \_ Result01 \_ RemoteDesktopServices02</span><span class="sxs-lookup"><span data-stu-id="01e13-105">MDM\_Policy\_Result01\_RemoteDesktopServices02 class</span></span>

<span data-ttu-id="01e13-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="01e13-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="01e13-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="01e13-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="01e13-108">A \_ classe MDM Policy \_ Result01 \_ RemoteDesktopServices02 representa as políticas de serviços de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="01e13-108">The MDM\_Policy\_Result01\_RemoteDesktopServices02 class represents the remote desktop services policies.</span></span>

<span data-ttu-id="01e13-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="01e13-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="01e13-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01e13-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteDesktopServices02
{
  string InstanceID;
  string ParentID;
  string AllowUsersToConnectRemotely;
  string ClientConnectionEncryptionLevel;
  string DoNotAllowDriveRedirection;
  string DoNotAllowPasswordSaving;
  string PromptForPasswordUponConnection;
  string RequireSecureRPCCommunication;
};
```

## <a name="members"></a><span data-ttu-id="01e13-111">Membros</span><span class="sxs-lookup"><span data-stu-id="01e13-111">Members</span></span>

<span data-ttu-id="01e13-112">A **classe \_ \_ Result01 \_ RemoteDesktopServices02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="01e13-112">The **MDM\_Policy\_Result01\_RemoteDesktopServices02** class has these types of members:</span></span>

-   [<span data-ttu-id="01e13-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01e13-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01e13-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01e13-114">Properties</span></span>

<span data-ttu-id="01e13-115">A **classe \_ \_ Result01 \_ RemoteDesktopServices02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="01e13-115">The **MDM\_Policy\_Result01\_RemoteDesktopServices02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="01e13-116">AllowUsersToConnectRemotely</span><span class="sxs-lookup"><span data-stu-id="01e13-116">AllowUsersToConnectRemotely</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-allowuserstoconnectremotely)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e13-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e13-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e13-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="01e13-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01e13-119">ClientConnectionEncryptionLevel</span><span class="sxs-lookup"><span data-stu-id="01e13-119">ClientConnectionEncryptionLevel</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-clientconnectionencryptionlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e13-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e13-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e13-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="01e13-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01e13-122">DoNotAllowDriveRedirection</span><span class="sxs-lookup"><span data-stu-id="01e13-122">DoNotAllowDriveRedirection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowdriveredirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e13-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e13-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e13-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="01e13-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01e13-125">DoNotAllowPasswordSaving</span><span class="sxs-lookup"><span data-stu-id="01e13-125">DoNotAllowPasswordSaving</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowpasswordsaving)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e13-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e13-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e13-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="01e13-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="01e13-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="01e13-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e13-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e13-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e13-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e13-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e13-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01e13-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="01e13-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="01e13-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e13-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e13-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e13-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e13-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e13-135">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="01e13-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01e13-136">PromptForPasswordUponConnection</span><span class="sxs-lookup"><span data-stu-id="01e13-136">PromptForPasswordUponConnection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-promptforpassworduponconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e13-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e13-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e13-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="01e13-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="01e13-139">RequireSecureRPCCommunication</span><span class="sxs-lookup"><span data-stu-id="01e13-139">RequireSecureRPCCommunication</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-requiresecurerpccommunication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e13-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e13-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e13-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="01e13-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01e13-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01e13-142">Requirements</span></span>



| <span data-ttu-id="01e13-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="01e13-143">Requirement</span></span> | <span data-ttu-id="01e13-144">Valor</span><span class="sxs-lookup"><span data-stu-id="01e13-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01e13-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01e13-145">Minimum supported client</span></span><br/> | <span data-ttu-id="01e13-146">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="01e13-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01e13-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01e13-147">Minimum supported server</span></span><br/> | <span data-ttu-id="01e13-148">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="01e13-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="01e13-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="01e13-149">Namespace</span></span><br/>                | <span data-ttu-id="01e13-150">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="01e13-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="01e13-151">MOF</span><span class="sxs-lookup"><span data-stu-id="01e13-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01e13-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01e13-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="01e13-153">DLL</span><span class="sxs-lookup"><span data-stu-id="01e13-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01e13-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01e13-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 


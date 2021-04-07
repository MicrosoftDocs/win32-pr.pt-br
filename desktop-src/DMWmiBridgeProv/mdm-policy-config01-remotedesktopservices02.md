---
title: Classe MDM_Policy_Config01_RemoteDesktopServices02
description: A \_ classe Config01 RemoteDesktopServices02 de política de MDM \_ \_ configura as políticas de serviço da área de trabalho remota.
ms.assetid: d2c53be7-6dec-4603-b851-e9c979475496
keywords:
- Classe MDM_Policy_Config01_RemoteDesktopServices02
- Classe MDM_Policy_Config01_RemoteDesktopServices02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteDesktopServices02
- MDM_Policy_Config01_RemoteDesktopServices02.InstanceID
- MDM_Policy_Config01_RemoteDesktopServices02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a023ae44c7b8ab170d4efe9c38aaacdeca3cc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918427"
---
# <a name="mdm_policy_config01_remotedesktopservices02-class"></a><span data-ttu-id="2c1d1-105">\_Classe MDM \_ Config01 \_ RemoteDesktopServices02</span><span class="sxs-lookup"><span data-stu-id="2c1d1-105">MDM\_Policy\_Config01\_RemoteDesktopServices02 class</span></span>

<span data-ttu-id="2c1d1-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="2c1d1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2c1d1-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="2c1d1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2c1d1-108">A \_ classe Config01 RemoteDesktopServices02 de política de MDM \_ \_ configura as políticas de serviço da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="2c1d1-108">The MDM\_Policy\_Config01\_RemoteDesktopServices02 class configures the remote desktop service policies.</span></span>

<span data-ttu-id="2c1d1-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2c1d1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c1d1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c1d1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteDesktopServices02
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

## <a name="members"></a><span data-ttu-id="2c1d1-111">Membros</span><span class="sxs-lookup"><span data-stu-id="2c1d1-111">Members</span></span>

<span data-ttu-id="2c1d1-112">A **classe \_ \_ Config01 \_ RemoteDesktopServices02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2c1d1-112">The **MDM\_Policy\_Config01\_RemoteDesktopServices02** class has these types of members:</span></span>

-   [<span data-ttu-id="2c1d1-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2c1d1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c1d1-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2c1d1-114">Properties</span></span>

<span data-ttu-id="2c1d1-115">A **classe \_ \_ Config01 \_ RemoteDesktopServices02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2c1d1-115">The **MDM\_Policy\_Config01\_RemoteDesktopServices02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2c1d1-116">AllowUsersToConnectRemotely</span><span class="sxs-lookup"><span data-stu-id="2c1d1-116">AllowUsersToConnectRemotely</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-allowuserstoconnectremotely)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c1d1-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c1d1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c1d1-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2c1d1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c1d1-119">ClientConnectionEncryptionLevel</span><span class="sxs-lookup"><span data-stu-id="2c1d1-119">ClientConnectionEncryptionLevel</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-clientconnectionencryptionlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c1d1-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c1d1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c1d1-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2c1d1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c1d1-122">DoNotAllowDriveRedirection</span><span class="sxs-lookup"><span data-stu-id="2c1d1-122">DoNotAllowDriveRedirection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowdriveredirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c1d1-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c1d1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c1d1-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2c1d1-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c1d1-125">DoNotAllowPasswordSaving</span><span class="sxs-lookup"><span data-stu-id="2c1d1-125">DoNotAllowPasswordSaving</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowpasswordsaving)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c1d1-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c1d1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c1d1-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2c1d1-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2c1d1-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2c1d1-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c1d1-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c1d1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c1d1-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c1d1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c1d1-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2c1d1-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2c1d1-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2c1d1-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c1d1-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c1d1-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c1d1-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2c1d1-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c1d1-135">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2c1d1-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c1d1-136">PromptForPasswordUponConnection</span><span class="sxs-lookup"><span data-stu-id="2c1d1-136">PromptForPasswordUponConnection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-promptforpassworduponconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c1d1-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c1d1-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c1d1-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2c1d1-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2c1d1-139">RequireSecureRPCCommunication</span><span class="sxs-lookup"><span data-stu-id="2c1d1-139">RequireSecureRPCCommunication</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-requiresecurerpccommunication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c1d1-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2c1d1-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c1d1-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2c1d1-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c1d1-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c1d1-142">Requirements</span></span>



| <span data-ttu-id="2c1d1-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c1d1-143">Requirement</span></span> | <span data-ttu-id="2c1d1-144">Valor</span><span class="sxs-lookup"><span data-stu-id="2c1d1-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c1d1-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c1d1-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2c1d1-146">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2c1d1-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c1d1-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c1d1-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2c1d1-148">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2c1d1-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2c1d1-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c1d1-149">Namespace</span></span><br/>                | <span data-ttu-id="2c1d1-150">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="2c1d1-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2c1d1-151">MOF</span><span class="sxs-lookup"><span data-stu-id="2c1d1-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c1d1-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c1d1-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c1d1-153">DLL</span><span class="sxs-lookup"><span data-stu-id="2c1d1-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c1d1-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c1d1-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 


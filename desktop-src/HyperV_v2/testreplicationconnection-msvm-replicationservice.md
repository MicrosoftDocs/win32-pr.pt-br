---
description: Verifica se a replicação pode ser habilitada do sistema de host atual para o sistema de recuperação especificado.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Método TestReplicationConnection da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6644ead653509d879e779928030ff8912a124ad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768498"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="4ebb6-103">Método TestReplicationConnection da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="4ebb6-103">TestReplicationConnection method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="4ebb6-104">Verifica se a replicação pode ser habilitada do sistema de host atual para o sistema de recuperação especificado.</span><span class="sxs-lookup"><span data-stu-id="4ebb6-104">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ebb6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ebb6-105">Syntax</span></span>


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4ebb6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ebb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ebb6-107">*RecoveryConnectionPoint* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebb6-107">*RecoveryConnectionPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebb6-108">O nome do ponto de conexão.</span><span class="sxs-lookup"><span data-stu-id="4ebb6-108">The name of the connection point.</span></span> <span data-ttu-id="4ebb6-109">Para um cluster de recuperação, esse é o nome da extremidade do agente.</span><span class="sxs-lookup"><span data-stu-id="4ebb6-109">For a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="4ebb6-110">Para um servidor de recuperação autônomo, esse é o nome do sistema do host.</span><span class="sxs-lookup"><span data-stu-id="4ebb6-110">For a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="4ebb6-111">*RecoveryServerPortNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebb6-111">*RecoveryServerPortNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebb6-112">O número da porta do ponto de conexão de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4ebb6-112">The recovery connection point port number.</span></span>

</dd> <dt>

<span data-ttu-id="4ebb6-113">*AuthenticationType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebb6-113">*AuthenticationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebb6-114">O esquema de autenticação de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4ebb6-114">The recovery authentication scheme.</span></span> <span data-ttu-id="4ebb6-115">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ebb6-115">This must be one of the following values.</span></span>

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span data-ttu-id="4ebb6-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Autenticação integrada** (1)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Integrated authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4ebb6-117">Autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="4ebb6-117">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="4ebb6-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticação baseada em certificado** (2)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4ebb6-119">Autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="4ebb6-119">Certificate based authentication.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4ebb6-120">*CertificateThumbPrint* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebb6-120">*CertificateThumbPrint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebb6-121">Impressão digital do certificado a ser usada quando o parâmetro *AuthenticationType* for autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="4ebb6-121">Certificate thumbprint to use when the *AuthenticationType* parameter is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="4ebb6-122">*BypassProxyServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ebb6-122">*BypassProxyServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebb6-123">Ignore o servidor proxy ao se conectar ao servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="4ebb6-123">Bypass the proxy server when connecting to the replica server.</span></span>

</dd> <dt>

<span data-ttu-id="4ebb6-124">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="4ebb6-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ebb6-125">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4ebb6-125">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ebb6-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ebb6-126">Return value</span></span>

<span data-ttu-id="4ebb6-127">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ebb6-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4ebb6-128">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-129">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-130">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-131">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-132">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-133">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-134">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-135">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-136">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-137">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-138">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-139">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-140">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="4ebb6-141">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="4ebb6-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4ebb6-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ebb6-142">Requirements</span></span>



| <span data-ttu-id="4ebb6-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ebb6-143">Requirement</span></span> | <span data-ttu-id="4ebb6-144">Valor</span><span class="sxs-lookup"><span data-stu-id="4ebb6-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ebb6-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ebb6-145">Minimum supported client</span></span><br/> | <span data-ttu-id="4ebb6-146">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4ebb6-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4ebb6-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ebb6-147">Minimum supported server</span></span><br/> | <span data-ttu-id="4ebb6-148">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4ebb6-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ebb6-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ebb6-149">Namespace</span></span><br/>                | <span data-ttu-id="4ebb6-150">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4ebb6-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4ebb6-151">MOF</span><span class="sxs-lookup"><span data-stu-id="4ebb6-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ebb6-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ebb6-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ebb6-153">DLL</span><span class="sxs-lookup"><span data-stu-id="4ebb6-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ebb6-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ebb6-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ebb6-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ebb6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ebb6-156">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="4ebb6-156">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 


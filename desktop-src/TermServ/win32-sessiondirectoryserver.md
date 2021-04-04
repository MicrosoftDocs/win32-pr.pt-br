---
title: Classe Win32_SessionDirectoryServer
description: Fornece propriedades para exibir as propriedades de um servidor do Conexão de Área de Trabalho Remota Broker (agente de conexão RD).
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionDirectoryServer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionDirectoryServer classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9e96efb19e4db56e582cd44d05f3e9865e5282c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918306"
---
# <a name="win32_sessiondirectoryserver-class"></a><span data-ttu-id="788a9-105">\_Classe Win32 SessionDirectoryServer</span><span class="sxs-lookup"><span data-stu-id="788a9-105">Win32\_SessionDirectoryServer class</span></span>

<span data-ttu-id="788a9-106">Fornece propriedades para exibir as propriedades de um servidor do Conexão de Área de Trabalho Remota Broker (agente de conexão RD).</span><span class="sxs-lookup"><span data-stu-id="788a9-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) server.</span></span>

> [!Note]  
> <span data-ttu-id="788a9-107">No Windows Server 2008 R2, o nome do agente de sessão dos serviços de terminal (agente de Sessão TS) foi alterado para o agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="788a9-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="788a9-108">Essas propriedades se aplicam a todos os sistemas operacionais com suporte, salvo indicação em contrário.</span><span class="sxs-lookup"><span data-stu-id="788a9-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="788a9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="788a9-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a><span data-ttu-id="788a9-110">Membros</span><span class="sxs-lookup"><span data-stu-id="788a9-110">Members</span></span>

<span data-ttu-id="788a9-111">A classe **Win32 \_ SessionDirectoryServer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="788a9-111">The **Win32\_SessionDirectoryServer** class has these types of members:</span></span>

-   [<span data-ttu-id="788a9-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="788a9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="788a9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="788a9-113">Properties</span></span>

<span data-ttu-id="788a9-114">A classe **Win32 \_ SessionDirectoryServer** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="788a9-114">The **Win32\_SessionDirectoryServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="788a9-115">**ClusterName**</span><span class="sxs-lookup"><span data-stu-id="788a9-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="788a9-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="788a9-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="788a9-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="788a9-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="788a9-118">Nome do farm que inclui o servidor.</span><span class="sxs-lookup"><span data-stu-id="788a9-118">Name of the farm that includes the server.</span></span>

</dd> <dt>

<span data-ttu-id="788a9-119">**Indicador**</span><span class="sxs-lookup"><span data-stu-id="788a9-119">**LoadIndicator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="788a9-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="788a9-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="788a9-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="788a9-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="788a9-122">Um número relativo que representa a carga do Host da Sessão RD Server quando o algoritmo de balanceamento de carga padrão é usado.</span><span class="sxs-lookup"><span data-stu-id="788a9-122">A relative number that represents the RD Session Host server load when the default load-balancing algorithm is used.</span></span> <span data-ttu-id="788a9-123">O valor da propriedade *loadindicator* é baseado no número de sessões, no número de solicitações de redirecionamento pendentes e no valor de peso do servidor.</span><span class="sxs-lookup"><span data-stu-id="788a9-123">The *LoadIndicator* property value is based on the number of sessions, the number of pending redirection requests, and the server weight value.</span></span>

</dd> <dt>

<span data-ttu-id="788a9-124">**NumberOfSessions**</span><span class="sxs-lookup"><span data-stu-id="788a9-124">**NumberOfSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="788a9-125">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="788a9-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="788a9-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="788a9-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="788a9-127">Número de sessões no servidor do agente de conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="788a9-127">Number of sessions in the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="788a9-128">**NumPendRedir**</span><span class="sxs-lookup"><span data-stu-id="788a9-128">**NumPendRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="788a9-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="788a9-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="788a9-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="788a9-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="788a9-131">Número de solicitações de redirecionamento pendentes.</span><span class="sxs-lookup"><span data-stu-id="788a9-131">Number of pending redirection requests.</span></span>

</dd> <dt>

<span data-ttu-id="788a9-132">**ServerIPAddress**</span><span class="sxs-lookup"><span data-stu-id="788a9-132">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="788a9-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="788a9-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="788a9-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="788a9-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="788a9-135">Endereço IP do servidor do agente de conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="788a9-135">IP address of the RD Connection Broker server.</span></span> <span data-ttu-id="788a9-136">Se o servidor estiver configurado para endereços IPv4 e IPv6, ele conterá o endereço IPv4.</span><span class="sxs-lookup"><span data-stu-id="788a9-136">If the server is configured for both IPv4 and IPv6 addresses, this will contain the IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="788a9-137">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="788a9-137">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="788a9-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="788a9-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="788a9-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="788a9-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="788a9-140">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="788a9-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="788a9-141">Nome do servidor do agente de conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="788a9-141">Name of the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="788a9-142">**ServerWeight**</span><span class="sxs-lookup"><span data-stu-id="788a9-142">**ServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="788a9-143">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="788a9-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="788a9-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="788a9-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="788a9-145">Valor de peso do servidor, usado no balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="788a9-145">Server weight value, used in load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="788a9-146">**SingleSessionMode**</span><span class="sxs-lookup"><span data-stu-id="788a9-146">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="788a9-147">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="788a9-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="788a9-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="788a9-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="788a9-149">Configuração de modo de sessão única do servidor do agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="788a9-149">Single session mode setting of the RD Connection Broker server.</span></span>

<dt>

<span data-ttu-id="788a9-150">0</span><span class="sxs-lookup"><span data-stu-id="788a9-150">0</span></span>
</dt> <dd>

<span data-ttu-id="788a9-151">O farm não está no modo de sessão única.</span><span class="sxs-lookup"><span data-stu-id="788a9-151">The farm is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="788a9-152">1</span><span class="sxs-lookup"><span data-stu-id="788a9-152">1</span></span>
</dt> <dd>

<span data-ttu-id="788a9-153">O farm no está em modo de sessão única.</span><span class="sxs-lookup"><span data-stu-id="788a9-153">The farm in is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="788a9-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="788a9-154">Remarks</span></span>

<span data-ttu-id="788a9-155">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="788a9-155">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="788a9-156">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="788a9-156">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="788a9-157">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="788a9-157">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="788a9-158">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="788a9-158">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="788a9-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="788a9-159">Requirements</span></span>



| <span data-ttu-id="788a9-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="788a9-160">Requirement</span></span> | <span data-ttu-id="788a9-161">Valor</span><span class="sxs-lookup"><span data-stu-id="788a9-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="788a9-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="788a9-162">Minimum supported client</span></span><br/> | <span data-ttu-id="788a9-163">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="788a9-163">None supported</span></span><br/>                                                              |
| <span data-ttu-id="788a9-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="788a9-164">Minimum supported server</span></span><br/> | <span data-ttu-id="788a9-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="788a9-165">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="788a9-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="788a9-166">Namespace</span></span><br/>                | <span data-ttu-id="788a9-167">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="788a9-167">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="788a9-168">MOF</span><span class="sxs-lookup"><span data-stu-id="788a9-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="788a9-169"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="788a9-169"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="788a9-170">DLL</span><span class="sxs-lookup"><span data-stu-id="788a9-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="788a9-171"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="788a9-171"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="788a9-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="788a9-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="788a9-173">**\_SessionDirectoryCluster Win32**</span><span class="sxs-lookup"><span data-stu-id="788a9-173">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="788a9-174">**\_SessionDirectorySession Win32**</span><span class="sxs-lookup"><span data-stu-id="788a9-174">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 


---
title: Classe Win32_SessionDirectorySession
description: Fornece propriedades para exibir as propriedades de uma sessão do agente de Conexão de Área de Trabalho Remota (agente de conexão RD).
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionDirectorySession Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionDirectorySession classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba8fdbdffc764c3bdcc1a8f5bc53aa479f318d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369361"
---
# <a name="win32_sessiondirectorysession-class"></a><span data-ttu-id="74769-105">\_Classe Win32 SessionDirectorySession</span><span class="sxs-lookup"><span data-stu-id="74769-105">Win32\_SessionDirectorySession class</span></span>

<span data-ttu-id="74769-106">Fornece propriedades para exibir as propriedades de uma sessão do agente de Conexão de Área de Trabalho Remota (agente de conexão RD).</span><span class="sxs-lookup"><span data-stu-id="74769-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) session.</span></span>

> [!Note]  
> <span data-ttu-id="74769-107">No Windows Server 2008 R2, o nome do agente de sessão dos serviços de terminal (agente de Sessão TS) foi alterado para o agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="74769-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="74769-108">Essas propriedades se aplicam a todos os sistemas operacionais com suporte, salvo indicação em contrário.</span><span class="sxs-lookup"><span data-stu-id="74769-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="74769-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74769-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a><span data-ttu-id="74769-110">Membros</span><span class="sxs-lookup"><span data-stu-id="74769-110">Members</span></span>

<span data-ttu-id="74769-111">A classe **Win32 \_ SessionDirectorySession** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="74769-111">The **Win32\_SessionDirectorySession** class has these types of members:</span></span>

-   [<span data-ttu-id="74769-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="74769-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74769-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="74769-113">Properties</span></span>

<span data-ttu-id="74769-114">A classe **Win32 \_ SessionDirectorySession** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="74769-114">The **Win32\_SessionDirectorySession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74769-115">**ApplicationType**</span><span class="sxs-lookup"><span data-stu-id="74769-115">**ApplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="74769-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74769-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74769-118">Aplicativo iniciado com esta sessão.</span><span class="sxs-lookup"><span data-stu-id="74769-118">Application started with this session.</span></span> <span data-ttu-id="74769-119">Isso é o mesmo que a propriedade **StartProgram** de [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="74769-119">This is the same as the **StartProgram** property of [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="74769-120">**ColorDepth**</span><span class="sxs-lookup"><span data-stu-id="74769-120">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-121">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74769-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74769-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74769-123">Profundidade de cor da sessão, medida em bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="74769-123">Color depth of the session, measured in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="74769-124">**CreateTime**</span><span class="sxs-lookup"><span data-stu-id="74769-124">**CreateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-125">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74769-125">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="74769-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74769-127">Data e hora em que a sessão foi criada.</span><span class="sxs-lookup"><span data-stu-id="74769-127">Date and time the session was created.</span></span> <span data-ttu-id="74769-128">Esse valor não é redefinido quando uma sessão é desconectada e reconectada.</span><span class="sxs-lookup"><span data-stu-id="74769-128">This value is not reset when a session is disconnected and reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="74769-129">**Desconectartime**</span><span class="sxs-lookup"><span data-stu-id="74769-129">**DisconnectTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-130">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74769-130">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="74769-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74769-132">Data e hora em que a sessão foi desconectada (se aplicável).</span><span class="sxs-lookup"><span data-stu-id="74769-132">Date and time the session was disconnected (if applicable).</span></span>

</dd> <dt>

<span data-ttu-id="74769-133">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="74769-133">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="74769-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74769-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74769-136">Nome de domínio do usuário conectado a esta sessão.</span><span class="sxs-lookup"><span data-stu-id="74769-136">Domain name of the user logged on to this session.</span></span>

</dd> <dt>

<span data-ttu-id="74769-137">**ResolutionHeight**</span><span class="sxs-lookup"><span data-stu-id="74769-137">**ResolutionHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-138">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74769-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74769-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74769-140">Altura da sessão, em pixels, para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="74769-140">Height of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="74769-141">**ResolutionWidth**</span><span class="sxs-lookup"><span data-stu-id="74769-141">**ResolutionWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74769-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74769-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74769-144">Largura da sessão, em pixels, para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="74769-144">Width of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="74769-145">**ServerIPAddress**</span><span class="sxs-lookup"><span data-stu-id="74769-145">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="74769-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74769-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74769-148">Endereço IP do servidor do agente de conexão RD para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="74769-148">IP address of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="74769-149">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="74769-149">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="74769-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74769-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74769-152">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="74769-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="74769-153">Nome do servidor do agente de conexão RD para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="74769-153">Name of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="74769-154">**SessionID**</span><span class="sxs-lookup"><span data-stu-id="74769-154">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-155">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74769-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74769-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74769-157">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="74769-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="74769-158">ID da sessão para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="74769-158">Session ID for this session.</span></span>

</dd> <dt>

<span data-ttu-id="74769-159">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="74769-159">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-160">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74769-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74769-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74769-162">Estado desta sessão.</span><span class="sxs-lookup"><span data-stu-id="74769-162">State of this session.</span></span>

<dt>

<span data-ttu-id="74769-163">0</span><span class="sxs-lookup"><span data-stu-id="74769-163">0</span></span>
</dt> <dd>

<span data-ttu-id="74769-164">A sessão está ativa.</span><span class="sxs-lookup"><span data-stu-id="74769-164">The session is active.</span></span>

</dd> <dt>

<span data-ttu-id="74769-165">1</span><span class="sxs-lookup"><span data-stu-id="74769-165">1</span></span>
</dt> <dd>

<span data-ttu-id="74769-166">A sessão está desconectada.</span><span class="sxs-lookup"><span data-stu-id="74769-166">The session is disconnected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74769-167">**TSProtocol**</span><span class="sxs-lookup"><span data-stu-id="74769-167">**TSProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-168">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74769-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74769-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74769-170">Protocolo para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="74769-170">Protocol for this session.</span></span>

<dt>

<span data-ttu-id="74769-171">0</span><span class="sxs-lookup"><span data-stu-id="74769-171">0</span></span>
</dt> <dd>

<span data-ttu-id="74769-172">Esta sessão está em execução em um console físico.</span><span class="sxs-lookup"><span data-stu-id="74769-172">This session is running on a physical console.</span></span>

</dd> <dt>

<span data-ttu-id="74769-173">1</span><span class="sxs-lookup"><span data-stu-id="74769-173">1</span></span>
</dt> <dd>

<span data-ttu-id="74769-174">Um protocolo de terceiros proprietário é usado para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="74769-174">A proprietary third-party protocol is used for this session.</span></span>

</dd> <dt>

<span data-ttu-id="74769-175">2</span><span class="sxs-lookup"><span data-stu-id="74769-175">2</span></span>
</dt> <dd>

<span data-ttu-id="74769-176">Protocolo RDP (RDP) é usado para esta sessão.</span><span class="sxs-lookup"><span data-stu-id="74769-176">Remote Desktop Protocol (RDP) is used for this session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74769-177">**UserName**</span><span class="sxs-lookup"><span data-stu-id="74769-177">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74769-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="74769-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74769-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74769-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74769-180">Nome de usuário do usuário conectado a esta sessão.</span><span class="sxs-lookup"><span data-stu-id="74769-180">User name of the user logged on to this session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74769-181">Comentários</span><span class="sxs-lookup"><span data-stu-id="74769-181">Remarks</span></span>

<span data-ttu-id="74769-182">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="74769-182">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="74769-183">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="74769-183">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="74769-184">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="74769-184">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="74769-185">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="74769-185">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="74769-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74769-186">Requirements</span></span>



| <span data-ttu-id="74769-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="74769-187">Requirement</span></span> | <span data-ttu-id="74769-188">Valor</span><span class="sxs-lookup"><span data-stu-id="74769-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74769-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74769-189">Minimum supported client</span></span><br/> | <span data-ttu-id="74769-190">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="74769-190">None supported</span></span><br/>                                                              |
| <span data-ttu-id="74769-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74769-191">Minimum supported server</span></span><br/> | <span data-ttu-id="74769-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74769-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="74769-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="74769-193">Namespace</span></span><br/>                | <span data-ttu-id="74769-194">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="74769-194">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="74769-195">MOF</span><span class="sxs-lookup"><span data-stu-id="74769-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74769-196"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74769-196"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="74769-197">DLL</span><span class="sxs-lookup"><span data-stu-id="74769-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74769-198"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74769-198"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74769-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="74769-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74769-200">**\_SessionDirectoryCluster Win32**</span><span class="sxs-lookup"><span data-stu-id="74769-200">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="74769-201">**\_SessionDirectoryServer Win32**</span><span class="sxs-lookup"><span data-stu-id="74769-201">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> </dl>

 


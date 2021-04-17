---
title: Rastreamento de eventos no ADSI
description: O Windows Server 2008 e o Windows Vista apresentam o rastreamento de eventos em ADSI (Active Directory Service Interfaces).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- ADSI de rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f43c0d840cd1f3f70d293a0a4f5c299fd129efe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105755904"
---
# <a name="event-tracing-in-adsi"></a><span data-ttu-id="b2a49-104">Rastreamento de eventos no ADSI</span><span class="sxs-lookup"><span data-stu-id="b2a49-104">Event Tracing in ADSI</span></span>

<span data-ttu-id="b2a49-105">O Windows Server 2008 e o Windows Vista apresentam o [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) em ADSI ( [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) ).</span><span class="sxs-lookup"><span data-stu-id="b2a49-105">Windows Server 2008 and Windows Vista introduce [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="b2a49-106">Determinadas áreas do provedor de LDAP ADSI têm uma implementação subjacente que é complexa ou que envolve uma sequência de etapas que dificulta o diagnóstico de problemas.</span><span class="sxs-lookup"><span data-stu-id="b2a49-106">Certain areas of the ADSI LDAP Provider have an underlying implementation that is complex or that involves a sequence of steps that makes it difficult to diagnose problems.</span></span> <span data-ttu-id="b2a49-107">Para ajudar os desenvolvedores de aplicativos a solucionar problemas, o rastreamento de eventos foi adicionado às seguintes áreas:</span><span class="sxs-lookup"><span data-stu-id="b2a49-107">To help application developers troubleshoot, Event Tracing has been added to the following areas:</span></span>

## <a name="schema-parsing-and-downloading"></a><span data-ttu-id="b2a49-108">Análise e download de esquema</span><span class="sxs-lookup"><span data-stu-id="b2a49-108">Schema Parsing and Downloading</span></span>

<span data-ttu-id="b2a49-109">A interface IADs na ADSI requer que o esquema LDAP seja armazenado em cache no cliente para que os atributos possam ser empacotados corretamente (conforme descrito no [modelo de esquema ADSI](adsi-schema-model.md)).</span><span class="sxs-lookup"><span data-stu-id="b2a49-109">The IADs interface in ADSI requires that the LDAP schema be cached on the client so that attributes can be marshaled correctly (as described in the [ADSI Schema Model](adsi-schema-model.md)).</span></span> <span data-ttu-id="b2a49-110">Para fazer isso, a ADSI carrega o esquema para cada processo (e para cada servidor/domínio LDAP) na memória a partir de um arquivo de esquema (. SCH) que é salvo no disco local ou baixando-o do servidor LDAP.</span><span class="sxs-lookup"><span data-stu-id="b2a49-110">To achieve this, ADSI loads the schema for each process (and for each LDAP server/domain) into memory either from a schema (.sch) file that is saved on the local disk or by downloading it from the LDAP server.</span></span> <span data-ttu-id="b2a49-111">Processos diferentes na mesma máquina cliente usam o esquema em cache em disco se ele estiver disponível e aplicável.</span><span class="sxs-lookup"><span data-stu-id="b2a49-111">Different processes on the same client machine use the cached schema on disk if it is available and applicable.</span></span>

<span data-ttu-id="b2a49-112">Se o esquema não puder ser obtido do disco ou do servidor, a ADSI usará um esquema padrão codificado.</span><span class="sxs-lookup"><span data-stu-id="b2a49-112">If the schema cannot be obtained from the disk or the server, ADSI uses a hardcoded default schema.</span></span> <span data-ttu-id="b2a49-113">Quando isso ocorre, os atributos que não fazem parte desse esquema padrão não podem ser empacotados e a ADSI retorna um erro ao recuperar esses atributos.</span><span class="sxs-lookup"><span data-stu-id="b2a49-113">When this occurs, attributes that are not part of this default schema cannot be marshaled and ADSI returns an error while retrieving these attributes.</span></span> <span data-ttu-id="b2a49-114">Vários fatores podem fazer com que isso aconteça, incluindo problemas na análise do esquema e privilégios insuficientes para baixar o esquema.</span><span class="sxs-lookup"><span data-stu-id="b2a49-114">A number of factors could cause this to happen, including problems in parsing the schema, and insufficient privileges to download the schema.</span></span> <span data-ttu-id="b2a49-115">Geralmente, é difícil determinar por que um determinado esquema padrão está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="b2a49-115">It is often difficult to determine why a certain default schema is being used.</span></span> <span data-ttu-id="b2a49-116">Usar o rastreamento de eventos nessa área ajudará a diagnosticar o problema mais rapidamente e corrigi-lo.</span><span class="sxs-lookup"><span data-stu-id="b2a49-116">Using Event Tracing in this area will help to more quickly diagnose the problem and fix it.</span></span>

## <a name="changing-and-setting-the-password"></a><span data-ttu-id="b2a49-117">Alterando e definindo a senha</span><span class="sxs-lookup"><span data-stu-id="b2a49-117">Changing and Setting the Password</span></span>

<span data-ttu-id="b2a49-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) e [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) empregam mais de um mecanismo para executar a operação solicitada com base na configuração disponível (conforme descrito em [definindo e alterando senhas de usuário com o provedor LDAP](setting-user-passwords-for-ldap-providers.md)).</span><span class="sxs-lookup"><span data-stu-id="b2a49-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) and [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) employ more than one mechanism to perform the requested operation based on the available configuration (as described in [Setting and Changing User Passwords with the LDAP Provider](setting-user-passwords-for-ldap-providers.md)).</span></span> <span data-ttu-id="b2a49-119">Quando **ChangePassword** e **SetPassword** falham, pode ser difícil determinar exatamente o porquê, e o rastreamento de eventos ajudará a solucionar problemas com esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b2a49-119">When **ChangePassword** and **SetPassword** fail, it can be difficult to determine exactly why, and Event Tracing will help to troubleshoot problems with these methods.</span></span>

## <a name="adsi-bind-cache"></a><span data-ttu-id="b2a49-120">Cache de associação ADSI</span><span class="sxs-lookup"><span data-stu-id="b2a49-120">ADSI Bind Cache</span></span>

<span data-ttu-id="b2a49-121">O ADSI tenta, internamente, reutilizar conexões LDAP sempre que possível (consulte [cache de conexão](connection-caching.md)).</span><span class="sxs-lookup"><span data-stu-id="b2a49-121">ADSI internally tries to reuse LDAP connections whenever possible (see [Connection Caching](connection-caching.md)).</span></span> <span data-ttu-id="b2a49-122">Ao solucionar problemas, é útil rastrear se uma nova conexão foi aberta para comunicação com o servidor ou se uma conexão existente foi usada.</span><span class="sxs-lookup"><span data-stu-id="b2a49-122">When troubleshooting, it is useful to trace whether a new connection was opened for communication with the server or whether an existing connection was used.</span></span> <span data-ttu-id="b2a49-123">Também pode ser útil rastrear o ciclo de vida do cache de conexão (às vezes chamado de cache de associação) e sua criação ou fechamento e se uma indicação de conexão ocorreu.</span><span class="sxs-lookup"><span data-stu-id="b2a49-123">It can also be useful to trace the lifecycle of the connection cache (sometimes referred to as the bind cache) and its creation or closure, and whether a connection referral took place.</span></span> <span data-ttu-id="b2a49-124">No caso de uma [ligação sem servidor](/windows/desktop/AD/serverless-binding-and-rootdse), a ADSI chama o localizador de DC para selecionar um servidor para o domínio do contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="b2a49-124">In the case of a [serverless bind](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI calls the DC locator to select a server for the domain of the user's context.</span></span> <span data-ttu-id="b2a49-125">Em seguida, o ADSI mantém um cache do mapeamento do servidor de domínio para conexões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b2a49-125">ADSI then maintains a cache of the domain-server mapping for subsequent connections.</span></span> <span data-ttu-id="b2a49-126">O rastreamento de eventos ajuda a rastrear a seleção do controlador de domínio e, portanto, é útil para solucionar problemas relacionados à conexão.</span><span class="sxs-lookup"><span data-stu-id="b2a49-126">Event Tracing helps to trace the selection of the DC, and is therefore helpful in troubleshooting connection-related issues.</span></span>

## <a name="enabling-tracing-and-starting-a-tracing-session"></a><span data-ttu-id="b2a49-127">Habilitando o rastreamento e iniciando uma sessão de rastreamento</span><span class="sxs-lookup"><span data-stu-id="b2a49-127">Enabling Tracing and Starting a Tracing Session</span></span>

<span data-ttu-id="b2a49-128">Para ativar o rastreamento ADSI, crie a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="b2a49-128">To turn on ADSI tracing, create the following registry key:</span></span>

<span data-ttu-id="b2a49-129">**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** de \\  \\ **rastreamento** ADSI \\ ***ProcessName***</span><span class="sxs-lookup"><span data-stu-id="b2a49-129">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\***ProcessName***</span></span>

<span data-ttu-id="b2a49-130">*ProcessName* é o nome completo do processo que você deseja rastrear, incluindo sua extensão (por exemplo, "Svchost.exe").</span><span class="sxs-lookup"><span data-stu-id="b2a49-130">*ProcessName* is the full name of the process that you want to trace, including its extension (for example, "Svchost.exe").</span></span> <span data-ttu-id="b2a49-131">Além disso, você pode inserir um valor opcional do tipo **DWORD** chamado PID nesta chave.</span><span class="sxs-lookup"><span data-stu-id="b2a49-131">In addition, you can place an optional value of type **DWORD** named PID in this key.</span></span> <span data-ttu-id="b2a49-132">É altamente recomendável que você defina esse valor e, portanto, rastreie apenas um processo específico.</span><span class="sxs-lookup"><span data-stu-id="b2a49-132">It is highly recommended that you set this value and thereby trace only a particular process.</span></span> <span data-ttu-id="b2a49-133">Caso contrário, todas as instâncias do aplicativo especificado por *ProcessName* serão rastreadas.</span><span class="sxs-lookup"><span data-stu-id="b2a49-133">Otherwise, all instances of the application specified by *ProcessName* will be traced.</span></span>

<span data-ttu-id="b2a49-134">Em seguida, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="b2a49-134">Then execute the following command:</span></span>

<span data-ttu-id="b2a49-135">**tracelog.exe-Start** *SessionName*  \* *-GUID \# \* \* \* \_ GUID do provedor* **-f** *filename* **-Flag** *sinalizadores* **de nível de**  arquivo</span><span class="sxs-lookup"><span data-stu-id="b2a49-135">**tracelog.exe -start** *sessionname* \**-guid \#\*\*\*provider\_guid* **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span></span>

<span data-ttu-id="b2a49-136">*SessionName* é simplesmente um identificador arbitrário que é usado para rotular a sessão de rastreamento (você precisará se referir a esse nome de sessão posteriormente ao parar a sessão de rastreamento).</span><span class="sxs-lookup"><span data-stu-id="b2a49-136">*sessionname* is simply an arbitrary identifier that is used to label the tracing session (you will need to refer to this session name later when you stop the tracing session).</span></span> <span data-ttu-id="b2a49-137">O GUID do provedor de controle ADSI é "7288c9f8-D63C-4932-a345-89d6b060174d".</span><span class="sxs-lookup"><span data-stu-id="b2a49-137">The GUID for the ADSI tracking provider is "7288c9f8-d63c-4932-a345-89d6b060174d".</span></span> <span data-ttu-id="b2a49-138">*filename* especifica o arquivo de log no qual os eventos serão gravados.</span><span class="sxs-lookup"><span data-stu-id="b2a49-138">*filename* specifies the logfile to which events will be written.</span></span> <span data-ttu-id="b2a49-139">*sinalizadores* deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b2a49-139">*traceFlags* should be one of the following values:</span></span>



|                                 |                       |
|---------------------------------|-----------------------|
| <span data-ttu-id="b2a49-140">**esquema de depuração \_**</span><span class="sxs-lookup"><span data-stu-id="b2a49-140">**DEBUG\_SCHEMA**</span></span><br/>    | <span data-ttu-id="b2a49-141">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b2a49-141">0x00000001</span></span><br/> |
| <span data-ttu-id="b2a49-142">**Depurar \_ CHANGEPWD**</span><span class="sxs-lookup"><span data-stu-id="b2a49-142">**DEBUG\_CHANGEPWD**</span></span><br/> | <span data-ttu-id="b2a49-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b2a49-143">0x00000002</span></span><br/> |
| <span data-ttu-id="b2a49-144">**Depurar \_ SETPWD**</span><span class="sxs-lookup"><span data-stu-id="b2a49-144">**DEBUG\_SETPWD**</span></span><br/>    | <span data-ttu-id="b2a49-145">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b2a49-145">0x00000004</span></span><br/> |
| <span data-ttu-id="b2a49-146">**Depurar \_ BINDCACHE**</span><span class="sxs-lookup"><span data-stu-id="b2a49-146">**DEBUG\_BINDCACHE**</span></span><br/> | <span data-ttu-id="b2a49-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b2a49-147">0x00000008</span></span><br/> |



 

<span data-ttu-id="b2a49-148">Esses sinalizadores determinam quais métodos [ADSI](active-directory-service-interfaces-adsi.md) serão rastreados, de acordo com a tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="b2a49-148">These flags determine which [ADSI](active-directory-service-interfaces-adsi.md) methods will be traced, according to the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2a49-149"><strong>DEBUG_SCHEMA</strong></span><span class="sxs-lookup"><span data-stu-id="b2a49-149"><strong>DEBUG_SCHEMA</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="b2a49-150">LdapGetSchema</span><span class="sxs-lookup"><span data-stu-id="b2a49-150">LdapGetSchema</span></span></li>
<li><span data-ttu-id="b2a49-151">GetSchemaInfoTime</span><span class="sxs-lookup"><span data-stu-id="b2a49-151">GetSchemaInfoTime</span></span></li>
<li><span data-ttu-id="b2a49-152">LdapReadSchemaInfoFromServer</span><span class="sxs-lookup"><span data-stu-id="b2a49-152">LdapReadSchemaInfoFromServer</span></span></li>
<li><span data-ttu-id="b2a49-153">ProcessSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="b2a49-153">ProcessSchemaInfo</span></span></li>
<li><span data-ttu-id="b2a49-154">HelperReadLdapSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="b2a49-154">HelperReadLdapSchemaInfo</span></span></li>
<li><span data-ttu-id="b2a49-155">ProcessClassInfoArray</span><span class="sxs-lookup"><span data-stu-id="b2a49-155">ProcessClassInfoArray</span></span></li>
<li><span data-ttu-id="b2a49-156">ReadSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="b2a49-156">ReadSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="b2a49-157">StoreSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="b2a49-157">StoreSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="b2a49-158">AttributeTypeDescription</span><span class="sxs-lookup"><span data-stu-id="b2a49-158">AttributeTypeDescription</span></span></li>
<li><span data-ttu-id="b2a49-159">ObjectClassDescription</span><span class="sxs-lookup"><span data-stu-id="b2a49-159">ObjectClassDescription</span></span></li>
<li><span data-ttu-id="b2a49-160">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="b2a49-160">DITContentRuleDescription</span></span></li>
<li><span data-ttu-id="b2a49-161">Directorystring</span><span class="sxs-lookup"><span data-stu-id="b2a49-161">DirectoryString</span></span></li>
<li><span data-ttu-id="b2a49-162">DirectoryStrings</span><span class="sxs-lookup"><span data-stu-id="b2a49-162">DirectoryStrings</span></span></li>
<li><span data-ttu-id="b2a49-163">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="b2a49-163">DITContentRuleDescription</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2a49-164"><strong>DEBUG_CHANGEPWD</strong></span><span class="sxs-lookup"><span data-stu-id="b2a49-164"><strong>DEBUG_CHANGEPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="b2a49-165">CADsUser:: ChangePassword</span><span class="sxs-lookup"><span data-stu-id="b2a49-165">CADsUser::ChangePassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2a49-166"><strong>DEBUG_SETPWD</strong></span><span class="sxs-lookup"><span data-stu-id="b2a49-166"><strong>DEBUG_SETPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="b2a49-167">CADsUser:: SetPassword</span><span class="sxs-lookup"><span data-stu-id="b2a49-167">CADsUser::SetPassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2a49-168"><strong>DEBUG_BINDCACHE</strong></span><span class="sxs-lookup"><span data-stu-id="b2a49-168"><strong>DEBUG_BINDCACHE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="b2a49-169">GetServerBasedObject</span><span class="sxs-lookup"><span data-stu-id="b2a49-169">GetServerBasedObject</span></span></li>
<li><span data-ttu-id="b2a49-170">GetServerLessBasedObject</span><span class="sxs-lookup"><span data-stu-id="b2a49-170">GetServerLessBasedObject</span></span></li>
<li><span data-ttu-id="b2a49-171">GetGCDomainName</span><span class="sxs-lookup"><span data-stu-id="b2a49-171">GetGCDomainName</span></span></li>
<li><span data-ttu-id="b2a49-172">GetDefaultDomainName</span><span class="sxs-lookup"><span data-stu-id="b2a49-172">GetDefaultDomainName</span></span></li>
<li><span data-ttu-id="b2a49-173">GetUserDomainFlatName</span><span class="sxs-lookup"><span data-stu-id="b2a49-173">GetUserDomainFlatName</span></span></li>
<li><span data-ttu-id="b2a49-174">BindCacheLookup</span><span class="sxs-lookup"><span data-stu-id="b2a49-174">BindCacheLookup</span></span></li>
<li><span data-ttu-id="b2a49-175">EquivalentPortNumbers</span><span class="sxs-lookup"><span data-stu-id="b2a49-175">EquivalentPortNumbers</span></span></li>
<li><span data-ttu-id="b2a49-176">CanCredentialsBeReused</span><span class="sxs-lookup"><span data-stu-id="b2a49-176">CanCredentialsBeReused</span></span></li>
<li><span data-ttu-id="b2a49-177">BindCacheAdd</span><span class="sxs-lookup"><span data-stu-id="b2a49-177">BindCacheAdd</span></span></li>
<li><span data-ttu-id="b2a49-178">BindCacheAddRef</span><span class="sxs-lookup"><span data-stu-id="b2a49-178">BindCacheAddRef</span></span></li>
<li><span data-ttu-id="b2a49-179">AddReferralLink</span><span class="sxs-lookup"><span data-stu-id="b2a49-179">AddReferralLink</span></span></li>
<li><span data-ttu-id="b2a49-180">CommonRemoveEntry</span><span class="sxs-lookup"><span data-stu-id="b2a49-180">CommonRemoveEntry</span></span></li>
<li><span data-ttu-id="b2a49-181">BindCacheDerefHelper</span><span class="sxs-lookup"><span data-stu-id="b2a49-181">BindCacheDerefHelper</span></span></li>
<li><span data-ttu-id="b2a49-182">NotifyNewConnection</span><span class="sxs-lookup"><span data-stu-id="b2a49-182">NotifyNewConnection</span></span></li>
<li><span data-ttu-id="b2a49-183">QueryForConnection</span><span class="sxs-lookup"><span data-stu-id="b2a49-183">QueryForConnection</span></span></li>
<li><span data-ttu-id="b2a49-184">LdapOpenBindWithCredentials</span><span class="sxs-lookup"><span data-stu-id="b2a49-184">LdapOpenBindWithCredentials</span></span></li>
<li><span data-ttu-id="b2a49-185">LdapOpenBindWithDefaultCredentials</span><span class="sxs-lookup"><span data-stu-id="b2a49-185">LdapOpenBindWithDefaultCredentials</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b2a49-186">Você pode combinar sinalizadores combinando os bits apropriados no argumento *sinalizadores* .</span><span class="sxs-lookup"><span data-stu-id="b2a49-186">You can combine flags by combining the appropriate bits in the *traceFlags* argument.</span></span> <span data-ttu-id="b2a49-187">Por exemplo, para especificar o **\_ esquema de depuração** e Depurar sinalizadores de **\_ BINDCACHE** , o valor de *sinalizadores* apropriado seria 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="b2a49-187">For example, to specify the **DEBUG\_SCHEMA** and **DEBUG\_BINDCACHE** flags, the appropriate *traceFlags* value would be 0x00000009.</span></span>

<span data-ttu-id="b2a49-188">Por fim, o sinalizador *traceLevel* deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b2a49-188">Finally, the *traceLevel* flag should be one of the following values:</span></span>



|                                          |                       |
|------------------------------------------|-----------------------|
| <span data-ttu-id="b2a49-189">**\_erro no nível de rastreamento \_**</span><span class="sxs-lookup"><span data-stu-id="b2a49-189">**TRACE\_LEVEL\_ERROR**</span></span><br/>       | <span data-ttu-id="b2a49-190">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b2a49-190">0x00000002</span></span><br/> |
| <span data-ttu-id="b2a49-191">**\_informações de nível de rastreamento \_**</span><span class="sxs-lookup"><span data-stu-id="b2a49-191">**TRACE\_LEVEL\_INFORMATION**</span></span><br/> | <span data-ttu-id="b2a49-192">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b2a49-192">0x00000004</span></span><br/> |



 

<span data-ttu-id="b2a49-193">**Rastrear \_ \_As informações de nível** fazem com que o processo de rastreamento Registre todos os eventos, enquanto que o **\_ \_ erro no nível de rastreamento** faz com que o processo de rastreamento grave apenas eventos de erro.</span><span class="sxs-lookup"><span data-stu-id="b2a49-193">**TRACE\_LEVEL\_INFORMATION** causes the tracing process to record all events, whereas **TRACE\_LEVEL\_ERROR** causes the tracing process to record only error events.</span></span>

<span data-ttu-id="b2a49-194">Para encerrar o rastreamento, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="b2a49-194">To terminate tracing, run the following command:</span></span>

<span data-ttu-id="b2a49-195">**tracelog.exe-parar** *SessionName*</span><span class="sxs-lookup"><span data-stu-id="b2a49-195">**tracelog.exe -stop** *sessionname*</span></span>

<span data-ttu-id="b2a49-196">No exemplo anterior, *SessionName* é o mesmo nome que aquele fornecido com o comando que iniciou a seção de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="b2a49-196">In the previous example, *sessionname* is the same name as the one that was provided with the command that started the tracing section.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2a49-197">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2a49-197">Remarks</span></span>

<span data-ttu-id="b2a49-198">É mais eficaz rastrear apenas processos específicos especificando um PID específico do que rastrear todos os processos em um computador.</span><span class="sxs-lookup"><span data-stu-id="b2a49-198">It is more effective to trace only specific processes by specifying a particular PID than to trace all processes on a computer.</span></span> <span data-ttu-id="b2a49-199">Se você precisar rastrear vários aplicativos no mesmo computador, pode haver um impacto no desempenho; Há uma saída substancial de depuração nas seções orientadas a desempenho do código.</span><span class="sxs-lookup"><span data-stu-id="b2a49-199">If you do need to trace multiple applications on the same machine, there might be a performance impact; there is substantial debugging output in performance-oriented sections of the code.</span></span> <span data-ttu-id="b2a49-200">Além disso, os administradores devem ter cuidado para definir corretamente as permissões dos arquivos de log ao rastrear vários processos; caso contrário, qualquer usuário poderá ler os logs de rastreamento, e outros usuários poderão rastrear os processos que contêm informações seguras.</span><span class="sxs-lookup"><span data-stu-id="b2a49-200">Also, administrators must be careful to properly set the permissions of the log files when tracing multiple processes; otherwise, any user might be able to read the tracing logs, and other users will be able to trace processes that contain secure information.</span></span>

<span data-ttu-id="b2a49-201">Por exemplo, suponha que o administrador configure o rastreamento para um aplicativo "Test.exe" e não especifique um PID no registro para rastrear várias instâncias do processo.</span><span class="sxs-lookup"><span data-stu-id="b2a49-201">For example, presume the administrator sets up tracing for an application "Test.exe", and does not specify a PID in the registry to trace multiple instances of the process.</span></span> <span data-ttu-id="b2a49-202">Agora, outro usuário deseja rastrear o aplicativo "Secure.exe".</span><span class="sxs-lookup"><span data-stu-id="b2a49-202">Now another user wants to trace the application "Secure.exe".</span></span> <span data-ttu-id="b2a49-203">Se os arquivos de log de rastreamento não forem corretamente restritos, tudo o que o usuário precisará fazer é renomear "Secure.exe" como "Test.exe" e ele será rastreado.</span><span class="sxs-lookup"><span data-stu-id="b2a49-203">If the tracing log files are not properly restricted, all that user needs to do is rename "Secure.exe" to "Test.exe", and it will be traced.</span></span> <span data-ttu-id="b2a49-204">Em geral, é melhor rastrear apenas processos específicos durante a solução de problemas e remover a chave do registro de rastreamento assim que a solução de problemas é feita.</span><span class="sxs-lookup"><span data-stu-id="b2a49-204">In general, it is best to trace only specific processes while troubleshooting, and to remove the tracing registry key as soon as troubleshooting is done.</span></span>

<span data-ttu-id="b2a49-205">Como habilitar o rastreamento de eventos produzirá arquivos de log adicionais, os administradores devem monitorar atentamente os tamanhos dos arquivos de log; a falta de espaço em disco no computador local pode causar uma negação de serviço.</span><span class="sxs-lookup"><span data-stu-id="b2a49-205">Since enabling Event Tracing will produce extra log files, administrators should carefully monitor log file sizes; lack of disk space on the local computer can cause a denial-of-service.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="b2a49-206">Cenários de Exemplo</span><span class="sxs-lookup"><span data-stu-id="b2a49-206">Example Scenarios</span></span>

<span data-ttu-id="b2a49-207">Cenário 1: o administrador vê um erro inesperado em um aplicativo que define senhas para contas de usuário, para que elas executem as etapas a seguir para corrigir o problema usando o rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="b2a49-207">Scenario 1: The administrator sees an unexpected error in an application that sets passwords for user accounts, so they would take the following steps to fix the problem using Event Tracing.</span></span>

1.  <span data-ttu-id="b2a49-208">Escreva um script que reproduza o problema e crie a chave do registro</span><span class="sxs-lookup"><span data-stu-id="b2a49-208">Write a script that reproduces the problem, and create the registry key</span></span>

    <span data-ttu-id="b2a49-209">**HKEY \_ \_** cscript.exede \\  \\  \\  \\  \\ **rastreamento** \\ \*\*\*\* ADSI dos serviços do sistema de computador local CurrentControlSet</span><span class="sxs-lookup"><span data-stu-id="b2a49-209">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

2.  <span data-ttu-id="b2a49-210">Inicie uma sessão de rastreamento, configurando *sinalizadores* para 0X2 (**debug \_ CHANGEPASSWD**) e *traceLevel* para 0x4 (**informações de \_ nível \_ de rastreamento**), usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="b2a49-210">Start a tracing session, setting *traceFlags* to 0x2 (**DEBUG\_CHANGEPASSWD**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**), using the following command:</span></span>

    <span data-ttu-id="b2a49-211">**tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-a345-89d6b060174d-f. \\ ADSI. etl-flag 0x2-nível 0x4**</span><span class="sxs-lookup"><span data-stu-id="b2a49-211">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

3.  <span data-ttu-id="b2a49-212">Execute cscript.exe com o script de teste para reproduzir o problema e, em seguida, encerre a sessão de rastreamento:</span><span class="sxs-lookup"><span data-stu-id="b2a49-212">Run cscript.exe with their test script to reproduce the problem, and then terminate the tracing session:</span></span>

    <span data-ttu-id="b2a49-213">**tracelog.exe-parar scripttrace**</span><span class="sxs-lookup"><span data-stu-id="b2a49-213">**tracelog.exe -stop scripttrace**</span></span>

4.  <span data-ttu-id="b2a49-214">Excluir a chave do registro</span><span class="sxs-lookup"><span data-stu-id="b2a49-214">Delete the registry key</span></span>

    <span data-ttu-id="b2a49-215">**HKEY \_ \_** cscript.exede \\  \\  \\  \\  \\ **rastreamento** \\ \*\*\*\* ADSI dos serviços do sistema de computador local CurrentControlSet</span><span class="sxs-lookup"><span data-stu-id="b2a49-215">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

5.  <span data-ttu-id="b2a49-216">Execute a ferramenta ETW Tracerpt.exe para analisar as informações de rastreamento do log:</span><span class="sxs-lookup"><span data-stu-id="b2a49-216">Run the ETW tool Tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="b2a49-217">**tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-a345-89d6b060174d-f. \\ ADSI. etl-flag 0x2-nível 0x4**</span><span class="sxs-lookup"><span data-stu-id="b2a49-217">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

<span data-ttu-id="b2a49-218">Cenário 2: o administrador deseja rastrear a análise de esquema e as operações de download em um aplicativo [ASP](https://msdn.microsoft.com/asp.net/default.aspx) chamado w3wp.exe que já está em execução.</span><span class="sxs-lookup"><span data-stu-id="b2a49-218">Scenario 2: The administrator wants to trace the schema parsing and download operations in an [ASP](https://msdn.microsoft.com/asp.net/default.aspx) application named w3wp.exe that is already running.</span></span> <span data-ttu-id="b2a49-219">Para fazer isso, o administrador executaria as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="b2a49-219">To do this, the administrator would take the following steps:</span></span>

1.  <span data-ttu-id="b2a49-220">Criar a chave do registro</span><span class="sxs-lookup"><span data-stu-id="b2a49-220">Create the registry key</span></span>

    <span data-ttu-id="b2a49-221">**HKEY \_ \_** w3wp.exede \\  \\  \\  \\  \\ **rastreamento** \\ \*\*\*\* ADSI dos serviços do sistema de computador local CurrentControlSet</span><span class="sxs-lookup"><span data-stu-id="b2a49-221">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**</span></span>

    <span data-ttu-id="b2a49-222">e dentro dessa chave, crie um valor do tipo DWORD chamado PID e defina-o como a ID do processo da instância do w3wp.exe que está em execução no computador local.</span><span class="sxs-lookup"><span data-stu-id="b2a49-222">and inside that key, create a value of type DWORD that is named PID and set it to the process ID of the instance of w3wp.exe that is currently running on the local computer.</span></span>

2.  <span data-ttu-id="b2a49-223">Em seguida, eles criam uma sessão de rastreamento, definindo *sinalizadores* como 0x1 (**\_ esquema de depuração**) e *traceLevel* para 0x4 (**\_ \_ informações de nível de rastreamento**):</span><span class="sxs-lookup"><span data-stu-id="b2a49-223">Then they create a tracing session, setting *traceFlags* to 0x1 (**DEBUG\_SCHEMA**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**):</span></span>

    <span data-ttu-id="b2a49-224">**tracelog.exe-Start w3wptrace-GUID \# 7288c9f8-D63C-4932-a345-89d6b060174d-f. \\ w3wp. etl-flag 0x1-nível 0x4**</span><span class="sxs-lookup"><span data-stu-id="b2a49-224">**tracelog.exe -start w3wptrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\w3wp.etl -flag 0x1 -level 0x4**</span></span>

3.  <span data-ttu-id="b2a49-225">Reproduza a operação que precisa de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="b2a49-225">Reproduce the operation that needs troubleshooting.</span></span>
4.  <span data-ttu-id="b2a49-226">Encerrar a sessão de rastreamento:</span><span class="sxs-lookup"><span data-stu-id="b2a49-226">Terminate the tracing session:</span></span>

    <span data-ttu-id="b2a49-227">**tracelog.exe-parar w3wptrace**</span><span class="sxs-lookup"><span data-stu-id="b2a49-227">**tracelog.exe -stop w3wptrace**</span></span>

5.  <span data-ttu-id="b2a49-228">Exclua a chave do registro **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\  \\ **w3wp.exe**.</span><span class="sxs-lookup"><span data-stu-id="b2a49-228">Delete the registry key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**.</span></span>
6.  <span data-ttu-id="b2a49-229">Execute a ferramenta ETW tracerpt.exe para analisar as informações de rastreamento do log:</span><span class="sxs-lookup"><span data-stu-id="b2a49-229">Run the ETW tool tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="b2a49-230">**tracerpt.exe. \\ w3wp. etl-o-relatório**</span><span class="sxs-lookup"><span data-stu-id="b2a49-230">**tracerpt.exe .\\w3wp.etl -o -report**</span></span>

 


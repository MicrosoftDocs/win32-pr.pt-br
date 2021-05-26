---
title: Rastreamento de eventos no ADSI
description: O Windows Server 2008 e o Windows Vista introduzem o Rastreamento de Eventos em ADSI (Interfaces de Serviço do Active Directory).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- ADSI de rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b26aee00404f5cf97d228698f64fec804c28e62
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423706"
---
# <a name="event-tracing-in-adsi"></a><span data-ttu-id="58f5f-104">Rastreamento de eventos no ADSI</span><span class="sxs-lookup"><span data-stu-id="58f5f-104">Event Tracing in ADSI</span></span>

<span data-ttu-id="58f5f-105">O Windows Server 2008 e o Windows Vista introduzem o Rastreamento [de](/windows/desktop/ETW/event-tracing-portal) Eventos em [ADSI (Interfaces](active-directory-service-interfaces-adsi.md) de Serviço do Active Directory).</span><span class="sxs-lookup"><span data-stu-id="58f5f-105">Windows Server 2008 and Windows Vista introduce [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="58f5f-106">Determinadas áreas do Provedor LDAP ADSI têm uma implementação subjacente que é complexa ou que envolve uma sequência de etapas que dificulta o diagnóstico de problemas.</span><span class="sxs-lookup"><span data-stu-id="58f5f-106">Certain areas of the ADSI LDAP Provider have an underlying implementation that is complex or that involves a sequence of steps that makes it difficult to diagnose problems.</span></span> <span data-ttu-id="58f5f-107">Para ajudar os desenvolvedores de aplicativos a solucionar problemas, o Rastreamento de Eventos foi adicionado às seguintes áreas:</span><span class="sxs-lookup"><span data-stu-id="58f5f-107">To help application developers troubleshoot, Event Tracing has been added to the following areas:</span></span>

## <a name="schema-parsing-and-downloading"></a><span data-ttu-id="58f5f-108">Análise e download de esquema</span><span class="sxs-lookup"><span data-stu-id="58f5f-108">Schema Parsing and Downloading</span></span>

<span data-ttu-id="58f5f-109">A interface IADs no ADSI requer que o esquema LDAP seja armazenado em cache no cliente para que os atributos possam ser empacotados corretamente (conforme descrito no Modelo [de Esquema ADSI).](adsi-schema-model.md)</span><span class="sxs-lookup"><span data-stu-id="58f5f-109">The IADs interface in ADSI requires that the LDAP schema be cached on the client so that attributes can be marshaled correctly (as described in the [ADSI Schema Model](adsi-schema-model.md)).</span></span> <span data-ttu-id="58f5f-110">Para fazer isso, a ADSI carrega o esquema de cada processo (e para cada servidor/domínio LDAP) na memória de um arquivo de esquema (.sch) salvo no disco local ou baixando-o do servidor LDAP.</span><span class="sxs-lookup"><span data-stu-id="58f5f-110">To achieve this, ADSI loads the schema for each process (and for each LDAP server/domain) into memory either from a schema (.sch) file that is saved on the local disk or by downloading it from the LDAP server.</span></span> <span data-ttu-id="58f5f-111">Processos diferentes no mesmo computador cliente usam o esquema armazenado em cache no disco, se ele estiver disponível e aplicável.</span><span class="sxs-lookup"><span data-stu-id="58f5f-111">Different processes on the same client machine use the cached schema on disk if it is available and applicable.</span></span>

<span data-ttu-id="58f5f-112">Se o esquema não puder ser obtido do disco ou do servidor, a ADSI usará um esquema padrão em código.</span><span class="sxs-lookup"><span data-stu-id="58f5f-112">If the schema cannot be obtained from the disk or the server, ADSI uses a hardcoded default schema.</span></span> <span data-ttu-id="58f5f-113">Quando isso ocorre, os atributos que não fazem parte desse esquema padrão não podem ser marshaling e a ADSI retorna um erro ao recuperar esses atributos.</span><span class="sxs-lookup"><span data-stu-id="58f5f-113">When this occurs, attributes that are not part of this default schema cannot be marshaled and ADSI returns an error while retrieving these attributes.</span></span> <span data-ttu-id="58f5f-114">Vários fatores podem fazer com que isso aconteça, incluindo problemas na análise do esquema e privilégios insuficientes para baixar o esquema.</span><span class="sxs-lookup"><span data-stu-id="58f5f-114">A number of factors could cause this to happen, including problems in parsing the schema, and insufficient privileges to download the schema.</span></span> <span data-ttu-id="58f5f-115">Geralmente, é difícil determinar por que um determinado esquema padrão está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="58f5f-115">It is often difficult to determine why a certain default schema is being used.</span></span> <span data-ttu-id="58f5f-116">Usar o Rastreamento de Eventos nessa área ajudará a diagnosticar o problema mais rapidamente e corrigi-lo.</span><span class="sxs-lookup"><span data-stu-id="58f5f-116">Using Event Tracing in this area will help to more quickly diagnose the problem and fix it.</span></span>

## <a name="changing-and-setting-the-password"></a><span data-ttu-id="58f5f-117">Alterando e definindo a senha</span><span class="sxs-lookup"><span data-stu-id="58f5f-117">Changing and Setting the Password</span></span>

<span data-ttu-id="58f5f-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) e [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) empregam mais de um mecanismo para executar a operação solicitada com base na configuração disponível (conforme descrito em Configurando e alterando senhas de usuário com o [provedor LDAP).](setting-user-passwords-for-ldap-providers.md)</span><span class="sxs-lookup"><span data-stu-id="58f5f-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) and [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) employ more than one mechanism to perform the requested operation based on the available configuration (as described in [Setting and Changing User Passwords with the LDAP Provider](setting-user-passwords-for-ldap-providers.md)).</span></span> <span data-ttu-id="58f5f-119">Quando **ChangePassword** e **SetPassword** falham, pode ser difícil determinar exatamente o porquê, e o rastreamento de eventos ajudará a solucionar problemas com esses métodos.</span><span class="sxs-lookup"><span data-stu-id="58f5f-119">When **ChangePassword** and **SetPassword** fail, it can be difficult to determine exactly why, and Event Tracing will help to troubleshoot problems with these methods.</span></span>

## <a name="adsi-bind-cache"></a><span data-ttu-id="58f5f-120">Cache de associação ADSI</span><span class="sxs-lookup"><span data-stu-id="58f5f-120">ADSI Bind Cache</span></span>

<span data-ttu-id="58f5f-121">O ADSI tenta, internamente, reutilizar conexões LDAP sempre que possível (consulte [cache de conexão](connection-caching.md)).</span><span class="sxs-lookup"><span data-stu-id="58f5f-121">ADSI internally tries to reuse LDAP connections whenever possible (see [Connection Caching](connection-caching.md)).</span></span> <span data-ttu-id="58f5f-122">Ao solucionar problemas, é útil rastrear se uma nova conexão foi aberta para comunicação com o servidor ou se uma conexão existente foi usada.</span><span class="sxs-lookup"><span data-stu-id="58f5f-122">When troubleshooting, it is useful to trace whether a new connection was opened for communication with the server or whether an existing connection was used.</span></span> <span data-ttu-id="58f5f-123">Também pode ser útil rastrear o ciclo de vida do cache de conexão (às vezes chamado de cache de associação) e sua criação ou fechamento e se uma indicação de conexão ocorreu.</span><span class="sxs-lookup"><span data-stu-id="58f5f-123">It can also be useful to trace the lifecycle of the connection cache (sometimes referred to as the bind cache) and its creation or closure, and whether a connection referral took place.</span></span> <span data-ttu-id="58f5f-124">No caso de uma [ligação sem servidor](/windows/desktop/AD/serverless-binding-and-rootdse), a ADSI chama o localizador de DC para selecionar um servidor para o domínio do contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="58f5f-124">In the case of a [serverless bind](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI calls the DC locator to select a server for the domain of the user's context.</span></span> <span data-ttu-id="58f5f-125">Em seguida, o ADSI mantém um cache do mapeamento do servidor de domínio para conexões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="58f5f-125">ADSI then maintains a cache of the domain-server mapping for subsequent connections.</span></span> <span data-ttu-id="58f5f-126">O rastreamento de eventos ajuda a rastrear a seleção do controlador de domínio e, portanto, é útil para solucionar problemas relacionados à conexão.</span><span class="sxs-lookup"><span data-stu-id="58f5f-126">Event Tracing helps to trace the selection of the DC, and is therefore helpful in troubleshooting connection-related issues.</span></span>

## <a name="enabling-tracing-and-starting-a-tracing-session"></a><span data-ttu-id="58f5f-127">Habilitando o rastreamento e iniciando uma sessão de rastreamento</span><span class="sxs-lookup"><span data-stu-id="58f5f-127">Enabling Tracing and Starting a Tracing Session</span></span>

<span data-ttu-id="58f5f-128">Para ativar o rastreamento ADSI, crie a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="58f5f-128">To turn on ADSI tracing, create the following registry key:</span></span>

<span data-ttu-id="58f5f-129">**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** de \\  \\ **rastreamento** ADSI \\ **_ProcessName_**</span><span class="sxs-lookup"><span data-stu-id="58f5f-129">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**_ProcessName_**</span></span>

<span data-ttu-id="58f5f-130">*ProcessName* é o nome completo do processo que você deseja rastrear, incluindo sua extensão (por exemplo, "Svchost.exe").</span><span class="sxs-lookup"><span data-stu-id="58f5f-130">*ProcessName* is the full name of the process that you want to trace, including its extension (for example, "Svchost.exe").</span></span> <span data-ttu-id="58f5f-131">Além disso, você pode inserir um valor opcional do tipo **DWORD** chamado PID nesta chave.</span><span class="sxs-lookup"><span data-stu-id="58f5f-131">In addition, you can place an optional value of type **DWORD** named PID in this key.</span></span> <span data-ttu-id="58f5f-132">É altamente recomendável que você defina esse valor e, portanto, rastreie apenas um processo específico.</span><span class="sxs-lookup"><span data-stu-id="58f5f-132">It is highly recommended that you set this value and thereby trace only a particular process.</span></span> <span data-ttu-id="58f5f-133">Caso contrário, todas as instâncias do aplicativo especificado por *ProcessName* serão rastreadas.</span><span class="sxs-lookup"><span data-stu-id="58f5f-133">Otherwise, all instances of the application specified by *ProcessName* will be traced.</span></span>

<span data-ttu-id="58f5f-134">Em seguida, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="58f5f-134">Then execute the following command:</span></span>

<span data-ttu-id="58f5f-135">**tracelog.exe-Start** *SessionName* **- \#** GUID do _provedor \__ **de GUID-f** *filename* **-Flag** *sinalizadores* **de nível de**  arquivo</span><span class="sxs-lookup"><span data-stu-id="58f5f-135">**tracelog.exe -start** *sessionname* **-guid \#**_provider\_guid_ **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span></span>

<span data-ttu-id="58f5f-136">*sessionname* é simplesmente um identificador arbitrário usado para rotular a sessão de rastreamento (você precisará consultar esse nome de sessão posteriormente quando interromper a sessão de rastreamento).</span><span class="sxs-lookup"><span data-stu-id="58f5f-136">*sessionname* is simply an arbitrary identifier that is used to label the tracing session (you will need to refer to this session name later when you stop the tracing session).</span></span> <span data-ttu-id="58f5f-137">O GUID do provedor de rastreamento ADSI é "7288c9f8-d63c-4932-a345-89d6b060174d".</span><span class="sxs-lookup"><span data-stu-id="58f5f-137">The GUID for the ADSI tracking provider is "7288c9f8-d63c-4932-a345-89d6b060174d".</span></span> <span data-ttu-id="58f5f-138">*filename* especifica o logfile no qual os eventos serão gravados.</span><span class="sxs-lookup"><span data-stu-id="58f5f-138">*filename* specifies the logfile to which events will be written.</span></span> <span data-ttu-id="58f5f-139">*traceFlags* deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="58f5f-139">*traceFlags* should be one of the following values:</span></span>



|         <span data-ttu-id="58f5f-140">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="58f5f-140">Flag</span></span>                        |         <span data-ttu-id="58f5f-141">Valor</span><span class="sxs-lookup"><span data-stu-id="58f5f-141">Value</span></span>              |
|---------------------------------|-----------------------|
| <span data-ttu-id="58f5f-142">**ESQUEMA DE \_ DEPURAÇÃO**</span><span class="sxs-lookup"><span data-stu-id="58f5f-142">**DEBUG\_SCHEMA**</span></span><br/>    | <span data-ttu-id="58f5f-143">0x00000001</span><span class="sxs-lookup"><span data-stu-id="58f5f-143">0x00000001</span></span><br/> |
| <span data-ttu-id="58f5f-144">**DEPURAR \_ CHANGEPWD**</span><span class="sxs-lookup"><span data-stu-id="58f5f-144">**DEBUG\_CHANGEPWD**</span></span><br/> | <span data-ttu-id="58f5f-145">0x00000002</span><span class="sxs-lookup"><span data-stu-id="58f5f-145">0x00000002</span></span><br/> |
| <span data-ttu-id="58f5f-146">**DEPURAR \_ SETPWD**</span><span class="sxs-lookup"><span data-stu-id="58f5f-146">**DEBUG\_SETPWD**</span></span><br/>    | <span data-ttu-id="58f5f-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="58f5f-147">0x00000004</span></span><br/> |
| <span data-ttu-id="58f5f-148">**DEPURAR \_ BINDCACHE**</span><span class="sxs-lookup"><span data-stu-id="58f5f-148">**DEBUG\_BINDCACHE**</span></span><br/> | <span data-ttu-id="58f5f-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="58f5f-149">0x00000008</span></span><br/> |



 

<span data-ttu-id="58f5f-150">Esses sinalizadores determinam quais [métodos ADSI](active-directory-service-interfaces-adsi.md) serão rastreados, de acordo com a tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="58f5f-150">These flags determine which [ADSI](active-directory-service-interfaces-adsi.md) methods will be traced, according to the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="58f5f-151"><strong>DEBUG_SCHEMA</strong></span><span class="sxs-lookup"><span data-stu-id="58f5f-151"><strong>DEBUG_SCHEMA</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="58f5f-152">LdapGetSchema</span><span class="sxs-lookup"><span data-stu-id="58f5f-152">LdapGetSchema</span></span></li>
<li><span data-ttu-id="58f5f-153">GetSchemaInfoTime</span><span class="sxs-lookup"><span data-stu-id="58f5f-153">GetSchemaInfoTime</span></span></li>
<li><span data-ttu-id="58f5f-154">LdapReadSchemaInfoFromServer</span><span class="sxs-lookup"><span data-stu-id="58f5f-154">LdapReadSchemaInfoFromServer</span></span></li>
<li><span data-ttu-id="58f5f-155">ProcessSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="58f5f-155">ProcessSchemaInfo</span></span></li>
<li><span data-ttu-id="58f5f-156">HelperReadLdapSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="58f5f-156">HelperReadLdapSchemaInfo</span></span></li>
<li><span data-ttu-id="58f5f-157">ProcessClassInfoArray</span><span class="sxs-lookup"><span data-stu-id="58f5f-157">ProcessClassInfoArray</span></span></li>
<li><span data-ttu-id="58f5f-158">ReadSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="58f5f-158">ReadSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="58f5f-159">StoreSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="58f5f-159">StoreSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="58f5f-160">AttributeTypeDescription</span><span class="sxs-lookup"><span data-stu-id="58f5f-160">AttributeTypeDescription</span></span></li>
<li><span data-ttu-id="58f5f-161">ObjectClassDescription</span><span class="sxs-lookup"><span data-stu-id="58f5f-161">ObjectClassDescription</span></span></li>
<li><span data-ttu-id="58f5f-162">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="58f5f-162">DITContentRuleDescription</span></span></li>
<li><span data-ttu-id="58f5f-163">Directorystring</span><span class="sxs-lookup"><span data-stu-id="58f5f-163">DirectoryString</span></span></li>
<li><span data-ttu-id="58f5f-164">DirectoryStrings</span><span class="sxs-lookup"><span data-stu-id="58f5f-164">DirectoryStrings</span></span></li>
<li><span data-ttu-id="58f5f-165">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="58f5f-165">DITContentRuleDescription</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58f5f-166"><strong>DEBUG_CHANGEPWD</strong></span><span class="sxs-lookup"><span data-stu-id="58f5f-166"><strong>DEBUG_CHANGEPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="58f5f-167">CADsUser:: ChangePassword</span><span class="sxs-lookup"><span data-stu-id="58f5f-167">CADsUser::ChangePassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58f5f-168"><strong>DEBUG_SETPWD</strong></span><span class="sxs-lookup"><span data-stu-id="58f5f-168"><strong>DEBUG_SETPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="58f5f-169">CADsUser:: SetPassword</span><span class="sxs-lookup"><span data-stu-id="58f5f-169">CADsUser::SetPassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58f5f-170"><strong>DEBUG_BINDCACHE</strong></span><span class="sxs-lookup"><span data-stu-id="58f5f-170"><strong>DEBUG_BINDCACHE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="58f5f-171">GetServerBasedObject</span><span class="sxs-lookup"><span data-stu-id="58f5f-171">GetServerBasedObject</span></span></li>
<li><span data-ttu-id="58f5f-172">GetServerLessBasedObject</span><span class="sxs-lookup"><span data-stu-id="58f5f-172">GetServerLessBasedObject</span></span></li>
<li><span data-ttu-id="58f5f-173">GetGCDomainName</span><span class="sxs-lookup"><span data-stu-id="58f5f-173">GetGCDomainName</span></span></li>
<li><span data-ttu-id="58f5f-174">GetDefaultDomainName</span><span class="sxs-lookup"><span data-stu-id="58f5f-174">GetDefaultDomainName</span></span></li>
<li><span data-ttu-id="58f5f-175">GetUserDomainFlatName</span><span class="sxs-lookup"><span data-stu-id="58f5f-175">GetUserDomainFlatName</span></span></li>
<li><span data-ttu-id="58f5f-176">BindCacheLookup</span><span class="sxs-lookup"><span data-stu-id="58f5f-176">BindCacheLookup</span></span></li>
<li><span data-ttu-id="58f5f-177">EquivalentPortNumbers</span><span class="sxs-lookup"><span data-stu-id="58f5f-177">EquivalentPortNumbers</span></span></li>
<li><span data-ttu-id="58f5f-178">CanCredentialsBeReused</span><span class="sxs-lookup"><span data-stu-id="58f5f-178">CanCredentialsBeReused</span></span></li>
<li><span data-ttu-id="58f5f-179">BindCacheAdd</span><span class="sxs-lookup"><span data-stu-id="58f5f-179">BindCacheAdd</span></span></li>
<li><span data-ttu-id="58f5f-180">BindCacheAddRef</span><span class="sxs-lookup"><span data-stu-id="58f5f-180">BindCacheAddRef</span></span></li>
<li><span data-ttu-id="58f5f-181">AddReferralLink</span><span class="sxs-lookup"><span data-stu-id="58f5f-181">AddReferralLink</span></span></li>
<li><span data-ttu-id="58f5f-182">CommonRemoveEntry</span><span class="sxs-lookup"><span data-stu-id="58f5f-182">CommonRemoveEntry</span></span></li>
<li><span data-ttu-id="58f5f-183">BindCacheDerefHelper</span><span class="sxs-lookup"><span data-stu-id="58f5f-183">BindCacheDerefHelper</span></span></li>
<li><span data-ttu-id="58f5f-184">NotifyNewConnection</span><span class="sxs-lookup"><span data-stu-id="58f5f-184">NotifyNewConnection</span></span></li>
<li><span data-ttu-id="58f5f-185">QueryForConnection</span><span class="sxs-lookup"><span data-stu-id="58f5f-185">QueryForConnection</span></span></li>
<li><span data-ttu-id="58f5f-186">LdapOpenBindWithCredentials</span><span class="sxs-lookup"><span data-stu-id="58f5f-186">LdapOpenBindWithCredentials</span></span></li>
<li><span data-ttu-id="58f5f-187">LdapOpenBindWithDefaultCredentials</span><span class="sxs-lookup"><span data-stu-id="58f5f-187">LdapOpenBindWithDefaultCredentials</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="58f5f-188">Você pode combinar sinalizadores combinando os bits apropriados no *argumento traceFlags.*</span><span class="sxs-lookup"><span data-stu-id="58f5f-188">You can combine flags by combining the appropriate bits in the *traceFlags* argument.</span></span> <span data-ttu-id="58f5f-189">Por exemplo, para especificar os sinalizadores **DEBUG \_ SCHEMA** e **DEBUG \_ BINDCACHE,** o valor *de traceFlags* apropriado seria 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="58f5f-189">For example, to specify the **DEBUG\_SCHEMA** and **DEBUG\_BINDCACHE** flags, the appropriate *traceFlags* value would be 0x00000009.</span></span>

<span data-ttu-id="58f5f-190">Por fim, *o sinalizador traceLevel* deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="58f5f-190">Finally, the *traceLevel* flag should be one of the following values:</span></span>



|      <span data-ttu-id="58f5f-191">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="58f5f-191">Flag</span></span>                                    |       <span data-ttu-id="58f5f-192">Valor</span><span class="sxs-lookup"><span data-stu-id="58f5f-192">Value</span></span>                |
|------------------------------------------|-----------------------|
| <span data-ttu-id="58f5f-193">**ERRO DE \_ NÍVEL DE \_ RASTREAMENTO**</span><span class="sxs-lookup"><span data-stu-id="58f5f-193">**TRACE\_LEVEL\_ERROR**</span></span><br/>       | <span data-ttu-id="58f5f-194">0x00000002</span><span class="sxs-lookup"><span data-stu-id="58f5f-194">0x00000002</span></span><br/> |
| <span data-ttu-id="58f5f-195">**INFORMAÇÕES \_ DE NÍVEL DE \_ RASTREAMENTO**</span><span class="sxs-lookup"><span data-stu-id="58f5f-195">**TRACE\_LEVEL\_INFORMATION**</span></span><br/> | <span data-ttu-id="58f5f-196">0x00000004</span><span class="sxs-lookup"><span data-stu-id="58f5f-196">0x00000004</span></span><br/> |



 

<span data-ttu-id="58f5f-197">**RASTREAMENTO \_ LEVEL \_ INFORMATION** faz com que o processo de rastreamento grave todos os eventos, enquanto **TRACE LEVEL \_ \_ ERROR** faz com que o processo de rastreamento grave apenas eventos de erro.</span><span class="sxs-lookup"><span data-stu-id="58f5f-197">**TRACE\_LEVEL\_INFORMATION** causes the tracing process to record all events, whereas **TRACE\_LEVEL\_ERROR** causes the tracing process to record only error events.</span></span>

<span data-ttu-id="58f5f-198">Para encerrar o rastreamento, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="58f5f-198">To terminate tracing, run the following command:</span></span>

<span data-ttu-id="58f5f-199">**tracelog.exe -stop** *sessionname*</span><span class="sxs-lookup"><span data-stu-id="58f5f-199">**tracelog.exe -stop** *sessionname*</span></span>

<span data-ttu-id="58f5f-200">No exemplo anterior, *sessionname* é o mesmo nome que o fornecido com o comando que iniciou a seção de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="58f5f-200">In the previous example, *sessionname* is the same name as the one that was provided with the command that started the tracing section.</span></span>

## <a name="remarks"></a><span data-ttu-id="58f5f-201">Comentários</span><span class="sxs-lookup"><span data-stu-id="58f5f-201">Remarks</span></span>

<span data-ttu-id="58f5f-202">É mais eficaz rastrear apenas processos específicos especificando um PID específico do que rastrear todos os processos em um computador.</span><span class="sxs-lookup"><span data-stu-id="58f5f-202">It is more effective to trace only specific processes by specifying a particular PID than to trace all processes on a computer.</span></span> <span data-ttu-id="58f5f-203">Se você precisar rastrear vários aplicativos no mesmo computador, poderá haver um impacto no desempenho; há uma saída substancial de depuração nas seções orientadas ao desempenho do código.</span><span class="sxs-lookup"><span data-stu-id="58f5f-203">If you do need to trace multiple applications on the same machine, there might be a performance impact; there is substantial debugging output in performance-oriented sections of the code.</span></span> <span data-ttu-id="58f5f-204">Além disso, os administradores devem ter cuidado para definir corretamente as permissões dos arquivos de log ao rastrear vários processos; caso contrário, qualquer usuário poderá ler os logs de rastreamento e outros usuários poderão rastrear processos que contêm informações seguras.</span><span class="sxs-lookup"><span data-stu-id="58f5f-204">Also, administrators must be careful to properly set the permissions of the log files when tracing multiple processes; otherwise, any user might be able to read the tracing logs, and other users will be able to trace processes that contain secure information.</span></span>

<span data-ttu-id="58f5f-205">Por exemplo, presume que o administrador configura o rastreamento para um aplicativo "Test.exe" e não especifica um PID no Registro para rastrear várias instâncias do processo.</span><span class="sxs-lookup"><span data-stu-id="58f5f-205">For example, presume the administrator sets up tracing for an application "Test.exe", and does not specify a PID in the registry to trace multiple instances of the process.</span></span> <span data-ttu-id="58f5f-206">Agora, outro usuário deseja rastrear o aplicativo "Secure.exe".</span><span class="sxs-lookup"><span data-stu-id="58f5f-206">Now another user wants to trace the application "Secure.exe".</span></span> <span data-ttu-id="58f5f-207">Se os arquivos de log de rastreamento não forem corretamente restritos, tudo o que o usuário precisará fazer é renomear "Secure.exe" como "Test.exe" e ele será rastreado.</span><span class="sxs-lookup"><span data-stu-id="58f5f-207">If the tracing log files are not properly restricted, all that user needs to do is rename "Secure.exe" to "Test.exe", and it will be traced.</span></span> <span data-ttu-id="58f5f-208">Em geral, é melhor rastrear apenas processos específicos durante a solução de problemas e remover a chave do registro de rastreamento assim que a solução de problemas é feita.</span><span class="sxs-lookup"><span data-stu-id="58f5f-208">In general, it is best to trace only specific processes while troubleshooting, and to remove the tracing registry key as soon as troubleshooting is done.</span></span>

<span data-ttu-id="58f5f-209">Como habilitar o rastreamento de eventos produzirá arquivos de log adicionais, os administradores devem monitorar atentamente os tamanhos dos arquivos de log; a falta de espaço em disco no computador local pode causar uma negação de serviço.</span><span class="sxs-lookup"><span data-stu-id="58f5f-209">Since enabling Event Tracing will produce extra log files, administrators should carefully monitor log file sizes; lack of disk space on the local computer can cause a denial-of-service.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="58f5f-210">Cenários de Exemplo</span><span class="sxs-lookup"><span data-stu-id="58f5f-210">Example Scenarios</span></span>

<span data-ttu-id="58f5f-211">Cenário 1: o administrador vê um erro inesperado em um aplicativo que define senhas para contas de usuário, para que elas executem as etapas a seguir para corrigir o problema usando o rastreamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="58f5f-211">Scenario 1: The administrator sees an unexpected error in an application that sets passwords for user accounts, so they would take the following steps to fix the problem using Event Tracing.</span></span>

1.  <span data-ttu-id="58f5f-212">Escreva um script que reproduza o problema e crie a chave do registro</span><span class="sxs-lookup"><span data-stu-id="58f5f-212">Write a script that reproduces the problem, and create the registry key</span></span>

    <span data-ttu-id="58f5f-213">**HKEY \_ \_** cscript.exede \\  \\  \\  \\  \\ **rastreamento** \\ \*\*\*\* ADSI dos serviços do sistema de computador local CurrentControlSet</span><span class="sxs-lookup"><span data-stu-id="58f5f-213">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

2.  <span data-ttu-id="58f5f-214">Inicie uma sessão de rastreamento, configurando *sinalizadores* para 0X2 (**debug \_ CHANGEPASSWD**) e *traceLevel* para 0x4 (**informações de \_ nível \_ de rastreamento**), usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="58f5f-214">Start a tracing session, setting *traceFlags* to 0x2 (**DEBUG\_CHANGEPASSWD**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**), using the following command:</span></span>

    <span data-ttu-id="58f5f-215">**tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-a345-89d6b060174d-f. \\ ADSI. etl-flag 0x2-nível 0x4**</span><span class="sxs-lookup"><span data-stu-id="58f5f-215">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

3.  <span data-ttu-id="58f5f-216">Execute cscript.exe com o script de teste para reproduzir o problema e, em seguida, encerre a sessão de rastreamento:</span><span class="sxs-lookup"><span data-stu-id="58f5f-216">Run cscript.exe with their test script to reproduce the problem, and then terminate the tracing session:</span></span>

    <span data-ttu-id="58f5f-217">**tracelog.exe-parar scripttrace**</span><span class="sxs-lookup"><span data-stu-id="58f5f-217">**tracelog.exe -stop scripttrace**</span></span>

4.  <span data-ttu-id="58f5f-218">Excluir a chave do registro</span><span class="sxs-lookup"><span data-stu-id="58f5f-218">Delete the registry key</span></span>

    <span data-ttu-id="58f5f-219">**HKEY \_ \_** cscript.exede \\  \\  \\  \\  \\ **rastreamento** \\ \*\*\*\* ADSI dos serviços do sistema de computador local CurrentControlSet</span><span class="sxs-lookup"><span data-stu-id="58f5f-219">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

5.  <span data-ttu-id="58f5f-220">Execute a ferramenta ETW Tracerpt.exe para analisar as informações de rastreamento do log:</span><span class="sxs-lookup"><span data-stu-id="58f5f-220">Run the ETW tool Tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="58f5f-221">**tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-a345-89d6b060174d-f. \\ ADSI. etl-flag 0x2-nível 0x4**</span><span class="sxs-lookup"><span data-stu-id="58f5f-221">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

<span data-ttu-id="58f5f-222">Cenário 2: o administrador deseja rastrear a análise de esquema e as operações de download em um aplicativo [ASP](https://msdn.microsoft.com/asp.net/default.aspx) chamado w3wp.exe que já está em execução.</span><span class="sxs-lookup"><span data-stu-id="58f5f-222">Scenario 2: The administrator wants to trace the schema parsing and download operations in an [ASP](https://msdn.microsoft.com/asp.net/default.aspx) application named w3wp.exe that is already running.</span></span> <span data-ttu-id="58f5f-223">Para fazer isso, o administrador executaria as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="58f5f-223">To do this, the administrator would take the following steps:</span></span>

1.  <span data-ttu-id="58f5f-224">Criar a chave do registro</span><span class="sxs-lookup"><span data-stu-id="58f5f-224">Create the registry key</span></span>

    <span data-ttu-id="58f5f-225">**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**</span><span class="sxs-lookup"><span data-stu-id="58f5f-225">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**</span></span>

    <span data-ttu-id="58f5f-226">e dentro dessa chave, crie um valor do tipo DWORD chamado PID e de definido como a ID de processo da instância do w3wp.exe que está sendo executado no computador local.</span><span class="sxs-lookup"><span data-stu-id="58f5f-226">and inside that key, create a value of type DWORD that is named PID and set it to the process ID of the instance of w3wp.exe that is currently running on the local computer.</span></span>

2.  <span data-ttu-id="58f5f-227">Em seguida, eles criam uma sessão de rastreamento, definindo *traceFlags* como 0x1 (**DEBUG \_ SCHEMA**) e *traceLevel* como 0x4 (**TRACE LEVEL \_ \_ INFORMATION**):</span><span class="sxs-lookup"><span data-stu-id="58f5f-227">Then they create a tracing session, setting *traceFlags* to 0x1 (**DEBUG\_SCHEMA**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**):</span></span>

    <span data-ttu-id="58f5f-228">**tracelog.exe -start w3wptrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ w3wp.etl -flag 0x1 -level 0x4**</span><span class="sxs-lookup"><span data-stu-id="58f5f-228">**tracelog.exe -start w3wptrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\w3wp.etl -flag 0x1 -level 0x4**</span></span>

3.  <span data-ttu-id="58f5f-229">Reproduza a operação que precisa de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="58f5f-229">Reproduce the operation that needs troubleshooting.</span></span>
4.  <span data-ttu-id="58f5f-230">Encerrar a sessão de rastreamento:</span><span class="sxs-lookup"><span data-stu-id="58f5f-230">Terminate the tracing session:</span></span>

    <span data-ttu-id="58f5f-231">**tracelog.exe -stop w3wptrace**</span><span class="sxs-lookup"><span data-stu-id="58f5f-231">**tracelog.exe -stop w3wptrace**</span></span>

5.  <span data-ttu-id="58f5f-232">Exclua a chave do Registro **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**.</span><span class="sxs-lookup"><span data-stu-id="58f5f-232">Delete the registry key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**.</span></span>
6.  <span data-ttu-id="58f5f-233">Execute a ferramenta ETW tracerpt.exe para analisar as informações de rastreamento do log:</span><span class="sxs-lookup"><span data-stu-id="58f5f-233">Run the ETW tool tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="58f5f-234">**tracerpt.exe . \\ w3wp.etl -o -report**</span><span class="sxs-lookup"><span data-stu-id="58f5f-234">**tracerpt.exe .\\w3wp.etl -o -report**</span></span>

 


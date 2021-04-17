---
description: Conecta-se ao namespace no computador especificado no parâmetro strServer.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: Método SWbemLocator. ConnectServer (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 31c2e6de8cf1504543727cad056a3616a51182d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761235"
---
# <a name="swbemlocatorconnectserver-method"></a><span data-ttu-id="a90c5-103">Método SWbemLocator. ConnectServer</span><span class="sxs-lookup"><span data-stu-id="a90c5-103">SWbemLocator.ConnectServer method</span></span>

<span data-ttu-id="a90c5-104">O método **ConnectServer** do objeto [**SWbemLocator**](swbemlocator.md) se conecta ao namespace no computador especificado no parâmetro *strServer* .</span><span class="sxs-lookup"><span data-stu-id="a90c5-104">The **ConnectServer** method of the [**SWbemLocator**](swbemlocator.md) object connects to the namespace on the computer that is specified in the *strServer* parameter.</span></span> <span data-ttu-id="a90c5-105">O computador de destino pode ser local ou remoto, mas ele deve ter o WMI instalado.</span><span class="sxs-lookup"><span data-stu-id="a90c5-105">The target computer can be either local or remote, but it must have WMI installed.</span></span> <span data-ttu-id="a90c5-106">Para obter exemplos e uma comparação com o tipo de moniker de conexão, consulte [criando um script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="a90c5-106">For examples and a comparison with the moniker type of connection, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

<span data-ttu-id="a90c5-107">A partir do Windows Vista, o **SWbemLocator. ConnectServer** pode se conectar a computadores que executam o IPv6 usando um endereço IPv6 no parâmetro *strServer* .</span><span class="sxs-lookup"><span data-stu-id="a90c5-107">Starting with Windows Vista, **SWbemLocator.ConnectServer** can connect with computers running IPv6 using an IPv6 address in the *strServer* parameter.</span></span> <span data-ttu-id="a90c5-108">Para obter mais informações, consulte [suporte a IPv6 e IPv4 no WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a90c5-108">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="a90c5-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a90c5-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a90c5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a90c5-110">Syntax</span></span>


```VB
objwbemServices = .ConnectServer( _
  [ ByVal strServer ], _
  [ ByVal strNamespace ], _
  [ ByVal strUser ], _
  [ ByVal strPassword ], _
  [ ByVal strLocale ], _
  [ ByVal strAuthority ], _
  [ ByVal iSecurityFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a90c5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a90c5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a90c5-112">*strServer* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a90c5-112">*strServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-113">Nome do computador ao qual você está se conectando.</span><span class="sxs-lookup"><span data-stu-id="a90c5-113">Computer name to which you are connecting.</span></span> <span data-ttu-id="a90c5-114">Se o computador remoto estiver em um domínio diferente da conta de usuário sob a qual você faz logon, use o nome do computador totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="a90c5-114">If the remote computer is in a different domain than the user account under which you log in, then use the fully qualified computer name.</span></span> <span data-ttu-id="a90c5-115">Se você não fornecer esse parâmetro, a chamada usa como padrão o computador local.</span><span class="sxs-lookup"><span data-stu-id="a90c5-115">If you do not provide this parameter, the call defaults to the local computer.</span></span>

<span data-ttu-id="a90c5-116">Exemplo: `server1.network.fabrikam`</span><span class="sxs-lookup"><span data-stu-id="a90c5-116">Example: `server1.network.fabrikam`</span></span>

<span data-ttu-id="a90c5-117">Você também pode usar um endereço IP nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a90c5-117">You also can use an IP address in this parameter.</span></span> <span data-ttu-id="a90c5-118">Se o endereço IP estiver no formato IPv6, o computador de destino deverá estar executando o IPv6.</span><span class="sxs-lookup"><span data-stu-id="a90c5-118">If the IP address is in IPv6 format, the target computer must be running IPv6.</span></span> <span data-ttu-id="a90c5-119">Um endereço em IPv4 é semelhante a `123.123.123.123`</span><span class="sxs-lookup"><span data-stu-id="a90c5-119">An address in IPv4 looks like `123.123.123.123`</span></span>

<span data-ttu-id="a90c5-120">Um endereço IP no formato IPv6 é semelhante a `2010:836B:4179::836B:4179`</span><span class="sxs-lookup"><span data-stu-id="a90c5-120">An IP address in IPv6 format looks like `2010:836B:4179::836B:4179`</span></span>

<span data-ttu-id="a90c5-121">Para obter mais informações sobre DNS e IPv4, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="a90c5-121">For more information on DNS and IPv4, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="a90c5-122">*strNamespace* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a90c5-122">*strNamespace* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-123">Cadeia de caracteres que especifica o namespace no qual você faz logon.</span><span class="sxs-lookup"><span data-stu-id="a90c5-123">String that specifies the namespace to which you log on.</span></span> <span data-ttu-id="a90c5-124">Por exemplo, para fazer logon no namespace raiz \\ padrão, use o \\ padrão raiz.</span><span class="sxs-lookup"><span data-stu-id="a90c5-124">For example, to log on to the root\\default namespace, use root\\default.</span></span> <span data-ttu-id="a90c5-125">Se você não especificar esse parâmetro, o padrão será o namespace configurado como o namespace padrão para scripts.</span><span class="sxs-lookup"><span data-stu-id="a90c5-125">If you do not specify this parameter, it defaults to the namespace that is configured as the default namespace for scripting.</span></span> <span data-ttu-id="a90c5-126">Para obter mais informações, consulte [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="a90c5-126">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

<span data-ttu-id="a90c5-127">Exemplo: "raiz \\ cimv2"</span><span class="sxs-lookup"><span data-stu-id="a90c5-127">Example: "root\\CIMV2"</span></span>

</dd> <dt>

<span data-ttu-id="a90c5-128">*strUser* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a90c5-128">*strUser* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-129">Nome de usuário a ser usado para se conectar.</span><span class="sxs-lookup"><span data-stu-id="a90c5-129">User name to use to connect.</span></span> <span data-ttu-id="a90c5-130">A cadeia de caracteres pode estar na forma de um nome de usuário ou de um domínio de \\ usuário.</span><span class="sxs-lookup"><span data-stu-id="a90c5-130">The string can be in the form of either a user name or a Domain\\Username.</span></span> <span data-ttu-id="a90c5-131">Deixe esse parâmetro em branco para usar o contexto de segurança atual.</span><span class="sxs-lookup"><span data-stu-id="a90c5-131">Leave this parameter blank to use the current security context.</span></span> <span data-ttu-id="a90c5-132">O parâmetro *strUser* só deve ser usado com conexões com servidores WMI remotos.</span><span class="sxs-lookup"><span data-stu-id="a90c5-132">The *strUser* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="a90c5-133">Se você tentar especificar *strUser* para uma conexão WMI local, a tentativa de conexão falhará.</span><span class="sxs-lookup"><span data-stu-id="a90c5-133">If you attempt to specify *strUser* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="a90c5-134">Se a autenticação Kerberos estiver em uso, o nome de usuário e a senha especificados em *strUser* e *strPassword* não poderão ser interceptados em uma rede.</span><span class="sxs-lookup"><span data-stu-id="a90c5-134">If Kerberos authentication is in use, then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on a network.</span></span> <span data-ttu-id="a90c5-135">Você pode usar o formato UPN para especificar o *strUser*.</span><span class="sxs-lookup"><span data-stu-id="a90c5-135">You can use the UPN format to specify the *strUser*.</span></span>

<span data-ttu-id="a90c5-136">Exemplo: "nome_do_domínio nome de \\ usuário"</span><span class="sxs-lookup"><span data-stu-id="a90c5-136">Example: "DomainName\\UserName"</span></span>

> [!Note]  
> <span data-ttu-id="a90c5-137">Se um domínio for especificado em *strAuthority*, o domínio não deverá ser especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="a90c5-137">If a domain is specified in *strAuthority*, then the domain must not be specified here.</span></span> <span data-ttu-id="a90c5-138">A especificação do domínio em ambos os parâmetros resulta em um erro de parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="a90c5-138">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="a90c5-139">*strPassword* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a90c5-139">*strPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-140">Cadeia de caracteres que especifica a senha a ser usada ao tentar se conectar.</span><span class="sxs-lookup"><span data-stu-id="a90c5-140">String that specifies the password to use when attempting to connect.</span></span> <span data-ttu-id="a90c5-141">Deixe o parâmetro em branco para usar o contexto de segurança atual.</span><span class="sxs-lookup"><span data-stu-id="a90c5-141">Leave the parameter blank to use the current security context.</span></span> <span data-ttu-id="a90c5-142">O parâmetro *strPassword* só deve ser usado com conexões com servidores WMI remotos.</span><span class="sxs-lookup"><span data-stu-id="a90c5-142">The *strPassword* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="a90c5-143">Se você tentar especificar *strPassword* para uma conexão WMI local, a tentativa de conexão falhará.</span><span class="sxs-lookup"><span data-stu-id="a90c5-143">If you attempt to specify *strPassword* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="a90c5-144">Se a autenticação Kerberos estiver em uso, o nome de usuário e a senha especificados em *strUser* e *strPassword* não poderão ser interceptados na rede.</span><span class="sxs-lookup"><span data-stu-id="a90c5-144">If Kerberos authentication is in use then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on the network.</span></span>

</dd> <dt>

<span data-ttu-id="a90c5-145">*strLocale* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a90c5-145">*strLocale* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-146">Cadeia de caracteres que especifica o código de localização.</span><span class="sxs-lookup"><span data-stu-id="a90c5-146">String that specifies the localization code.</span></span> <span data-ttu-id="a90c5-147">Se você quiser usar a localidade atual, deixe em branco.</span><span class="sxs-lookup"><span data-stu-id="a90c5-147">If you want to use the current locale, leave it blank.</span></span> <span data-ttu-id="a90c5-148">Se não estiver em branco, esse parâmetro deverá ser uma cadeia de caracteres que indica a localidade desejada onde as informações devem ser recuperadas.</span><span class="sxs-lookup"><span data-stu-id="a90c5-148">If not blank, this parameter must be a string that indicates the desired locale where information must be retrieved.</span></span> <span data-ttu-id="a90c5-149">Para identificadores de localidade da Microsoft, o formato da cadeia de caracteres é "MS \_ xxxx", onde xxxx é uma cadeia de caracteres no formato hexadecimal que indica o LCID.</span><span class="sxs-lookup"><span data-stu-id="a90c5-149">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in the hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="a90c5-150">Por exemplo, inglês americano apareceria como "MS \_ 409".</span><span class="sxs-lookup"><span data-stu-id="a90c5-150">For example, American English would appear as "MS\_409".</span></span>

</dd> <dt>

<span data-ttu-id="a90c5-151">*strAuthority* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a90c5-151">*strAuthority* \[in, optional\]</span></span>
</dt> <dd>

<dt>

<span data-ttu-id="a90c5-152">""</span><span class="sxs-lookup"><span data-stu-id="a90c5-152">""</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-153">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="a90c5-153">This parameter is optional.</span></span> <span data-ttu-id="a90c5-154">No entanto, se for especificado, somente Kerberos ou NTLMDomain poderão ser usados.</span><span class="sxs-lookup"><span data-stu-id="a90c5-154">However, if it is specified, only Kerberos or NTLMDomain can be used.</span></span>

</dd> <dt>

<span data-ttu-id="a90c5-155">Kerberos</span><span class="sxs-lookup"><span data-stu-id="a90c5-155">Kerberos:</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-156">Se o parâmetro *strAuthority* começar com a cadeia de caracteres "Kerberos:", a autenticação Kerberos será usada e esse parâmetro deverá conter um nome de entidade de segurança Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a90c5-156">If the *strAuthority* parameter begins with the string "Kerberos:", then Kerberos authentication is used and this parameter should contain a Kerberos principal name.</span></span> <span data-ttu-id="a90c5-157">O nome da entidade de segurança Kerberos é especificado como Kerberos:*Domain*, por exemplo, `Kerberos:fabrikam` onde `fabrikam` é o servidor ao qual você está tentando se conectar.</span><span class="sxs-lookup"><span data-stu-id="a90c5-157">The Kerberos principal name is specified as Kerberos:*domain*, such as `Kerberos:fabrikam` where `fabrikam` is the server to which you are attempting to connect.</span></span>

<span data-ttu-id="a90c5-158">Exemplo: "Kerberos: DOMAIN"</span><span class="sxs-lookup"><span data-stu-id="a90c5-158">Example: "Kerberos:DOMAIN"</span></span>

</dd> <dt>

<span data-ttu-id="a90c5-159">NTLMDomain:</span><span class="sxs-lookup"><span data-stu-id="a90c5-159">NTLMDomain:</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-160">Para usar a autenticação NTLM (NT LAN Manager), você deve especificá-la como NTLMDomain:*Domain*, por exemplo, `NTLMDomain:fabrikam` onde `fabrikam` é o nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="a90c5-160">To use NT Lan Manager (NTLM) authentication, you must specify it as NTLMDomain:*domain*, such as `NTLMDomain:fabrikam` where `fabrikam` is the name of the domain.</span></span>

<span data-ttu-id="a90c5-161">Exemplo: "NTLMDomain: DOMAIN"</span><span class="sxs-lookup"><span data-stu-id="a90c5-161">Example: "NTLMDomain:DOMAIN"</span></span>

</dd> </dl>

<span data-ttu-id="a90c5-162">Se você deixar esse parâmetro em branco, o sistema operacional negociará com com para determinar se a autenticação NTLM ou Kerberos será usada.</span><span class="sxs-lookup"><span data-stu-id="a90c5-162">If you leave this parameter blank, the operating system negotiates with COM to determine whether NTLM or Kerberos authentication is used.</span></span> <span data-ttu-id="a90c5-163">Esse parâmetro só deve ser usado com conexões com servidores WMI remotos.</span><span class="sxs-lookup"><span data-stu-id="a90c5-163">This parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="a90c5-164">Se você tentar definir a autoridade para uma conexão WMI local, a tentativa de conexão falhará.</span><span class="sxs-lookup"><span data-stu-id="a90c5-164">If you attempt to set the authority for a local WMI connection, the connection attempt fails.</span></span>

> [!Note]  
> <span data-ttu-id="a90c5-165">Se o domínio for especificado em *strUser*, que é o local preferido, ele não deverá ser especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="a90c5-165">If the domain is specified in *strUser*, which is the preferred location, then it must not be specified here.</span></span> <span data-ttu-id="a90c5-166">A especificação do domínio em ambos os parâmetros resulta em um erro de parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="a90c5-166">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="a90c5-167">*iSecurityFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a90c5-167">*iSecurityFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-168">Usado para passar valores de sinalizador para **ConnectServer**.</span><span class="sxs-lookup"><span data-stu-id="a90c5-168">Used to pass flag values to **ConnectServer**.</span></span>

<dt>

<span data-ttu-id="a90c5-169">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="a90c5-169">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-170">Um valor de 0 para esse parâmetro faz com que a chamada para **ConnectServer** seja retornada somente depois que a conexão com o servidor é estabelecida.</span><span class="sxs-lookup"><span data-stu-id="a90c5-170">A value of 0 for this parameter causes the call to **ConnectServer** to return only after the connection to the server is established.</span></span> <span data-ttu-id="a90c5-171">Isso pode fazer com que o programa pare de responder indefinidamente se não for possível estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="a90c5-171">This could cause your program to stop responding indefinitely if the connection cannot be established.</span></span>

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span data-ttu-id="a90c5-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="a90c5-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>\*\*\*\*wbemConnectFlagUseMaxWait\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="a90c5-173">A chamada **ConnectServer** é garantida para retornar em 2 minutos ou menos.</span><span class="sxs-lookup"><span data-stu-id="a90c5-173">The **ConnectServer** call is guaranteed to return in 2 minutes or less.</span></span> <span data-ttu-id="a90c5-174">Use esse sinalizador para impedir que o programa deixar responda indefinidamente se não for possível estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="a90c5-174">Use this flag to prevent your program from ceasing to respond indefinitely if the connection cannot be established.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a90c5-175">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a90c5-175">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-176">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="a90c5-176">Typically, this is undefined.</span></span> <span data-ttu-id="a90c5-177">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="a90c5-177">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="a90c5-178">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="a90c5-178">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a90c5-179">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a90c5-179">Return value</span></span>

<span data-ttu-id="a90c5-180">Se for bem-sucedido, o WMI retornará um objeto [**SWbemServices**](swbemservices.md) que está associado ao namespace especificado em *strNamespace* no computador especificado em *strServer*.</span><span class="sxs-lookup"><span data-stu-id="a90c5-180">If successful, WMI returns an [**SWbemServices**](swbemservices.md) object that is bound to the namespace that is specified in *strNamespace* on the computer that is specified in *strServer*.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a90c5-181">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a90c5-181">Error codes</span></span>

<span data-ttu-id="a90c5-182">Após a conclusão do método **ConnectServer** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="a90c5-182">After the completion of the **ConnectServer** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a90c5-183">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="a90c5-183">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-184">O nome de usuário e a senha atuais ou especificados não eram válidos ou autorizados a estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="a90c5-184">The current or specified user name and password were not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="a90c5-185">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a90c5-185">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-186">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="a90c5-186">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a90c5-187">**wbemErrInvalidNamespace** -2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="a90c5-187">**wbemErrInvalidNamespace** - 2147749902 (0x8004100E)</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-188">O namespace especificado não existia no servidor.</span><span class="sxs-lookup"><span data-stu-id="a90c5-188">The specified namespace did not exist on the server.</span></span>

</dd> <dt>

<span data-ttu-id="a90c5-189">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a90c5-189">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-190">Um parâmetro inválido foi especificado ou o namespace não pôde ser analisado.</span><span class="sxs-lookup"><span data-stu-id="a90c5-190">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="a90c5-191">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a90c5-191">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-192">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="a90c5-192">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a90c5-193">**wbemErrTransportFailure** -2147749909</span><span class="sxs-lookup"><span data-stu-id="a90c5-193">**wbemErrTransportFailure** - 2147749909</span></span>
</dt> <dd>

<span data-ttu-id="a90c5-194">Ocorreu um erro de rede, impedindo A operação normal.</span><span class="sxs-lookup"><span data-stu-id="a90c5-194">A networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a90c5-195">Comentários</span><span class="sxs-lookup"><span data-stu-id="a90c5-195">Remarks</span></span>

<span data-ttu-id="a90c5-196">O método **ConnectServer** geralmente é usado ao se conectar a uma conta com credenciais de nome de usuário e senha diferentes em um computador remoto porque você não pode especificar uma senha diferente em uma cadeia de caracteres de [moniker](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="a90c5-196">The **ConnectServer** method is often used when connecting to an account with a different username and password credentials on a remote computer because you cannot specify a different password in a [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="a90c5-197">Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="a90c5-197">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="a90c5-198">Usar um endereço IPv4 para se conectar a um servidor remoto pode resultar em um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="a90c5-198">Using an IPv4 address to connect to a remote server may result in unexpected behavior.</span></span> <span data-ttu-id="a90c5-199">A causa provável é as entradas DNS obsoletas em seu ambiente.</span><span class="sxs-lookup"><span data-stu-id="a90c5-199">The likely cause is stale DNS entries in your environment.</span></span> <span data-ttu-id="a90c5-200">Nessas circunstâncias, a entrada PTR obsoleta para o computador será usada, com resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="a90c5-200">In these circumstances, the stale PTR entry for the machine will be used, with unpredictable results.</span></span> <span data-ttu-id="a90c5-201">Para evitar esse comportamento, você pode acrescentar um ponto (".") ao endereço IP antes de chamar ConnectServer.</span><span class="sxs-lookup"><span data-stu-id="a90c5-201">To avoid this behavior, you can append a period (".") to the IP address before calling ConnectServer.</span></span> <span data-ttu-id="a90c5-202">Isso faz com que a pesquisa de DNS reverso falhe, mas pode permitir que a chamada **ConnectServer** seja bem-sucedida no computador correto.</span><span class="sxs-lookup"><span data-stu-id="a90c5-202">This causes the reverse DNS lookup to fail, but may allow the **ConnectServer** call to succeed on the correct machine.</span></span>

## <a name="examples"></a><span data-ttu-id="a90c5-203">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a90c5-203">Examples</span></span>

<span data-ttu-id="a90c5-204">O exemplo de código VBScript a seguir descreve como se conectar a um computador remoto para obter dados do [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) .</span><span class="sxs-lookup"><span data-stu-id="a90c5-204">The following VBScript code example describes how to connect to a remote computer to obtain [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) data.</span></span> <span data-ttu-id="a90c5-205">O nome de domínio especificado em *strDomain* é usado em *strAuthority*.</span><span class="sxs-lookup"><span data-stu-id="a90c5-205">The domain name that is specified in *strDomain* is used in *strAuthority*.</span></span>


```VB
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```



<span data-ttu-id="a90c5-206">O trecho do PowerShell a seguir acessa um servidor remoto e lista as classes WMI disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a90c5-206">The following PowerShell snippet access a remote server and lists the available WMI classes.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="a90c5-207">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a90c5-207">Requirements</span></span>



| <span data-ttu-id="a90c5-208">Requisito</span><span class="sxs-lookup"><span data-stu-id="a90c5-208">Requirement</span></span> | <span data-ttu-id="a90c5-209">Valor</span><span class="sxs-lookup"><span data-stu-id="a90c5-209">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a90c5-210">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a90c5-210">Minimum supported client</span></span><br/> | <span data-ttu-id="a90c5-211">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a90c5-211">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a90c5-212">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a90c5-212">Minimum supported server</span></span><br/> | <span data-ttu-id="a90c5-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a90c5-213">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a90c5-214">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a90c5-214">Header</span></span><br/>                   | <dl> <span data-ttu-id="a90c5-215"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a90c5-215"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a90c5-216">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a90c5-216">Type library</span></span><br/>             | <dl> <span data-ttu-id="a90c5-217"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a90c5-217"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a90c5-218">DLL</span><span class="sxs-lookup"><span data-stu-id="a90c5-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a90c5-219"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a90c5-219"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a90c5-220">CLSID</span><span class="sxs-lookup"><span data-stu-id="a90c5-220">CLSID</span></span><br/>                    | <span data-ttu-id="a90c5-221">\_SWBEMLOCATOR CLSID</span><span class="sxs-lookup"><span data-stu-id="a90c5-221">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="a90c5-222">IID</span><span class="sxs-lookup"><span data-stu-id="a90c5-222">IID</span></span><br/>                      | <span data-ttu-id="a90c5-223">ISWbemLocator de IID \_</span><span class="sxs-lookup"><span data-stu-id="a90c5-223">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="a90c5-224">Confira também</span><span class="sxs-lookup"><span data-stu-id="a90c5-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a90c5-225">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="a90c5-225">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="a90c5-226">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="a90c5-226">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="a90c5-227">Conectando-se ao WMI em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="a90c5-227">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="a90c5-228">Criando um script WMI</span><span class="sxs-lookup"><span data-stu-id="a90c5-228">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> </dl>

 


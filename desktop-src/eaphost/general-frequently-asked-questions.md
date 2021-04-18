---
title: Perguntas frequentes gerais
description: Leia as respostas para as perguntas mais frequentes sobre as APIs do EAPHost, como ' Qual é o tempo de vida de uma autenticação? '.
ms.assetid: 4025e8da-8cb1-477b-86bb-7756d9636224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb0dd9b3b997d8682c3cab1ba91afc3ee2db7ba
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "105812034"
---
# <a name="general-frequently-asked-questions"></a><span data-ttu-id="226da-103">Perguntas frequentes gerais</span><span class="sxs-lookup"><span data-stu-id="226da-103">General Frequently Asked Questions</span></span>

<span data-ttu-id="226da-104">O tópico a seguir fornece respostas para perguntas mais frequentes sobre as APIs do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="226da-104">The following topic provides answers to commonly-asked questions about the EAPHost APIs.</span></span>

### <a name="general-frequently-asked-questions"></a><span data-ttu-id="226da-105">Perguntas frequentes gerais</span><span class="sxs-lookup"><span data-stu-id="226da-105">General Frequently Asked Questions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="226da-106">Pergunta</span><span class="sxs-lookup"><span data-stu-id="226da-106">Question</span></span></th>
<th><span data-ttu-id="226da-107">Resposta</span><span class="sxs-lookup"><span data-stu-id="226da-107">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="226da-108">O que é um suplicante?</span><span class="sxs-lookup"><span data-stu-id="226da-108">What is a supplicant?</span></span></td>
<td><span data-ttu-id="226da-109">O suplicante é a entidade a ser autenticada usando o EAPHost.</span><span class="sxs-lookup"><span data-stu-id="226da-109">The supplicant is the entity to be authenticated using EAPHost.</span></span> <span data-ttu-id="226da-110">Os suplicantes típicos são clientes [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) , 802,3 clientes e RRAS (serviço de roteamento e acesso remoto), clientes de ponto a ponto (PPP).</span><span class="sxs-lookup"><span data-stu-id="226da-110">Typical supplicants are [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) clients, 802.3 clients, and Routing and Remote Access Service (RRAS), Point-to-Point (PPP) clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="226da-111">O que é um par?</span><span class="sxs-lookup"><span data-stu-id="226da-111">What is a peer?</span></span></td>
<td><span data-ttu-id="226da-112">O par é o lado do cliente de uma autenticação EAP.</span><span class="sxs-lookup"><span data-stu-id="226da-112">The peer is the client side of an EAP authentication.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="226da-113">Como um par difere de um suplicante?</span><span class="sxs-lookup"><span data-stu-id="226da-113">How does a peer differ from a supplicant?</span></span></td>
<td><span data-ttu-id="226da-114">O suplicante transporta pacotes, enquanto um par não.</span><span class="sxs-lookup"><span data-stu-id="226da-114">The supplicant transports packets, whereas a peer does not.</span></span> <span data-ttu-id="226da-115">No entanto, os termos par, suplicante e cliente são amplamente sinônimos.</span><span class="sxs-lookup"><span data-stu-id="226da-115">Nonetheless, the terms peer, supplicant and client are largely synonymous.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="226da-116">O que é um autenticador?</span><span class="sxs-lookup"><span data-stu-id="226da-116">What is an authenticator?</span></span></td>
<td><span data-ttu-id="226da-117">O autenticador é o ponto de acesso sem fio, o NAS (servidor de acesso à rede) ou o NAD (dispositivo de acesso à rede) que autentica o suplicante.</span><span class="sxs-lookup"><span data-stu-id="226da-117">The authenticator is the wireless access point, network access server (NAS), or network access device (NAD) that authenticates the supplicant.</span></span> <span data-ttu-id="226da-118">O autenticador também é conhecido como o servidor EAP.</span><span class="sxs-lookup"><span data-stu-id="226da-118">The authenticator is also known as the EAP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="226da-119">Qual é o tempo de vida de uma autenticação?</span><span class="sxs-lookup"><span data-stu-id="226da-119">What is the lifetime of an authentication?</span></span></td>
<td><span data-ttu-id="226da-120">O tempo de vida de uma única sessão de autenticação no lado do cliente é tudo o que ocorre entre as funções [<strong>EapHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) e [<strong>EapHostPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerendsession) que estão sendo chamadas.</span><span class="sxs-lookup"><span data-stu-id="226da-120">The lifetime of a single authentication session on the client side is everything that occurs between the [<strong>EapHostPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) and [<strong>EapHostPeerEndSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) functions being called.</span></span> <span data-ttu-id="226da-121">O tempo de vida no lado do autenticador é tudo o que ocorre entre as funções [<strong>EapPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerbeginsession) e [<strong>EapPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerendsession).</span><span class="sxs-lookup"><span data-stu-id="226da-121">The lifetime on the authenticator side is everything that occurs between the [<strong>EapPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) and [<strong>EapPeerEndSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="226da-122">O que é um BLOB?</span><span class="sxs-lookup"><span data-stu-id="226da-122">What is a BLOB?</span></span> <span data-ttu-id="226da-123">Por que eu converteria um BLOB de configuração (binário) em XML?</span><span class="sxs-lookup"><span data-stu-id="226da-123">Why would I convert a configuration (binary) BLOB to XML?</span></span></td>
<td><span data-ttu-id="226da-124">Um BLOB é um objeto binário grande.</span><span class="sxs-lookup"><span data-stu-id="226da-124">A BLOB is a binary large object.</span></span> <span data-ttu-id="226da-125">O XML tem várias vantagens em relação a um BLOB de configuração binária.</span><span class="sxs-lookup"><span data-stu-id="226da-125">XML has several advantages over a binary configuration BLOB.</span></span> <span data-ttu-id="226da-126">Os dados de configuração armazenados em XML são legíveis, humanos-editable e de plataforma cruzada.</span><span class="sxs-lookup"><span data-stu-id="226da-126">Configuration data that is stored in XML is human-readable, human-editable, and cross-platform.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="226da-127">Quando converto um BLOB XML armazenado de volta em um BLOB binário?</span><span class="sxs-lookup"><span data-stu-id="226da-127">When do I convert a stored XML BLOB back to a binary BLOB?</span></span></td>
<td><span data-ttu-id="226da-128">É possível armazenar um blob binário ou BLOB XML, mas você sempre deve converter o BLOB XML de volta em um BLOB binário antes de usá-lo com APIs de tempo de execução; as APIs de tempo de execução não podem aceitar um diretório XML.</span><span class="sxs-lookup"><span data-stu-id="226da-128">It's possible to store a binary BLOB or XML BLOB, but you must always convert the XML BLOB back to a binary BLOB before use with run-time APIs; the run-time APIs cannot accept an XML directory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="226da-129">O que são métodos nativos?</span><span class="sxs-lookup"><span data-stu-id="226da-129">What are native methods?</span></span></td>
<td><span data-ttu-id="226da-130">Os métodos EAP nativos usam a nova API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="226da-130">Native EAP methods use the new EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="226da-131">O que são métodos herdados?</span><span class="sxs-lookup"><span data-stu-id="226da-131">What are legacy methods?</span></span></td>
<td><span data-ttu-id="226da-132">Os métodos EAP herdados são definidos na [referência do protocolo de autenticação extensível](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference).</span><span class="sxs-lookup"><span data-stu-id="226da-132">Legacy EAP methods are defined in the [Extensible Authentication Protocol Reference](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference).</span></span> <span data-ttu-id="226da-133">Os métodos EAP herdados estão disponíveis para uso no Windows Vista e no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="226da-133">The legacy EAP methods are available for use in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="226da-134">Esses métodos podem não estar disponíveis para uso em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="226da-134">These methods may not be available for use in subsequent versions of the operating system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="226da-135">Qual é a diferença entre os métodos herdados e nativos?</span><span class="sxs-lookup"><span data-stu-id="226da-135">What's the difference between legacy and native methods?</span></span></td>
<td><span data-ttu-id="226da-136">As APIs nativas são mais simples e têm menos recursos.</span><span class="sxs-lookup"><span data-stu-id="226da-136">The native APIs are simpler and have fewer features.</span></span> <span data-ttu-id="226da-137">Todos os novos métodos EAP devem ser escritos usando a API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="226da-137">All new EAP methods should be written using the EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="226da-138">O que é &quot; diretiva de grupo &quot; ?</span><span class="sxs-lookup"><span data-stu-id="226da-138">What is &quot;group policy&quot;?</span></span></td>
<td><span data-ttu-id="226da-139">Para obter uma descrição da diretiva de grupo, consulte [política de grupo coleção](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="226da-139">For a description of group policy, see [Group Policy Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="226da-140">As funções EAPHost podem substituir a política de configuração especificada pela política de grupo?</span><span class="sxs-lookup"><span data-stu-id="226da-140">Can EAPHost functions override configuration policy specified by group policy?</span></span></td>
<td><span data-ttu-id="226da-141">Não, nunca.</span><span class="sxs-lookup"><span data-stu-id="226da-141">No, never.</span></span> <span data-ttu-id="226da-142">Se a política de grupo estiver em uso, as configurações da política de grupo sempre substituirão as definições de configuração do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="226da-142">If group policy is in use, group policy settings will always override EAPHost configuration settings.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="226da-143">O que é SSO (logon único)?</span><span class="sxs-lookup"><span data-stu-id="226da-143">What is Single-Sign-On (SSO)?</span></span></td>
<td><span data-ttu-id="226da-144">[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) é um mecanismo de autenticação de camada 2.</span><span class="sxs-lookup"><span data-stu-id="226da-144">[802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) is a layer 2 authentication mechanism.</span></span> <span data-ttu-id="226da-145">Dependendo da configuração de SSO, o SSO permite que os usuários se autentiquem na rede usando a autenticação [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) antes ou imediatamente após o logon no Windows.</span><span class="sxs-lookup"><span data-stu-id="226da-145">Depending on the SSO configuration, SSO enables users to authenticate to the network using [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authentication before or immediately after logging on to Windows.</span></span> <span data-ttu-id="226da-146">O SSO pode ser configurado para usar credenciais do Windows para autenticação de rede (nesse caso, os usuários inserem suas credenciais apenas uma vez) ou usam credenciais diferentes para o Windows e a autenticação de rede.</span><span class="sxs-lookup"><span data-stu-id="226da-146">SSO can be configured to use Windows credentials for network authentication (in which case users enter their credentials only once) or use different credentials for Windows and network authentication.</span></span> <span data-ttu-id="226da-147">Para obter mais informações, consulte [SSO e PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="226da-147">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="226da-148">O que é provedor de acesso pré-logon (PLAP)</span><span class="sxs-lookup"><span data-stu-id="226da-148">What is Pre-Logon Access Provider (PLAP)</span></span></td>
<td><span data-ttu-id="226da-149">Para obter mais informações, consulte [SSO e PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="226da-149">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="226da-150">O que é PEAP (protocolo de autenticação extensível protegida)?</span><span class="sxs-lookup"><span data-stu-id="226da-150">What is Protected Extensible Authentication Protocol (PEAP)?</span></span></td>
<td><span data-ttu-id="226da-151">Para obter mais informações, consulte [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) e [sobre o protocolo de autenticação extensível](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</span><span class="sxs-lookup"><span data-stu-id="226da-151">For more information, see [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) and [About Extensible Authentication Protocol](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="226da-152">Como o PEAP lida com a retomada da sessão e a nova autenticação?</span><span class="sxs-lookup"><span data-stu-id="226da-152">How does PEAP deal with session resumption and re-authentication?</span></span></td>
<td><span data-ttu-id="226da-153">A retomada da sessão e a nova autenticação normalmente ocorrem durante o roaming em uma rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="226da-153">Session resumption and re-authentication typically occurs while roaming on a wireless network.</span></span> <span data-ttu-id="226da-154">A API de proteção de dados do Windows (DPAPI) fornece uma maneira de proteger e associar dados a um usuário e, opcionalmente, à sessão de logon.</span><span class="sxs-lookup"><span data-stu-id="226da-154">Windows Data Protection API (DPAPI) provides a way to protect and bind data to a user and optionally the logon session.</span></span> <span data-ttu-id="226da-155">O chamador dá ao [<strong>CryptProtectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptprotectmemory) um buffer não criptografado, e a DPAPI criptografará a memória no local.</span><span class="sxs-lookup"><span data-stu-id="226da-155">The caller gives [<strong>CryptProtectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory) an unencrypted buffer and DPAPI will encrypt the memory in place.</span></span> <span data-ttu-id="226da-156">Posteriormente, o chamador pode passar o buffer criptografado para [<strong>CryptUnprotectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptunprotectmemory) e a DPAPI descriptografará a memória, novamente no lugar.</span><span class="sxs-lookup"><span data-stu-id="226da-156">Later, the caller can pass in the encrypted buffer to [<strong>CryptUnprotectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory) and DPAPI will decrypt the memory, once again in place.</span></span> <span data-ttu-id="226da-157">Para obter mais informações, consulte [extensão de aplicativo interno TLS (TSL/ia)](https://go.microsoft.com/fwlink/p/?linkid=84011) e [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="226da-157">For more information, see [TLS Inner Application Extension (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) and [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="226da-158">O que é o EAP-TLS (segurança de nível EAP-Transport)?</span><span class="sxs-lookup"><span data-stu-id="226da-158">What is EAP-Transport Level Security (EAP-TLS)?</span></span></td>
<td><span data-ttu-id="226da-159">O EAP-TLS é um protocolo de cliente-servidor no qual os perfis de certificado distintos normalmente são usados para o cliente e o servidor. Para obter mais informações, consulte [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="226da-159">EAP-TLS is a client-server protocol in which distinct certificate profiles are typically used for the client and server.For more information, see [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="226da-160">Como fazer implementar uma alteração de senha usando a API da autoridade de segurança local (LSA)?</span><span class="sxs-lookup"><span data-stu-id="226da-160">How do I implement a password change using the Local Security Authority (LSA) API?</span></span></td>
<td><span data-ttu-id="226da-161">Use a função [<strong>LsaCallAuthenticationPackage</strong>] (/Windows/Desktop/API/ntsecapi/NF-ntsecapi-lsacallauthenticationpackage) para implementar uma alteração de senha.</span><span class="sxs-lookup"><span data-stu-id="226da-161">Use the [<strong>LsaCallAuthenticationPackage</strong>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) function to implement a password change.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="226da-162">Por que desejo habilitar o rastreamento no EAPHost?</span><span class="sxs-lookup"><span data-stu-id="226da-162">Why would I want to enable tracing in EAPHost?</span></span></td>
<td><span data-ttu-id="226da-163">Os logs de rastreamento contêm informações de depuração (disponíveis somente em inglês) que podem ajudar os desenvolvedores e parceiros da Microsoft a encontrar as causas raiz de quaisquer problemas com o processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="226da-163">The trace logs contain debugging information (available in English only) that may assist Microsoft developers and partners in finding the root causes of any issues being experienced with the authentication process.</span></span> <span data-ttu-id="226da-164">Para obter mais informações, consulte [habilitando o rastreamento](enabling-tracing.md).</span><span class="sxs-lookup"><span data-stu-id="226da-164">For more information, see [Enabling Tracing](enabling-tracing.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="226da-165">Por que encontro o código de erro, NTE_BAD_KEY_STATE (0x8009000BL) quando uso a API de [criptografia](/windows/desktop/SecCrypto/cryptography-portal) para entrar no Exchange EAP-TLS?</span><span class="sxs-lookup"><span data-stu-id="226da-165">Why do I encounter the error code, NTE_BAD_KEY_STATE (0x8009000BL) when I use the [Cryptography](/windows/desktop/SecCrypto/cryptography-portal) API to sign into the EAP-TLS exchange?</span></span></td>
<td><span data-ttu-id="226da-166">No Winerror. h NTE_BAD_KEY_STATE (0x8009000BL) é definido como uma &quot; chave não válida para uso no estado especificado &quot; .</span><span class="sxs-lookup"><span data-stu-id="226da-166">In Winerror.h NTE_BAD_KEY_STATE (0x8009000BL) is defined as a &quot;key not valid for use in specified state&quot;.</span></span> <span data-ttu-id="226da-167">Esse erro normalmente é retornado nos cenários a seguir.</span><span class="sxs-lookup"><span data-stu-id="226da-167">This error is typically returned in the following scenarios.</span></span>
<ul>
<li><span data-ttu-id="226da-168">Ao tentar exportar um BLOB de chave privada não exportável</span><span class="sxs-lookup"><span data-stu-id="226da-168">When attempting to export a non-exportable private key BLOB</span></span></li>
<li><span data-ttu-id="226da-169">Quando a tentativa de gerar um identificador de hash de uma função pseudo aleatória (PRF) não é bem-sucedida usando [<strong>CryptCreateHash</strong>] (/Windows/Desktop/API/WinCrypt/NF-WinCrypt-CryptCreateHash)</span><span class="sxs-lookup"><span data-stu-id="226da-169">When unsuccessfully attempting to generate a pseudo-random function (PRF) hash handle using [<strong>CryptCreateHash</strong>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash)</span></span></li>
</ul>
<span data-ttu-id="226da-170">Para obter mais informações, consulte [concluir mensagens no protocolo TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span><span class="sxs-lookup"><span data-stu-id="226da-170">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="226da-171">O que é uma função pseudo aleatória (PRF)?</span><span class="sxs-lookup"><span data-stu-id="226da-171">What is a pseudo-random function (PRF)?</span></span></td>
<td><span data-ttu-id="226da-172">Uma função que usa uma chave, rótulo e semente como entrada e produz uma saída de comprimento arbitrário.</span><span class="sxs-lookup"><span data-stu-id="226da-172">A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span> <span data-ttu-id="226da-173">Para obter mais informações, consulte [concluir mensagens no protocolo TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span><span class="sxs-lookup"><span data-stu-id="226da-173">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="226da-174">Como o EAPHost se associa a adaptadores de rede?</span><span class="sxs-lookup"><span data-stu-id="226da-174">How does EAPHost bind to network adapters?</span></span></td>
<td><span data-ttu-id="226da-175">O EAPHost permite que vários suplicantes operem simultaneamente, e cada suplicante pode se associar a vários adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="226da-175">EAPHost allows multiple supplicants to operate simultaneously, and each supplicant can bind to multiple network adapters.</span></span> <span data-ttu-id="226da-176">Os suplicantes do EAPHost fornecem associação às camadas de rede e orientam o processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="226da-176">EAPHost supplicants provide binding to the network layers and drive the authentication process.</span></span> <span data-ttu-id="226da-177">Os suplicantes contêm configuração de autenticação.</span><span class="sxs-lookup"><span data-stu-id="226da-177">Supplicants contain authentication configuration.</span></span> <span data-ttu-id="226da-178">Os suplicantes também salvam o estado e fornecem segurança de conexão subsequente.</span><span class="sxs-lookup"><span data-stu-id="226da-178">Supplicants also save the state and provide subsequent connection security.</span></span> <span data-ttu-id="226da-179">Como o EAPHost não se associa diretamente a nenhum mecanismo de rede, a extensibilidade do suplicante é possível.</span><span class="sxs-lookup"><span data-stu-id="226da-179">Because EAPHost doesn't directly bind to any network mechanism, supplicant extensibility is possible.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="226da-180">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="226da-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="226da-181">Perguntas frequentes do suplicante do EAPHost</span><span class="sxs-lookup"><span data-stu-id="226da-181">EAPHost Supplicant FAQs</span></span>](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="226da-182">FAQs do método EAPHost</span><span class="sxs-lookup"><span data-stu-id="226da-182">EAPHost Method FAQs</span></span>](eap-method-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="226da-183">Perguntas frequentes de desenvolvimento do EAPHost</span><span class="sxs-lookup"><span data-stu-id="226da-183">EAPHost Development FAQs</span></span>](eaphost-development-frequently-asked-questions.md)
</dt> </dl>


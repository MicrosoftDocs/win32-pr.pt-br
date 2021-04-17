---
title: Exemplos de camada de canal de segurança
description: Os exemplos a seguir ilustram a segurança na camada de canal.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- exemplos de segurança
- exemplos de segurança, instalação
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1283339b1a4af624e118e3f6c76a07449f9274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105773066"
---
# <a name="security-channel-layer-examples"></a><span data-ttu-id="5b117-107">Exemplos de camada de canal de segurança</span><span class="sxs-lookup"><span data-stu-id="5b117-107">Security Channel Layer Examples</span></span>

<span data-ttu-id="5b117-108">Os exemplos a seguir ilustram a segurança na [camada de canal](channel-layer-overview.md)</span><span class="sxs-lookup"><span data-stu-id="5b117-108">The following examples illustrate security in the [Channel Layer](channel-layer-overview.md)</span></span>

<span data-ttu-id="5b117-109">Segurança de transporte do Windows sobre TCP: cliente: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), servidor: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).</span><span class="sxs-lookup"><span data-stu-id="5b117-109">Windows transport security over TCP: Client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).</span></span>

<span data-ttu-id="5b117-110">Segurança de transporte do Windows em pipes nomeados: cliente: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), servidor: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).</span><span class="sxs-lookup"><span data-stu-id="5b117-110">Windows transport security over named pipes: Client: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Server: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).</span></span>

<span data-ttu-id="5b117-111">Segurança de transporte SSL: cliente: [HttpClientWithSslExample](httpclientwithsslexample.md), servidor: [HttpServerWithSslExample](httpserverwithsslexample.md).</span><span class="sxs-lookup"><span data-stu-id="5b117-111">SSL transport security: Client: [HttpClientWithSslExample](httpclientwithsslexample.md), Server: [HttpServerWithSslExample](httpserverwithsslexample.md).</span></span>

<span data-ttu-id="5b117-112">Nome de usuário sobre SSL de modo misto de segurança: cliente: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), servidor: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="5b117-112">Username over SSL mixed-mode security: Client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), Server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).</span></span>

<span data-ttu-id="5b117-113">Nome de usuário sobre SSL de modo misto de segurança: cliente: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), servidor: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="5b117-113">Username over SSL mixed-mode security: Client: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), Server: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).</span></span>

<span data-ttu-id="5b117-114">Nome de usuário sobre segurança de modo misto SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="5b117-114">Username over SSL mixed-mode security: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md).</span></span> <span data-ttu-id="5b117-115">Token emitido sobre segurança de modo misto SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="5b117-115">Issued token over SSL mixed-mode security: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md).</span></span> <span data-ttu-id="5b117-116">Certificado X509 sobre segurança de modo misto SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="5b117-116">X509 certificate over SSL mixed-mode security: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).</span></span>

## <a name="one-time-setup-for-security-samples"></a><span data-ttu-id="5b117-117">Configuração de One-Time para exemplos de segurança</span><span class="sxs-lookup"><span data-stu-id="5b117-117">One-Time Setup for Security Samples</span></span>

<span data-ttu-id="5b117-118">Para executar exemplos de segurança do WWSAPI, você precisa configurar os certificados de cliente e de servidor para SSL, bem como uma conta de usuário local para autenticação de cabeçalho HTTP.</span><span class="sxs-lookup"><span data-stu-id="5b117-118">To run WWSAPI security examples, you need to set up the client and server certificates for SSL, as well as a local user account for HTTP header authentication.</span></span> <span data-ttu-id="5b117-119">Antes de começar, você precisará das seguintes ferramentas:</span><span class="sxs-lookup"><span data-stu-id="5b117-119">Before you start, you need the following tools:</span></span>

-   <span data-ttu-id="5b117-120">MakeCert.exe (disponível no SDK do Windows 7).</span><span class="sxs-lookup"><span data-stu-id="5b117-120">MakeCert.exe (Available in the Windows 7 SDK.)</span></span>
-   <span data-ttu-id="5b117-121">CertUtil.exe ou CertMgr.exe (CertUtil.exe está disponível nos SDKs do Windows a partir do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5b117-121">CertUtil.exe or CertMgr.exe (CertUtil.exe is available in the Windows SDKs starting with Windows Server 2003.</span></span> <span data-ttu-id="5b117-122">CertMgr.exe está disponível no SDK do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5b117-122">CertMgr.exe is available in the Windows 7 SDK.</span></span> <span data-ttu-id="5b117-123">Você só precisa de uma dessas ferramentas.)</span><span class="sxs-lookup"><span data-stu-id="5b117-123">You only need one of these tools.)</span></span>
-   <span data-ttu-id="5b117-124">HttpCfg.exe: (você só precisará disso se estiver usando o Windows 2003 ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5b117-124">HttpCfg.exe: (You need this only if you are using Windows 2003 or Windows XP.</span></span> <span data-ttu-id="5b117-125">Essa ferramenta está disponível em ferramentas de suporte do Windows XP SP2 e também vem com o CD do Windows Server 2003 Resource Kit Tools.)</span><span class="sxs-lookup"><span data-stu-id="5b117-125">This tool is available in Windows XP SP2 Support Tools and also comes with the Windows Server 2003 Resource Kit Tools CD.)</span></span>

<span data-ttu-id="5b117-126">Se você receber os exemplos de WWSAPI instalando o SDK do Windows 7, poderá encontrar o MakeCert.exe e CertMgr.exe em% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ bin.</span><span class="sxs-lookup"><span data-stu-id="5b117-126">If you get the WWSAPI examples by installing the Windows 7 SDK, you can find the MakeCert.exe and CertMgr.exe under %ProgramFiles%\\Microsoft SDKs\\Windows\\v7.0\\bin.</span></span>

<span data-ttu-id="5b117-127">Execute a seguinte configuração de cinco etapas no prompt de comando (elevado se você estiver usando o Windows Vista e superior):</span><span class="sxs-lookup"><span data-stu-id="5b117-127">Perform the following five-step setup from the command prompt (elevated if you are using Windows Vista and above):</span></span>

1.  <span data-ttu-id="5b117-128">Gere um certificado autoassinado para ser a autoridade de certificação (CA) ou o emissor: **MakeCert.exe-SS root-Sr LocalMachine-n "CN = falsifique-Test-CA"-Cy Authority-r-SK "CAKeyContainer"**</span><span class="sxs-lookup"><span data-stu-id="5b117-128">Generate a self-signed certificate to be the certificate authority (CA) or issuer: **MakeCert.exe -ss Root -sr LocalMachine -n "CN=Fake-Test-CA" -cy authority -r -sk "CAKeyContainer"**</span></span>
2.  <span data-ttu-id="5b117-129">Gerar um certificado de servidor usando o certificado anterior como o emissor: **MakeCert.exe-SS My-Sr LocalMachine-n "CN = localhost"-céu Exchange-is root-ir LocalMachine-in falsificated-Test-CA-SK "ServerKeyContainer"**</span><span class="sxs-lookup"><span data-stu-id="5b117-129">Generate a server certificate using the previous certificate as the issuer: **MakeCert.exe -ss My -sr LocalMachine -n "CN=localhost" -sky exchange -is Root -ir LocalMachine -in Fake-Test-CA -sk "ServerKeyContainer"**</span></span>
3.  <span data-ttu-id="5b117-130">Localize a impressão digital (um hash de 40 caracteres SHA-1) do certificado do servidor executando qualquer um dos comandos a seguir e pesquise o certificado chamado localhost com o emissor falso-Test-CA:</span><span class="sxs-lookup"><span data-stu-id="5b117-130">Find the thumbprint (a 40-character SHA-1 hash) of the server certificate by running either of the following commands and search for the certificate named localhost with issuer Fake-Test-CA:</span></span>
    -   <span data-ttu-id="5b117-131">**CertUtil.exe-armazenar meu localhost**</span><span class="sxs-lookup"><span data-stu-id="5b117-131">**CertUtil.exe -store My localhost**</span></span>
    -   <span data-ttu-id="5b117-132">**CertMgr.exe-s-r LocalMachine My**</span><span class="sxs-lookup"><span data-stu-id="5b117-132">**CertMgr.exe -s -r LocalMachine My**</span></span>
4.  <span data-ttu-id="5b117-133">Registre a impressão digital do certificado do servidor? s sem espaços com HTTP.SYS:</span><span class="sxs-lookup"><span data-stu-id="5b117-133">Register the server certificate?s thumbprint with no spaces with HTTP.SYS:</span></span>
    -   <span data-ttu-id="5b117-134">No Windows Vista e superior (a opção "AppID" é um GUID arbitrário): **Netsh.exe http add sslcert IPPORT = 0.0.0.0:8443 AppID = {00112233-4455-6677-8899-AABBCCDDEEFF}** certhash =<40CharacterThumbprint></span><span class="sxs-lookup"><span data-stu-id="5b117-134">On Windows Vista and above (the "appid" option is an arbitrary GUID): **Netsh.exe http add sslcert ipport=0.0.0.0:8443 appid={00112233-4455-6677-8899-AABBCCDDEEFF}** certhash=<40CharacterThumbprint></span></span>
    -   <span data-ttu-id="5b117-135">No Windows XP ou 2003: **conjunto deHttpCfg.exe SSL-i 0.0.0.0:8443-h <40CharacterThumbprint>**</span><span class="sxs-lookup"><span data-stu-id="5b117-135">On Windows XP or 2003: **HttpCfg.exe set ssl -i 0.0.0.0:8443 -h <40CharacterThumbprint>**</span></span>
5.  <span data-ttu-id="5b117-136">Criar um usuário local: **net user "TestUserForBasicAuth" "TstPWD@ \* 4Bsic"/Add**</span><span class="sxs-lookup"><span data-stu-id="5b117-136">Create a local user: **Net user "TestUserForBasicAuth" "TstPWD@\*4Bsic" /add**</span></span>

<span data-ttu-id="5b117-137">Para limpar os certificados, a associação de certificado SSL e a conta de usuário criada nas etapas anteriores, execute os comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b117-137">To clean up the certificates, SSL certificate binding and the user account created in the previous steps, run the following commands.</span></span> <span data-ttu-id="5b117-138">Observe que, se houver vários certificados com o mesmo nome, CertMgr.exe precisarão de sua entrada antes de excluí-los.</span><span class="sxs-lookup"><span data-stu-id="5b117-138">Note if there are multiple certificates of the same name, CertMgr.exe will need your input before deleting them.</span></span>

-   <span data-ttu-id="5b117-139">**CertMgr.exe-del-c-n falsificado-Test-CA-s-r LocalMachine root**</span><span class="sxs-lookup"><span data-stu-id="5b117-139">**CertMgr.exe -del -c -n Fake-Test-CA -s -r LocalMachine Root**</span></span>
-   <span data-ttu-id="5b117-140">**CertMgr.exe-del-c-n localhost-s-r LocalMachine My**</span><span class="sxs-lookup"><span data-stu-id="5b117-140">**CertMgr.exe -del -c -n localhost -s -r LocalMachine My**</span></span>
-   <span data-ttu-id="5b117-141">**Netsh.exe http Delete SSLCERT IPPORT = 0.0.0.0:8443 (ou HttpCfg.exe Delete SSL-i 0.0.0.0:8443)**</span><span class="sxs-lookup"><span data-stu-id="5b117-141">**Netsh.exe http delete sslcert ipport=0.0.0.0:8443 (or HttpCfg.exe delete ssl -i 0.0.0.0:8443)**</span></span>
-   <span data-ttu-id="5b117-142">**Net user "TestUserForBasicAuth"/Delete**</span><span class="sxs-lookup"><span data-stu-id="5b117-142">**Net user "TestUserForBasicAuth" /delete**</span></span>

<span data-ttu-id="5b117-143">Verifique se há apenas um certificado raiz chamado falso-Test-CA.</span><span class="sxs-lookup"><span data-stu-id="5b117-143">Make sure there is only one root certificate named Fake-Test-CA.</span></span> <span data-ttu-id="5b117-144">Se você não tiver certeza, é sempre seguro tentar limpar esses certificados usando os comandos de limpeza acima (e ignorar erros) antes de iniciar a configuração de cinco etapas.</span><span class="sxs-lookup"><span data-stu-id="5b117-144">If you are unsure, it?s always safe to try to clean up these certificates using the cleanup commands above (and ignore errors) before starting the five-step setup.</span></span>

 

 





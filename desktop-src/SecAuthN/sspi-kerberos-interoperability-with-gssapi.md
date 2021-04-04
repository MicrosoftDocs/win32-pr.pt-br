---
description: Deve-se ter cuidado ao usar o SSP (provedor de suporte de segurança) do Kerberos se a interoperabilidade com GSSAPI for um requisito.
ms.assetid: 3ab29ee9-42d8-498b-b507-13f8efa0b0e2
title: Interoperabilidade de SSPI/Kerberos com GSSAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9efaae6b2433d76dff290d57e27e893885692a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646674"
---
# <a name="sspikerberos-interoperability-with-gssapi"></a><span data-ttu-id="15f6e-103">Interoperabilidade de SSPI/Kerberos com GSSAPI</span><span class="sxs-lookup"><span data-stu-id="15f6e-103">SSPI/Kerberos Interoperability with GSSAPI</span></span>

<span data-ttu-id="15f6e-104">Deve-se ter cuidado ao usar o SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) do [*Kerberos*](../secgloss/k-gly.md) se a interoperabilidade com GSSAPI for um requisito.</span><span class="sxs-lookup"><span data-stu-id="15f6e-104">Care must be taken when using the [*Kerberos*](../secgloss/k-gly.md) [*security support provider*](../secgloss/s-gly.md) (SSP) if interoperability with GSSAPI is a requirement.</span></span> <span data-ttu-id="15f6e-105">As convenções de código a seguir permitem a interoperabilidade com aplicativos baseados em GSSAPI:</span><span class="sxs-lookup"><span data-stu-id="15f6e-105">The following code conventions allow interoperability with GSSAPI-based applications:</span></span>

-   [<span data-ttu-id="15f6e-106">Nomes compatíveis com o Windows</span><span class="sxs-lookup"><span data-stu-id="15f6e-106">Windows-Compatible Names</span></span>](#windows-compatible-names)
-   [<span data-ttu-id="15f6e-107">Autenticação</span><span class="sxs-lookup"><span data-stu-id="15f6e-107">Authentication</span></span>](#authentication)
-   [<span data-ttu-id="15f6e-108">Integridade e privacidade da mensagem</span><span class="sxs-lookup"><span data-stu-id="15f6e-108">Message Integrity and Privacy</span></span>](#message-integrity-and-privacy)

<span data-ttu-id="15f6e-109">Você pode encontrar o código de exemplo no SDK (Kit de desenvolvimento de software) da plataforma em amostras \\ segurança \\ SSPI \\ GSS.</span><span class="sxs-lookup"><span data-stu-id="15f6e-109">You can find sample code in the Platform Software Development Kit (SDK) under Samples\\Security\\SSPI\\GSS.</span></span> <span data-ttu-id="15f6e-110">Além disso, o exemplo equivalente em UNIX é distribuído nas distribuições Kerberos MIT e Heimdal, GSS Client e Server.</span><span class="sxs-lookup"><span data-stu-id="15f6e-110">In addition, the equivalent UNIX sample is distributed in the MIT and Heimdal Kerberos distributions, GSS client and server.</span></span>

## <a name="windows-compatible-names"></a><span data-ttu-id="15f6e-111">Nomes de Windows-Compatible</span><span class="sxs-lookup"><span data-stu-id="15f6e-111">Windows-Compatible Names</span></span>

<span data-ttu-id="15f6e-112">As funções GSSAPI usam um formato de nome conhecido como GSS \_ NT \_ \_ Name, conforme especificado na RFC.</span><span class="sxs-lookup"><span data-stu-id="15f6e-112">GSSAPI functions use a name format known as gss\_nt\_service\_name as specified in the RFC.</span></span> <span data-ttu-id="15f6e-113">Por exemplo, sample@host.dom.com é um nome que pode ser usado em um aplicativo baseado em GSSAPI.</span><span class="sxs-lookup"><span data-stu-id="15f6e-113">For example, sample@host.dom.com is a name that can be used in a GSSAPI-based application.</span></span> <span data-ttu-id="15f6e-114">O sistema operacional Windows não reconhece o formato de \_ nome do serviço GSS NT \_ \_ e o [*nome da entidade de serviço*](../secgloss/s-gly.md)completo, por exemplo sample/host.dom.com@REALM , deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="15f6e-114">The Windows operating system does not recognize the gss\_nt\_service\_name format, and the full [*service principal name*](../secgloss/s-gly.md), for example sample/host.dom.com@REALM, must be used.</span></span>

## <a name="authentication"></a><span data-ttu-id="15f6e-115">Autenticação</span><span class="sxs-lookup"><span data-stu-id="15f6e-115">Authentication</span></span>

<span data-ttu-id="15f6e-116">A autenticação é normalmente tratada quando uma conexão é configurada pela primeira vez entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="15f6e-116">Authentication is usually handled when a connection is first set up between a client and a server.</span></span> <span data-ttu-id="15f6e-117">Neste exemplo, o cliente está usando a [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) (SSPI) e o servidor está usando GSSAPI.</span><span class="sxs-lookup"><span data-stu-id="15f6e-117">In this sample, the client is using [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) and the server is using GSSAPI.</span></span>

<span data-ttu-id="15f6e-118">**Para configurar a autenticação no cliente SSPI**</span><span class="sxs-lookup"><span data-stu-id="15f6e-118">**To set up authentication in the SSPI client**</span></span>

1.  <span data-ttu-id="15f6e-119">Obter [*credenciais*](../secgloss/c-gly.md) de saída usando [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span><span class="sxs-lookup"><span data-stu-id="15f6e-119">Get outbound [*credentials*](../secgloss/c-gly.md) by using [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span></span>
2.  <span data-ttu-id="15f6e-120">Crie um nome de serviço com o **nome de importação de GSS \_ \_ ()** e obtenha credenciais de entrada usando **GSS \_ adquirir \_ credenciais**.</span><span class="sxs-lookup"><span data-stu-id="15f6e-120">Create a service name with **gss\_import\_name()** and get inbound credentials by using **gss\_acquire\_cred**.</span></span>
3.  <span data-ttu-id="15f6e-121">Obtenha um token de autenticação para enviar ao servidor usando o [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="15f6e-121">Get an authentication token to send to the server by using [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
4.  <span data-ttu-id="15f6e-122">Envie o token para o servidor.</span><span class="sxs-lookup"><span data-stu-id="15f6e-122">Send the token to the server.</span></span>

<span data-ttu-id="15f6e-123">**Para configurar a autenticação no servidor GSSAPI**</span><span class="sxs-lookup"><span data-stu-id="15f6e-123">**To set up authentication in the GSSAPI server**</span></span>

1.  <span data-ttu-id="15f6e-124">Analise a mensagem do cliente para extrair o token de segurança.</span><span class="sxs-lookup"><span data-stu-id="15f6e-124">Parse the message from the client to extract the security token.</span></span> <span data-ttu-id="15f6e-125">Use a função de **\_ \_ \_ contexto GSS Accept s** , passando o token como um argumento.</span><span class="sxs-lookup"><span data-stu-id="15f6e-125">Use the **gss\_accept\_sec\_context** function, passing the token as an argument.</span></span>
2.  <span data-ttu-id="15f6e-126">Analise a mensagem do servidor para extrair o token de segurança.</span><span class="sxs-lookup"><span data-stu-id="15f6e-126">Parse the message from the server to extract the security token.</span></span> <span data-ttu-id="15f6e-127">Passe este token de segurança para [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="15f6e-127">Pass this security token to [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
3.  <span data-ttu-id="15f6e-128">Envie um token de resposta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="15f6e-128">Send a response token to the client.</span></span>

    <span data-ttu-id="15f6e-129">A função de **\_ \_ \_ contexto GSS Accept s** pode retornar um token que você pode enviar de volta para o cliente.</span><span class="sxs-lookup"><span data-stu-id="15f6e-129">The **gss\_accept\_sec\_context** function can return a token that you can send back to the client.</span></span>

4.  <span data-ttu-id="15f6e-130">Se for necessário continuar, envie um token de resposta para o servidor; caso contrário, a configuração da autenticação será concluída.</span><span class="sxs-lookup"><span data-stu-id="15f6e-130">If it is necessary to continue, send a response token to the server; otherwise, the setup of authentication is complete.</span></span>
5.  <span data-ttu-id="15f6e-131">Se for necessário continuar, aguarde o próximo token do cliente; caso contrário, a configuração da autenticação será concluída.</span><span class="sxs-lookup"><span data-stu-id="15f6e-131">If it is necessary to continue, wait for the next token from the client; otherwise, the setup of authentication is complete.</span></span>

## <a name="message-integrity-and-privacy"></a><span data-ttu-id="15f6e-132">Integridade e privacidade da mensagem</span><span class="sxs-lookup"><span data-stu-id="15f6e-132">Message Integrity and Privacy</span></span>

<span data-ttu-id="15f6e-133">A maioria dos aplicativos baseados em GSSAPI usa a função **GSS \_ Wrap** para assinar uma mensagem antes de enviá-la.</span><span class="sxs-lookup"><span data-stu-id="15f6e-133">Most GSSAPI-based applications use the **GSS\_Wrap** function to sign a message before sending it.</span></span> <span data-ttu-id="15f6e-134">Por outro lado, a função de **\_ desencapsulamento GSS** verifica a assinatura.</span><span class="sxs-lookup"><span data-stu-id="15f6e-134">Conversely, the **GSS\_Unwrap** function verifies the signature.</span></span> <span data-ttu-id="15f6e-135">**GSS \_ O encapsulamento** está disponível na versão 2,0 da API e agora é amplamente usado e especificado em padrões da Internet que descrevem o uso do GSSAPI para adicionar segurança aos protocolos.</span><span class="sxs-lookup"><span data-stu-id="15f6e-135">**GSS\_Wrap** is available in version 2.0 of the API and is now widely used and specified in Internet standards that describe using the GSSAPI for adding security to protocols.</span></span> <span data-ttu-id="15f6e-136">Anteriormente, as funções GSS **SignMessage** e **SealMessage** eram usadas para a [*integridade*](../secgloss/i-gly.md) e a [*privacidade*](../secgloss/p-gly.md)da mensagem.</span><span class="sxs-lookup"><span data-stu-id="15f6e-136">Earlier, the GSS **SignMessage** and **SealMessage** functions were used for message [*integrity*](../secgloss/i-gly.md) and [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="15f6e-137">**GSS \_ Encapsular** e **GSS \_ Unwrap** são usados para integridade e privacidade com o uso de privacidade controlado pelo valor do argumento "conf \_ Flag".</span><span class="sxs-lookup"><span data-stu-id="15f6e-137">**GSS\_Wrap** and **GSS\_Unwrap** are used for both integrity and privacy with the use of privacy controlled by the value of the "conf\_flag" argument.</span></span>

<span data-ttu-id="15f6e-138">Se um protocolo baseado em GSSAPI for especificado para usar as **funções GSS \_ Get \_ MIC** e **GSS \_ Verify \_ MIC** , as funções SSPI corretas seriam [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature).</span><span class="sxs-lookup"><span data-stu-id="15f6e-138">If a GSSAPI-based protocol is specified to use the **gss\_get\_mic** and **gss\_verify\_mic** functions, the correct SSPI functions would be [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature).</span></span> <span data-ttu-id="15f6e-139">Lembre-se de que **MakeSignature** e **VerifySignature** não interoperarão com **GSS \_ Wrap** quando o \_ sinalizador conf estiver definido como zero ou com **GSS \_ Wrap**.</span><span class="sxs-lookup"><span data-stu-id="15f6e-139">Be aware that **MakeSignature** and **VerifySignature** will not interoperate with **GSS\_Wrap** when conf\_flag is set to zero, or with **GSS\_Wrap**.</span></span> <span data-ttu-id="15f6e-140">O mesmo vale para misturar [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) definido somente para assinatura e **GSS \_ verificar \_ MIC**.</span><span class="sxs-lookup"><span data-stu-id="15f6e-140">The same is true for mixing [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) set for signature only and **gss\_verify\_mic**.</span></span>

> [!Note]  
> <span data-ttu-id="15f6e-141">Não use as funções [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) ou [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) quando o **GSS \_ Wrap** e **o \_ desencapsulamento de GSS** forem chamados para.</span><span class="sxs-lookup"><span data-stu-id="15f6e-141">Do not use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) or [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions when **GSS\_Wrap** and **GSS\_Unwrap** are called for.</span></span>

 

<span data-ttu-id="15f6e-142">O equivalente de SSPI a **GSS \_ Wrap** é [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) para integridade e privacidade.</span><span class="sxs-lookup"><span data-stu-id="15f6e-142">The SSPI equivalent to **GSS\_Wrap** is [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) for both integrity and privacy.</span></span>

<span data-ttu-id="15f6e-143">O exemplo a seguir mostra o uso de [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) para assinar dados que serão verificados pelo **GSS \_ desencapsulado**.</span><span class="sxs-lookup"><span data-stu-id="15f6e-143">The following example shows using [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) to sign data that will be verified by **GSS\_Unwrap**.</span></span>

<span data-ttu-id="15f6e-144">No cliente SSPI:</span><span class="sxs-lookup"><span data-stu-id="15f6e-144">In the SSPI client:</span></span>


```C++
// Need three descriptors, two for the SSP and
// one to hold the application data. 
in_buf_desc.cBuffers = 3;
in_buf_desc.pBuffers = wrap_bufs;
in_buf_desc.ulVersion = SECBUFFER_VERSION;
wrap_bufs[0].cbBuffer = sizes.cbSecurityTrailer;
wrap_bufs[0].BufferType = SECBUFFER_TOKEN;
wrap_bufs[0].pvBuffer = malloc(sizes.cbSecurityTrailer);

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = in_buf.cbBuffer;
wrap_bufs[1].pvBuffer = malloc(wrap_bufs[1].cbBuffer);
memcpy(wrap_bufs[1].pvBuffer, in_buf.pvBuffer, in_buf.cbBuffer);
wrap_bufs[2].BufferType = SECBUFFER_PADDING;
wrap_bufs[2].cbBuffer = sizes.cbBlockSize;
wrap_bufs[2].pvBuffer = malloc(wrap_bufs[2].cbBuffer);
maj_stat = EncryptMessage(&context,
SignOnly ? KERB_WRAP_NO_ENCRYPT : 0,
&in_buf_desc, 0);

// Send a message to the server.
```



<span data-ttu-id="15f6e-145">No servidor GSSAPI:</span><span class="sxs-lookup"><span data-stu-id="15f6e-145">In the GSSAPI server:</span></span>


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



<span data-ttu-id="15f6e-146">O equivalente SSPI a **GSS \_ desencapsulado** é [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span><span class="sxs-lookup"><span data-stu-id="15f6e-146">The SSPI equivalent to **GSS\_Unwrap** is [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span> <span data-ttu-id="15f6e-147">Aqui está um exemplo que mostra como usar **DecryptMessage (Kerberos)** para descriptografar dados que foram criptografados por **GSS \_ Wrap**.</span><span class="sxs-lookup"><span data-stu-id="15f6e-147">Here is an example that shows how to use **DecryptMessage (Kerberos)** to decrypt data that was encrypted by **GSS\_Wrap**.</span></span>

<span data-ttu-id="15f6e-148">No servidor GSSAPI:</span><span class="sxs-lookup"><span data-stu-id="15f6e-148">In the GSSAPI server:</span></span>


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



<span data-ttu-id="15f6e-149">No cliente SSPI:</span><span class="sxs-lookup"><span data-stu-id="15f6e-149">In the SSPI client:</span></span>


```C++
wrap_buf_desc.cBuffers = 2;
wrap_buf_desc.pBuffers = wrap_bufs;
wrap_buf_desc.ulVersion = SECBUFFER_VERSION; 

// This buffer is for SSPI.
wrap_bufs[0].BufferType = SECBUFFER_STREAM;
wrap_bufs[0].pvBuffer = xmit_buf.pvBuffer;
wrap_bufs[0].cbBuffer = xmit_buf.cbBuffer;

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = 0;
wrap_bufs[1].pvBuffer = NULL;
maj_stat = DecryptMessage(
&context,
&wrap_buf_desc,
0, // no sequence number
&qop
);

// This is where the data is.
msg_buf = wrap_bufs[1];

// Check QOP of received message.
// If QOP is KERB_WRAP_NO_ENCRYPT, the message is signed only; 
// otherwise, it is encrypted.
```



 

 

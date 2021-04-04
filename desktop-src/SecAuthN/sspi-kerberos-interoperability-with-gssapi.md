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
# <a name="sspikerberos-interoperability-with-gssapi"></a>Interoperabilidade de SSPI/Kerberos com GSSAPI

Deve-se ter cuidado ao usar o SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) do [*Kerberos*](../secgloss/k-gly.md) se a interoperabilidade com GSSAPI for um requisito. As convenções de código a seguir permitem a interoperabilidade com aplicativos baseados em GSSAPI:

-   [Nomes compatíveis com o Windows](#windows-compatible-names)
-   [Autenticação](#authentication)
-   [Integridade e privacidade da mensagem](#message-integrity-and-privacy)

Você pode encontrar o código de exemplo no SDK (Kit de desenvolvimento de software) da plataforma em amostras \\ segurança \\ SSPI \\ GSS. Além disso, o exemplo equivalente em UNIX é distribuído nas distribuições Kerberos MIT e Heimdal, GSS Client e Server.

## <a name="windows-compatible-names"></a>Nomes de Windows-Compatible

As funções GSSAPI usam um formato de nome conhecido como GSS \_ NT \_ \_ Name, conforme especificado na RFC. Por exemplo, sample@host.dom.com é um nome que pode ser usado em um aplicativo baseado em GSSAPI. O sistema operacional Windows não reconhece o formato de \_ nome do serviço GSS NT \_ \_ e o [*nome da entidade de serviço*](../secgloss/s-gly.md)completo, por exemplo sample/host.dom.com@REALM , deve ser usado.

## <a name="authentication"></a>Autenticação

A autenticação é normalmente tratada quando uma conexão é configurada pela primeira vez entre um cliente e um servidor. Neste exemplo, o cliente está usando a [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) (SSPI) e o servidor está usando GSSAPI.

**Para configurar a autenticação no cliente SSPI**

1.  Obter [*credenciais*](../secgloss/c-gly.md) de saída usando [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).
2.  Crie um nome de serviço com o **nome de importação de GSS \_ \_ ()** e obtenha credenciais de entrada usando **GSS \_ adquirir \_ credenciais**.
3.  Obtenha um token de autenticação para enviar ao servidor usando o [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
4.  Envie o token para o servidor.

**Para configurar a autenticação no servidor GSSAPI**

1.  Analise a mensagem do cliente para extrair o token de segurança. Use a função de **\_ \_ \_ contexto GSS Accept s** , passando o token como um argumento.
2.  Analise a mensagem do servidor para extrair o token de segurança. Passe este token de segurança para [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
3.  Envie um token de resposta para o cliente.

    A função de **\_ \_ \_ contexto GSS Accept s** pode retornar um token que você pode enviar de volta para o cliente.

4.  Se for necessário continuar, envie um token de resposta para o servidor; caso contrário, a configuração da autenticação será concluída.
5.  Se for necessário continuar, aguarde o próximo token do cliente; caso contrário, a configuração da autenticação será concluída.

## <a name="message-integrity-and-privacy"></a>Integridade e privacidade da mensagem

A maioria dos aplicativos baseados em GSSAPI usa a função **GSS \_ Wrap** para assinar uma mensagem antes de enviá-la. Por outro lado, a função de **\_ desencapsulamento GSS** verifica a assinatura. **GSS \_ O encapsulamento** está disponível na versão 2,0 da API e agora é amplamente usado e especificado em padrões da Internet que descrevem o uso do GSSAPI para adicionar segurança aos protocolos. Anteriormente, as funções GSS **SignMessage** e **SealMessage** eram usadas para a [*integridade*](../secgloss/i-gly.md) e a [*privacidade*](../secgloss/p-gly.md)da mensagem. **GSS \_ Encapsular** e **GSS \_ Unwrap** são usados para integridade e privacidade com o uso de privacidade controlado pelo valor do argumento "conf \_ Flag".

Se um protocolo baseado em GSSAPI for especificado para usar as **funções GSS \_ Get \_ MIC** e **GSS \_ Verify \_ MIC** , as funções SSPI corretas seriam [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature). Lembre-se de que **MakeSignature** e **VerifySignature** não interoperarão com **GSS \_ Wrap** quando o \_ sinalizador conf estiver definido como zero ou com **GSS \_ Wrap**. O mesmo vale para misturar [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) definido somente para assinatura e **GSS \_ verificar \_ MIC**.

> [!Note]  
> Não use as funções [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) ou [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) quando o **GSS \_ Wrap** e **o \_ desencapsulamento de GSS** forem chamados para.

 

O equivalente de SSPI a **GSS \_ Wrap** é [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) para integridade e privacidade.

O exemplo a seguir mostra o uso de [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) para assinar dados que serão verificados pelo **GSS \_ desencapsulado**.

No cliente SSPI:


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



No servidor GSSAPI:


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



O equivalente SSPI a **GSS \_ desencapsulado** é [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage). Aqui está um exemplo que mostra como usar **DecryptMessage (Kerberos)** para descriptografar dados que foram criptografados por **GSS \_ Wrap**.

No servidor GSSAPI:


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



No cliente SSPI:


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



 

 

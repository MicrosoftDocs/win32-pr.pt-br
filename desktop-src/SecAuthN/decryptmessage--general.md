---
description: Descriptografa uma mensagem.
ms.assetid: ea271d0c-9167-41c5-8919-09611206fc71
title: Função DecryptMessage (geral) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: a05906c721d9046920c465fdfdf6b1c790b06640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164699"
---
# <a name="decryptmessage-general-function"></a>Função DecryptMessage (geral)

A função **DecryptMessage (geral)** descriptografa uma mensagem. Alguns pacotes não criptografam e descriptografam mensagens, mas executam e verificam um [*hash*](../secgloss/h-gly.md)de integridade.

O SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) Digest fornece criptografia e confidencialidade para mensagens trocadas entre o cliente e o servidor como um mecanismo SASL apenas.

Essa função também é usada com o SSP do Schannel para sinalizar uma solicitação de um remetente de mensagem para uma renegociação (refazer) dos atributos de conexão ou para um desligamento da conexão.

> [!Note]  
> [**EncryptMessage (geral)**](encryptmessage--general.md) e **DecryptMessage (geral)** podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ) se um thread estiver Criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

 

Para obter informações sobre como usar essa função com um SSP específico, consulte os tópicos a seguir.



| Tópico                                                            | Descrição                            |
|------------------------------------------------------------------|----------------------------------------|
| [**DecryptMessage (resumo)**](decryptmessage--digest.md)       | Descriptografa uma mensagem usando Digest.    |
| [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)   | Descriptografa uma mensagem usando o Kerberos.  |
| [**DecryptMessage (negociar)**](decryptmessage--negotiate.md) | Descriptografa uma mensagem usando Negotiate. |
| [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md)           | Descriptografa uma mensagem usando NTLM.      |
| [**DecryptMessage (Schannel)**](decryptmessage--schannel.md)   | Descriptografa uma mensagem usando Schannel.  |



 

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phContext* \[ no\]
</dt> <dd>

Um identificador para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para descriptografar a mensagem.

</dd> <dt>

*PMessage* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Um deles pode ser do tipo dados SECBUFFER \_ . Esse buffer contém a mensagem criptografada. A mensagem criptografada é descriptografada no local, substituindo o conteúdo original de seu buffer.

Ao usar o SSP de resumo, na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Um deles deve ser do tipo SECBUFFER \_ data ou SECBUFFER \_ Stream e deve conter a mensagem criptografada.

Ao usar o SSP do Schannel com contextos que não são orientados a conexão, na entrada, a estrutura deve conter quatro estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Exatamente um buffer deve ser do tipo \_ dados SECBUFFER e conter uma mensagem criptografada, que é descriptografada no local. Os buffers restantes são usados para saída e devem ser do tipo SECBUFFER \_ vazio. Para contextos orientados a conexão, um \_ buffer de tipo de dados SECBUFFER deve ser fornecido, conforme observado para contextos não orientados para conexão. Além disso, um segundo \_ buffer de tipo de token SECBUFFER que contém um token de segurança também deve ser fornecido.

</dd> <dt>

*MessageSeqNo* \[ no\]
</dt> <dd>

O número de sequência esperado pelo aplicativo de transporte, se houver. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser definido como zero.

Ao usar o SSP de resumo, esse parâmetro deve ser definido como zero. O SSP de resumo gerencia a numeração de sequência internamente.

Ao usar o SSP do Schannel, esse parâmetro deve ser definido como zero. O SSP do Schannel não usa números de sequência.

</dd> <dt>

*pfQOP* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável do tipo **ULONG** que recebe sinalizadores específicos do pacote que indicam a qualidade da proteção.

Ao usar o SSP do Schannel, esse parâmetro não é usado e deve ser definido como **nulo**.

Esse parâmetro pode ser um dos sinalizadores a seguir.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valor</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>A mensagem não foi criptografada, mas um cabeçalho ou trailer foi produzido.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</blockquote><br/></td></tr><tr class="even"><td><span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl> <dt><strong>SIGN_ONLY</strong></dt> </dl></td><td>Ao usar o SSP de resumo, use esse sinalizador quando o [*contexto de segurança*](../secgloss/s-gly.md) for definido para verificar apenas a [*assinatura*](../secgloss/s-gly.md) . Para obter mais informações, consulte [qualidade de proteção](quality-of-protection.md).<br/></td></tr></tbody></table>



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função verificar que a mensagem foi recebida na sequência correta, a função retornará s \_ E \_ OK.

Se a função falhar ao descriptografar a mensagem, ela retornará um dos seguintes códigos de erro.



| Código de retorno                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ buffer \_ muito \_ pequeno**</dt> </dl>      | O buffer de mensagens é muito pequeno. Usado com o SSP de resumo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**s \_ E \_ sistema de criptografia \_ \_ inválidos**</dt> </dl> | Não há suporte para a [*codificação*](../secgloss/c-gly.md) escolhida para o [*contexto de segurança*](../secgloss/s-gly.md) . Usado com o SSP de resumo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**s \_ E \_ mensagem incompleta \_**</dt> </dl>     | Os dados no buffer de entrada estão incompletos. O aplicativo precisa ler mais dados do servidor e chamar [**DecryptMessage (geral)**](decryptmessage--general.md) novamente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**s \_ E \_ \_ identificador inválido**</dt> </dl>         | Um identificador de contexto inválido foi especificado no parâmetro *phContext* . Usado com os SSPs Digest e Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**s \_ E \_ \_ token inválido**</dt> </dl>          | Os buffers são do tipo incorreto ou nenhum buffer do tipo dados de SECBUFFER \_ foi encontrado. Usado com o SSP do Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**s \_ E \_ mensagem \_ alterada**</dt> </dl>        | A mensagem foi alterada. Usado com os SSPs Digest e Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**s \_ E \_ fora \_ de \_ sequência**</dt> </dl>       | A mensagem não foi recebida na sequência correta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**s \_ E \_ QOP \_ não \_ têm suporte**</dt> </dl>     | Nenhuma confidencialidade nem [*integridade*](../secgloss/i-gly.md) têm suporte no [*contexto de segurança*](../secgloss/s-gly.md). Usado com o SSP de resumo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**s \_ I \_ contexto \_ expirado**</dt> </dl>        | O remetente da mensagem concluiu o uso da conexão e iniciou um desligamento. Para obter informações sobre como iniciar ou reconhecer um desligamento, consulte [desligar uma conexão Schannel](shutting-down-an-schannel-connection.md). Usado com o SSP do Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**s \_ \_ renegociar**</dt> </dl>             | A parte remota requer uma nova sequência de handshake ou o aplicativo acabou de iniciar um desligamento. Retorne ao loop de negociação e chame [**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md) ou [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md), passando buffers de entrada vazios. <br/> Se a função retornar um buffer de buffer de tipo **s \_ \_ extra**, isso deve ser passado para a função [**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md) como um buffer de entrada.<br/> Usado com o SSP do Schannel.<br/> Não há suporte para a renegociação no modo kernel Schannel. O chamador deve ignorar esse valor de retorno ou desligar a conexão. Se o valor for ignorado, o cliente ou o servidor poderá desligar a conexão como resultado.<br/> |



 

## <a name="remarks"></a>Comentários

Quando você usa o Schannel SSP, a função **DecryptMessage (geral)** retorna um \_ \_ contexto de s I \_ expirou quando o remetente da mensagem desligou a conexão. Para obter informações sobre como iniciar ou reconhecer um desligamento, consulte [desligar uma conexão Schannel](shutting-down-an-schannel-connection.md).

Quando você usa o SSP do Schannel, **DecryptMessage (geral)** retorna \_ s \_ renegotiate quando o remetente da mensagem deseja renegociar a conexão ([*contexto de segurança*](../secgloss/s-gly.md)). Um aplicativo manipula uma renegociação solicitada chamando [**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md) (lado do servidor) ou [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md) (lado do cliente) e passando buffers de entrada vazios. Depois que essa chamada inicial retorna um valor, continue como se seu aplicativo estivesse criando uma nova conexão. Para obter mais informações, consulte [criando um [*contexto de segurança*](../secgloss/s-gly.md)Schannel](creating-an-schannel-security-context.md).

Para obter informações sobre a interoperação com o GSSAPI, consulte [interoperabilidade entre SSPI/Kerberos com GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**EncryptMessage (geral)**](encryptmessage--general.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 

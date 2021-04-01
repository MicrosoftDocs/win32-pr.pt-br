---
description: Descriptografa uma mensagem usando Schannel.
ms.assetid: 5d7c8598-2d6b-4839-ae98-dff964bc962c
title: Função DecryptMessage (Schannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 6bfbb354be9f3553e5369b8ce1f8b4260eab8ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646785"
---
# <a name="decryptmessage-schannel-function"></a>Função DecryptMessage (Schannel)

A função **DecryptMessage (Schannel)** descriptografa uma mensagem. Alguns pacotes não criptografam e descriptografam mensagens, mas executam e verificam um [*hash*](../secgloss/h-gly.md)de integridade.


Essa função também é usada com o SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY) Schannel) para sinalizar uma solicitação de um remetente de mensagem para uma renegociação (refazer) dos atributos de conexão ou para um desligamento da conexão.

> [!Note]  
> [**EncryptMessage (Schannel)**](encryptmessage--schannel.md) e **DecryptMessage (Schannel)** podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY) ), se um thread estiver Criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.


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

*phContext* \[ no\]


Um identificador para o [*contexto de segurança*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) a ser usado para descriptografar a mensagem.

*PMessage* \[ entrada, saída\]

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Um deles pode ser do tipo dados SECBUFFER \_ . Esse buffer contém a mensagem criptografada. A mensagem criptografada é descriptografada no local, substituindo o conteúdo original de seu buffer.

Ao usar o SSP do Schannel com contextos que não são orientados a conexão, na entrada, a estrutura deve conter quatro estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Exatamente um buffer deve ser do tipo \_ dados SECBUFFER e conter uma mensagem criptografada, que é descriptografada no local. Os buffers restantes são usados para saída e devem ser do tipo SECBUFFER \_ vazio. Para contextos orientados a conexão, um \_ buffer de tipo de dados SECBUFFER deve ser fornecido, conforme observado para contextos não orientados para conexão. Além disso, um segundo \_ buffer de tipo de token SECBUFFER que contém um token de segurança também deve ser fornecido.

*MessageSeqNo* \[ no\]

O número de sequência esperado pelo aplicativo de transporte, se houver. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser definido como zero.

Ao usar o SSP do Schannel, esse parâmetro deve ser definido como zero. O SSP do Schannel não usa números de sequência.

*pfQOP* \[ fora\]

Um ponteiro para uma variável do tipo **ULONG** que recebe sinalizadores específicos do pacote que indicam a qualidade da proteção.

Ao usar o SSP do Schannel, esse parâmetro não é usado e deve ser definido como **nulo**.

Esse parâmetro pode ser o sinalizador a seguir.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valor</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>A mensagem não foi criptografada, mas um cabeçalho ou trailer foi produzido.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Retornar valor

Se a função verificar que a mensagem foi recebida na sequência correta, a função retornará s \_ E \_ OK.

Se a função falhar ao descriptografar a mensagem, ela retornará um dos seguintes códigos de erro.

| Código de retorno                     | Descrição                                                                                                    |
|---------------------------------|----------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ \_ identificador inválido**     | Um identificador de contexto inválido foi especificado no parâmetro *phContext* . Usado com o SSP do Schannel.     |
| **s \_ E \_ \_ token inválido**      | Os buffers são do tipo incorreto ou nenhum buffer do tipo dados de SECBUFFER \_ foi encontrado. Usado com o SSP do Schannel.  |
| **s \_ E \_ mensagem \_ alterada**    | A mensagem foi alterada. Usado com o SSP do Schannel.                                                      |
| **s \_ E \_ fora \_ de \_ sequência**   | A mensagem não foi recebida na sequência correta.                                                          |
| **s \_ I \_ contexto \_ expirado**    | O remetente da mensagem concluiu o uso da conexão e iniciou um desligamento. Para obter informações sobre como iniciar ou reconhecer um desligamento, consulte [desligar uma conexão Schannel](shutting-down-an-schannel-connection.md). Usado com o SSP do Schannel. |
| **s \_ \_ renegociar**         | A parte remota requer uma nova sequência de handshake ou o aplicativo acabou de iniciar um desligamento. Retorne ao loop de negociação e chame [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) ou [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md), passe SECBUFFER_EXTRA retornado de DecryptMessage (). Não há suporte para a renegociação no modo kernel Schannel. O chamador deve ignorar esse valor de retorno ou desligar a conexão. Se o valor for ignorado, o cliente ou o servidor poderá desligar a conexão como resultado. |


## <a name="remarks"></a>Comentários

Às vezes, um aplicativo lerá os dados da parte remota, tentará descriptografá-los usando **DecryptMessage (Schannel)** e descobrirá que o **DecryptMessage (Schannel)** foi bem-sucedido, mas os buffers de saída estão vazios. Esse comportamento é normal e os aplicativos devem ser capazes de lidar com eles.

Quando você usa o Schannel SSP, a função [**DecryptMessage (geral)**](decryptmessage--general.md) retorna um \_ \_ contexto de s I \_ expirou quando o remetente da mensagem desligou a conexão. Para obter informações sobre como iniciar ou reconhecer um desligamento, consulte [desligar uma conexão Schannel](shutting-down-an-schannel-connection.md).

Se você estiver usando o TLS 1,0, talvez seja necessário chamar essa função várias vezes, ajustando o buffer de entrada em cada chamada, para descriptografar uma mensagem inteira.


A função **DecryptMessage (Schannel)** retorna s \_ \_ renegotiate quando o remetente da mensagem deseja renegociar a conexão ([*contexto de segurança*](../secgloss/s-gly.md)). Um aplicativo manipula uma renegociação solicitada chamando [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (lado do servidor) ou [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md) (lado do cliente) e passa SECBUFFER_EXTRA retornado de DecryptMessage (). Depois que essa chamada inicial retorna um valor, continue como se seu aplicativo estivesse criando uma nova conexão. Para obter mais informações, consulte [criando um contexto de segurança Schannel](creating-an-schannel-security-context.md).


## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|-------------------------------------------|
| Cliente mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows XP\]          |
| Servidor mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Server 2003\] |
| parâmetro                   | SSPI. h (incluir Security. h)               |
| Biblioteca                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Confira também

- [Funções SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

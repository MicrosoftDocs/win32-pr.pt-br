---
description: Criptografa uma mensagem para fornecer privacidade usando Digest.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: Função EncryptMessage (Digest) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: af16238ca58449c286edd9eabb88d7bc9a3f7fa781fac360863fdd52f7296833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008424"
---
# <a name="encryptmessage-digest-function"></a>Função EncryptMessage (Digest)

A **função EncryptMessage (Digest)** criptografa uma mensagem para fornecer [*privacidade.*](../secgloss/p-gly.md) **EncryptMessage (Digest)** permite que o aplicativo escolha entre [*algoritmos criptográficos*](../secgloss/c-gly.md) com suporte pelo mecanismo escolhido. A **função EncryptMessage (Digest)** usa o [*contexto de segurança*](../secgloss/s-gly.md) referenciado pelo handle de contexto. Alguns pacotes não têm mensagens a serem criptografadas ou descriptografadas, mas fornecem um hash de [*integridade*](../secgloss/h-gly.md) que pode ser verificado.

Essa função está disponível apenas como um mecanismo SASL.

> [!Note]  
> **EncryptMessage (Digest)** e [**DecryptMessage (Digest)**](decryptmessage--digest.md) podem ser chamados ao mesmo tempo de dois threads diferentes em um contexto de SSPI [*(interface*](../secgloss/s-gly.md) de provedor de suporte de segurança) única se um thread estiver criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

 

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phContext* \[ Em\]
</dt> <dd>

Um handle para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para criptografar a mensagem.

</dd> <dt>

*fQOP* \[ Em\]
</dt> <dd>

Sinalizadores específicos do pacote que indicam a qualidade da proteção. Um [*pacote de segurança*](../secgloss/s-gly.md) pode usar esse parâmetro para habilitar a seleção de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Ao usar o SSP digest, esse parâmetro deve ser definido como zero.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Um ponteiro para uma [**estrutura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que podem ser do tipo SECBUFFER \_ DATA. Esse buffer contém a mensagem a ser criptografada. A mensagem é criptografada no local, sobrescrevendo o conteúdo original da estrutura.

A função não processa buffers com o atributo SECBUFFER \_ READONLY.

O comprimento da estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contém a mensagem não deve ser maior que **cbMaximumMessage**, que é obtido da função [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG \_ ATTR \_ STREAM \_ SIZES).

Ao usar o SSP digest, deve haver um segundo buffer do tipo SECBUFFER PADDING ou DADOS DE \_ BUFFER SEC para manter informações \_ \_ [*de*](../secgloss/d-gly.md#_security_digital_signature_gly) assinatura. Para obter o tamanho do buffer de saída, chame a [**função QueryContextAttributes (Digest)**](querycontextattributes--digest.md) e especifique SECPKG \_ ATTR \_ SIZES. A função retornará uma estrutura [**De tamanhos \_ SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) O tamanho do buffer de saída é a soma dos valores nos membros **cbMaxSignature** e **cbBlockSize.**

Os aplicativos que não usam SSL devem fornecer [**um SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) do tipo SECBUFFER \_ PADDING.

</dd> <dt>

*MessageSeqNo* \[ Em\]
</dt> <dd>

O número de sequência que o aplicativo de transporte atribuiu à mensagem. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser zero.

Ao usar o SSP digest, esse parâmetro deve ser definido como zero. O SSP digest gerencia a numeração de sequência internamente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função retornará SEC \_ E \_ OK.

Se a função falhar, ela retornará um dos códigos de erro a seguir.



| Código de retorno                                                                                                    | Descrição                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E BUFFER MUITO \_ \_ \_ PEQUENO**</dt> </dl>      | O buffer de saída é muito pequeno. Para obter mais informações, consulte Comentários.<br/>                                                                                                                                                                 |
| <dl> <dt>**CONTEXTO \_ SEC E \_ \_ EXPIRADO**</dt> </dl>        | O aplicativo está referenciando um contexto que já foi fechado. Um aplicativo escrito corretamente não deve receber esse erro.<br/>                                                                                               |
| <dl> <dt>**SISTEMA \_ DE CRIPTOGRAFIA SEC E \_ \_ \_ INVÁLIDO**</dt> </dl> | Não [*há*](../secgloss/c-gly.md) suporte para a [*codificação*](../secgloss/s-gly.md) escolhida para o contexto de segurança.<br/>                                                                                                         |
| <dl> <dt>**S \_ E \_ MEMÓRIA \_ INSUFICIENTE**</dt> </dl>    | Não há memória suficiente disponível para concluir a ação solicitada.<br/>                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ INVALID \_ HANDLE**</dt> </dl>         | Um alça de contexto que não é válido foi especificado no *parâmetro phContext.*<br/>                                                                                                                                                     |
| <dl> <dt>**SEC \_ E \_ TOKEN \_ INVÁLIDO**</dt> </dl>          | Nenhum buffer de tipo \_ DE DADOS SECBUFFER foi encontrado.<br/>                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ QOP NÃO TEM \_ \_ SUPORTE**</dt> </dl>     | Não há suporte [*para*](../secgloss/i-gly.md) confidencialidade nem integridade no contexto de [*segurança*](../secgloss/s-gly.md).<br/> |



 

## <a name="remarks"></a>Comentários

A **função EncryptMessage (Digest)** criptografa uma mensagem com base na mensagem e na chave de [*sessão*](../secgloss/s-gly.md) de um contexto [*de segurança*](../secgloss/s-gly.md).

Se o aplicativo [](../secgloss/s-gly.md) de transporte criou o contexto de segurança para dar suporte à detecção de sequência e o chamador fornece um número de sequência, a função inclui essas informações com a mensagem criptografada. Incluir essas informações protege contra reprodução, inserção e supressão de mensagens. O [*pacote de segurança*](../secgloss/s-gly.md) incorpora o número de sequência passado do aplicativo de transporte.

Ao usar o SSP digest, obter o tamanho do buffer de saída chamando a função [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) e especificando SECPKG \_ ATTR \_ SIZES. A função retornará uma estrutura [**De tamanhos \_ SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) O tamanho do buffer de saída é a soma dos valores nos membros **cbMaxSignature** e **cbBlockSize.**

> [!Note]  
> Esses buffers devem ser fornecidos na ordem mostrada.

 



| Tipo de buffer                           | Descrição                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ STREAM \_ HEADER<br/>  | Usado internamente. Nenhuma inicialização é necessária.<br/>                                                                        |
| DADOS \_ SECBUFFER<br/>            | Contém a [*mensagem de texto não*](../secgloss/s-gly.md) criptografado a ser criptografada.<br/> |
| SECBUFFER \_ STREAM \_ TRAILER<br/> | Usado internamente. Nenhuma inicialização é necessária.<br/>                                                                        |
| SECBUFFER \_ VAZIO<br/>           | Usado internamente. Nenhuma inicialização é necessária. O tamanho pode ser zero.<br/>                                                      |



 

Para obter um desempenho ideal, as *estruturas pMessage* devem ser alocadas da memória contígua.

**Windows XP:** Essa função também era conhecida como **SealMessage.** Os aplicativos agora devem usar **somente EncryptMessage (Digest).**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Sspi.h (inclua Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**DecryptMessage (Digest)**](decryptmessage--digest.md)
</dt> <dt>

[**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**QueryContextAttributes (resumo)**](querycontextattributes--digest.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 

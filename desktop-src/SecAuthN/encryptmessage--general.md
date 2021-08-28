---
description: Criptografa uma mensagem para fornecer privacidade.
ms.assetid: 2e09f262-9c3e-4db2-9285-017f5e1810c7
title: Função EncryptMessage (Geral) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 6645d58b753503853dae7998982a32221d1f0d14
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476282"
---
# <a name="encryptmessage-general-function"></a>Função EncryptMessage (Geral)

A **função EncryptMessage (Geral)** criptografa uma mensagem para fornecer [*privacidade.*](../secgloss/p-gly.md) **EncryptMessage (Geral)** permite que um aplicativo escolha entre [*algoritmos criptográficos*](../secgloss/c-gly.md) com suporte pelo mecanismo escolhido. A **função EncryptMessage (Geral)** usa o [*contexto de segurança*](../secgloss/s-gly.md) referenciado pelo handle de contexto. Alguns pacotes não têm mensagens a serem criptografadas ou descriptografadas, mas fornecem um hash de [*integridade*](../secgloss/h-gly.md) que pode ser verificado.

Ao usar o SSP (provedor de suporte [*de*](../secgloss/s-gly.md) segurança digest), essa função está disponível apenas como um mecanismo SASL.

Ao usar o SSP Schannel, essa função criptografa mensagens usando uma chave de sessão negociada com [*a*](../secgloss/s-gly.md) parte remota que receberá a mensagem. O algoritmo de criptografia é determinado pelo [ [*pacote de criptografia*](../secgloss/c-gly.md)]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) em uso.

> [!Note]  
> **EncryptMessage (Geral)** e [**DecryptMessage (Geral)**](decryptmessage--general.md) podem ser chamados ao mesmo tempo de dois threads diferentes em um contexto de SSPI [*(interface*](../secgloss/s-gly.md) de provedor de suporte de segurança) única se um thread estiver criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

Para obter informações sobre como usar essa função com um SSP específico, consulte os tópicos a seguir.

| Tópico                                                            | Descrição                                               |
|------------------------------------------------------------------|-----------------------------------------------------------|
| [**EncryptMessage (Digest)**](encryptmessage--digest.md)       | Criptografa uma mensagem para fornecer privacidade usando Digest.    |
| [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)   | Criptografa uma mensagem para fornecer privacidade usando Kerberos.  |
| [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) | Criptografa uma mensagem para fornecer privacidade usando Negotiate. |
| [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)           | Criptografa uma mensagem para fornecer privacidade usando NTLM.      |
| [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)   | Criptografa uma mensagem para fornecer privacidade usando o Schannel.  |

## <a name="syntax"></a>Sintaxe

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```
## <a name="parameters"></a>Parâmetros

*phContext* \[ Em\]

Um handle para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para criptografar a mensagem.

*fQOP* \[ Em\]

Sinalizadores específicos do pacote que indicam a qualidade da proteção. Um [*pacote de segurança*](../secgloss/s-gly.md) pode usar esse parâmetro para habilitar a seleção de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Ao usar o SSP digest, esse parâmetro deve ser definido como zero.

Esse parâmetro pode ser um dos sinalizadores a seguir.


| Valor | Significado | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Produza um header ou um trailer, mas não criptografe a mensagem.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</blockquote><br /> | 
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl><dt><strong>SECQOP_WRAP_OOB_DATA</strong></dt></dl> | Envie uma mensagem de alerta do Schannel. Nesse caso, o parâmetro <em>pMessage</em> deve conter um código de evento SSL/TLS de dois byte padrão. Esse valor só é suportado pelo SSP Schannel.<br /> | 


*pMessage* \[ in, out\]

Um ponteiro para uma [**estrutura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Na entrada, a estrutura faz referência a uma ou mais [**estruturas SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Um deles pode ser do tipo SECBUFFER \_ DATA. Esse buffer contém a mensagem a ser criptografada. A mensagem é criptografada no local, sobrescrevendo o conteúdo original da estrutura.

A função não processa buffers com o atributo SECBUFFER \_ READONLY.

O comprimento da estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contém a mensagem não deve ser maior que **cbMaximumMessage**, que é obtido da função [**QueryContextAttributes (Geral)**](querycontextattributes--general.md) (SECPKG \_ ATTR \_ STREAM \_ SIZES).

Ao usar o SSP digest, deve haver um segundo buffer do tipo SECBUFFER PADDING ou DADOS DE \_ BUFFER SEC para manter informações \_ \_ [*de*](../secgloss/d-gly.md#_security_digital_signature_gly) assinatura. Para obter o tamanho do buffer de saída, chame a [**função QueryContextAttributes (Geral)**](querycontextattributes--general.md) e especifique SECPKG \_ ATTR \_ SIZES. A função retornará uma estrutura [**De tamanhos \_ SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) O tamanho do buffer de saída é a soma dos valores nos membros **cbMaxSignature** e **cbBlockSize.**

Os aplicativos que não usam SSL devem fornecer [**um SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) do tipo SECBUFFER \_ PADDING.

*MessageSeqNo* \[ Em\]

O número de sequência que o aplicativo de transporte atribuiu à mensagem. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser zero.

Ao usar o SSP digest, esse parâmetro deve ser definido como zero. O SSP digest gerencia a numeração de sequência internamente.

Ao usar o SSP Schannel, esse parâmetro deve ser definido como zero. O SSP Schannel não usa números de sequência.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função retornará SEC \_ E \_ OK.

Se a função falhar, ela retornará um dos códigos de erro a seguir.

| Código de retorno                         | Descrição                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **S \_ E BUFFER MUITO \_ \_ \_ PEQUENO**      | O buffer de saída é muito pequeno. Para obter mais informações, consulte Comentários.                                                                                                          |
| **CONTEXTO \_ SEC E \_ \_ EXPIRADO**        | O aplicativo está referenciando um contexto que já foi fechado. Um aplicativo escrito corretamente não deve receber esse erro.                                        |
| **SISTEMA \_ DE CRIPTOGRAFIA SEC E \_ \_ \_ INVÁLIDO** | Não [*há*](../secgloss/c-gly.md) suporte para a [*codificação*](../secgloss/s-gly.md) escolhida para o contexto de segurança.                                                                       |
| **S \_ E \_ MEMÓRIA \_ INSUFICIENTE**    | Não há memória suficiente disponível para concluir a ação solicitada.                                                                                                      |
| **SEC \_ E \_ INVALID \_ HANDLE**         | Um alça de contexto que não é válido foi especificado no *parâmetro phContext.*                                                                                              |
| **SEC \_ E \_ TOKEN \_ INVÁLIDO**          | Nenhum buffer de tipo \_ DE DADOS SECBUFFER foi encontrado.                                                                                                                                   |
| **SEC \_ E \_ QOP NÃO TEM \_ \_ SUPORTE**     | Não há suporte [*para*](../secgloss/i-gly.md) confidencialidade nem integridade no contexto de [*segurança*](../secgloss/s-gly.md). |

## <a name="remarks"></a>Comentários

A **função EncryptMessage (Geral)** criptografa uma mensagem com base na mensagem e na chave [*de*](../secgloss/s-gly.md) sessão de um contexto [*de segurança*](../secgloss/s-gly.md).

Se o aplicativo [](../secgloss/s-gly.md) de transporte criou o contexto de segurança para dar suporte à detecção de sequência e o chamador fornece um número de sequência, a função inclui essas informações com a mensagem criptografada. Incluir essas informações protege contra reprodução, inserção e supressão de mensagens. O [*pacote de segurança*](../secgloss/s-gly.md) incorpora o número de sequência passado do aplicativo de transporte.

Ao usar o SSP digest, obter o tamanho do buffer de saída chamando a função [**QueryContextAttributes (Geral)**](querycontextattributes--general.md) e especificando SECPKG \_ ATTR \_ SIZES. A função retornará uma estrutura [**De tamanhos \_ SecPkgContext.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) O tamanho do buffer de saída é a soma dos valores nos membros **cbMaxSignature** e **cbBlockSize.**

Quando usado com o SSP Schannel, o parâmetro *pMessage* deve conter uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) com os buffers a seguir.

> [!Note]  
> Esses buffers devem ser fornecidos na ordem mostrada.

| Tipo de buffer                | Descrição                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| SECBUFFER \_ STREAM \_ HEADER  | Usado internamente. Nenhuma inicialização é necessária.                                                |
| DADOS \_ SECBUFFER            | Contém a [*mensagem de texto não*](../secgloss/s-gly.md) criptografado a ser criptografada. |
| SECBUFFER \_ STREAM \_ TRAILER | Usado internamente. Nenhuma inicialização é necessária.                                                |
| SECBUFFER \_ VAZIO           | Usado internamente. Nenhuma inicialização é necessária. O tamanho pode ser zero.                              |

Ao usar o SSP Schannel, determine o tamanho máximo de cada um dos buffers chamando a função [**QueryContextAttributes (Geral)**](querycontextattributes--general.md) e especificando o atributo SECPKG \_ ATTR \_ STREAM \_ SIZES. Essa função retorna uma estrutura [**SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) cujos membros contêm os tamanhos máximos para os buffers de header **(membro cbHeader),** mensagem (**membro cbMaximumMessage)** e trailer (**membro cbTrailer).**

Para obter um desempenho ideal, as *estruturas pMessage* devem ser alocadas da memória contígua.

**Windows XP/2000:** Essa função também era conhecida como **SealMessage.** Os aplicativos agora devem usar **Somente EncryptMessage (Geral).**

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows Somente \[ aplicativos da área de trabalho XP\]                                                            |
| Servidor mínimo com suporte | Windows Somente aplicativos da área de trabalho server 2003 \[\]                                                   |
| Cabeçalho                   | <dl> <dt>Sspi.h (inclua Security.h)</dt> </dl> |
| Biblioteca                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| DLL                      | <dl> <dt>Secur32.dll</dt> </dl>                 |

## <a name="see-also"></a>Confira também

- [Funções SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (Geral)**](acceptsecuritycontext--general.md)
- [**DecryptMessage (Geral)**](decryptmessage--general.md)
- [**InitializeSecurityContext (Geral)**](initializesecuritycontext--general.md)
- [**QueryContextAttributes (Geral)**](querycontextattributes--general.md)
- [**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**Secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

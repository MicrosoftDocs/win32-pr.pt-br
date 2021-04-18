---
description: Criptografa uma mensagem para fornecer privacidade.
ms.assetid: 2e09f262-9c3e-4db2-9285-017f5e1810c7
title: Função EncryptMessage (geral) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 3c661f5f529700db19683966783c1aa0793e376b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814601"
---
# <a name="encryptmessage-general-function"></a>Função EncryptMessage (geral)

A função **EncryptMessage (geral)** criptografa uma mensagem para fornecer [*privacidade*](../secgloss/p-gly.md). **EncryptMessage (geral)** permite que um aplicativo escolha entre [*algoritmos de criptografia*](../secgloss/c-gly.md) com suporte no mecanismo escolhido. A função **EncryptMessage (geral)** usa o [*contexto de segurança*](../secgloss/s-gly.md) referenciado pelo identificador de contexto. Alguns pacotes não têm mensagens a serem criptografadas ou descriptografadas, mas fornecem um [*hash*](../secgloss/h-gly.md) de integridade que pode ser verificado.

Ao usar o SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) Digest, essa função está disponível apenas como um mecanismo SASL.

Ao usar o SSP do Schannel, essa função criptografa mensagens usando uma [*chave de sessão*](../secgloss/s-gly.md) negociada com a parte remota que receberá a mensagem. O algoritmo de criptografia é determinado pelo [conjunto de [*codificação*](../secgloss/c-gly.md)]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) em uso.

> [!Note]  
> **EncryptMessage (geral)** e [**DecryptMessage (geral)**](decryptmessage--general.md) podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ) se um thread estiver Criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

Para obter informações sobre como usar essa função com um SSP específico, consulte os tópicos a seguir.

| Tópico                                                            | Descrição                                               |
|------------------------------------------------------------------|-----------------------------------------------------------|
| [**EncryptMessage (resumo)**](encryptmessage--digest.md)       | Criptografa uma mensagem para fornecer privacidade usando Digest.    |
| [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)   | Criptografa uma mensagem para fornecer privacidade usando o Kerberos.  |
| [**EncryptMessage (negociar)**](encryptmessage--negotiate.md) | Criptografa uma mensagem para fornecer privacidade usando Negotiate. |
| [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)           | Criptografa uma mensagem para fornecer privacidade usando NTLM.      |
| [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)   | Criptografa uma mensagem para fornecer privacidade usando Schannel.  |

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

*phContext* \[ no\]

Um identificador para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para criptografar a mensagem.

*fQOP* \[ no\]

Sinalizadores específicos do pacote que indicam a qualidade da proteção. Um [*pacote de segurança*](../secgloss/s-gly.md) pode usar esse parâmetro para habilitar a seleção de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Ao usar o SSP de resumo, esse parâmetro deve ser definido como zero.

Esse parâmetro pode ser um dos sinalizadores a seguir.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valor</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Produz um cabeçalho ou um trailer, mas não criptografa a mensagem.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</blockquote><br/></td></tr><tr class="even"><td><span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt><strong>SECQOP_WRAP_OOB_DATA</strong></dt> </dl></td><td>Envie uma mensagem de alerta Schannel. Nesse caso, o parâmetro <em>PMessage</em> deve conter um código de evento SSL/TLS padrão de dois bytes. Esse valor tem suporte apenas pelo SSP do Schannel.<br/></td></tr></tbody></table>

*PMessage* \[ entrada, saída\]

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Um deles pode ser do tipo dados de SECBUFFER \_ . Esse buffer contém a mensagem a ser criptografada. A mensagem é criptografada no local, substituindo o conteúdo original da estrutura.

A função não processa buffers com o \_ atributo ReadOnly SECBUFFER.

O comprimento da estrutura de [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contém a mensagem não deve ser maior que **cbMaximumMessage**, que é obtido da função [**QueryContextAttributes (geral)**](querycontextattributes--general.md) (SECPKG de \_ fluxo de attr \_ \_ ).

Ao usar o SSP de resumo, deve haver um segundo buffer do tipo SECBUFFER \_ Padding ou \_ os dados de buffer de s \_ para manter as informações de [*assinatura*](../secgloss/d-gly.md#_security_digital_signature_gly) . Para obter o tamanho do buffer de saída, chame a função [**QueryContextAttributes (geral)**](querycontextattributes--general.md) e especifique os \_ tamanhos de attr SECPKG \_ . A função retornará uma estrutura [**de \_ tamanhos de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . O tamanho do buffer de saída é a soma dos valores nos membros **cbMaxSignature** e **cbBlockSize** .

Os aplicativos que não usam SSL devem fornecer um [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) do tipo \_ preenchimento SecBuffer.

*MessageSeqNo* \[ no\]

O número de sequência que o aplicativo de transporte atribuiu à mensagem. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser zero.

Ao usar o SSP de resumo, esse parâmetro deve ser definido como zero. O SSP de resumo gerencia a numeração de sequência internamente.

Ao usar o SSP do Schannel, esse parâmetro deve ser definido como zero. O SSP do Schannel não usa números de sequência.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.

Se a função falhar, ela retornará um dos seguintes códigos de erro.

| Código de retorno                         | Description                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ buffer \_ muito \_ pequeno**      | O buffer de saída é muito pequeno. Para obter mais informações, consulte Comentários.                                                                                                          |
| **o \_ contexto s E \_ \_ expirou**        | O aplicativo está fazendo referência a um contexto que já foi fechado. Um aplicativo escrito corretamente não deve receber esse erro.                                        |
| **s \_ E \_ sistema de criptografia \_ \_ inválidos** | Não há suporte para a [*codificação*](../secgloss/c-gly.md) escolhida para o [*contexto de segurança*](../secgloss/s-gly.md) .                                                                       |
| **s \_ E \_ memória insuficiente \_**    | Não há memória suficiente disponível para concluir a ação solicitada.                                                                                                      |
| **s \_ E \_ \_ identificador inválido**         | Um identificador de contexto inválido foi especificado no parâmetro *phContext* .                                                                                              |
| **s \_ E \_ \_ token inválido**          | Nenhum \_ buffer de tipo de dados SECBUFFER foi encontrado.                                                                                                                                   |
| **s \_ E \_ QOP \_ não \_ têm suporte**     | Nenhuma confidencialidade nem [*integridade*](../secgloss/i-gly.md) têm suporte no [*contexto de segurança*](../secgloss/s-gly.md). |

## <a name="remarks"></a>Comentários

A função **EncryptMessage (geral)** criptografa uma mensagem com base na mensagem e na [*chave de sessão*](../secgloss/s-gly.md) de um [*contexto de segurança*](../secgloss/s-gly.md).

Se o aplicativo de transporte criou o [*contexto de segurança*](../secgloss/s-gly.md) para dar suporte à detecção de sequência e o chamador fornecer um número de sequência, a função incluirá essas informações com a mensagem criptografada. A inclusão dessas informações protege contra reprodução, inserção e supressão de mensagens. O [*pacote de segurança*](../secgloss/s-gly.md) incorpora o número de sequência passado do aplicativo de transporte.

Ao usar o SSP de resumo, obtenha o tamanho do buffer de saída chamando a função [**QueryContextAttributes (geral)**](querycontextattributes--general.md) e especificando os \_ tamanhos de attr SECPKG \_ . A função retornará uma estrutura [**de \_ tamanhos de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . O tamanho do buffer de saída é a soma dos valores nos membros **cbMaxSignature** e **cbBlockSize** .

Quando usado com o Schannel SSP, o parâmetro *PMessage* deve conter uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) com os buffers a seguir.

> [!Note]  
> Esses buffers devem ser fornecidos na ordem mostrada.

| Tipo de buffer                | Description                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| \_cabeçalho de fluxo de SECBUFFER \_  | Usado internamente. Nenhuma inicialização é necessária.                                                |
| dados do SECBUFFER \_            | Contém a mensagem de [*texto sem formatação*](../secgloss/s-gly.md) a ser criptografada. |
| \_trailer de fluxo de SECBUFFER \_ | Usado internamente. Nenhuma inicialização é necessária.                                                |
| SECBUFFER \_ vazio           | Usado internamente. Nenhuma inicialização é necessária. O tamanho pode ser zero.                              |

Ao usar o SSP do Schannel, determine o tamanho máximo de cada um dos buffers chamando a função [**QueryContextAttributes (geral)**](querycontextattributes--general.md) e especificando o atributo de \_ tamanhos de fluxo SECPKG attr \_ \_ . Essa função retorna uma [**estrutura SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) cujos membros contêm os tamanhos máximos para os buffers de cabeçalho (membro **cbHeader** ), mensagem (membro **CbMaximumMessage** ) e trailer (membro **cbTrailer** ).

Para um desempenho ideal, as estruturas *PMessage* devem ser alocadas da memória contígua.

**Windows XP/2000:** Essa função também era conhecida como **SealMessage**. Os aplicativos agora devem usar **EncryptMessage (geral)** apenas.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows XP\]                                                            |
| Servidor mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Server 2003\]                                                   |
| parâmetro                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL                      | <dl> <dt>Secur32.dll</dt> </dl>                 |

## <a name="see-also"></a>Confira também

- [Funções SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md)
- [**DecryptMessage (geral)**](decryptmessage--general.md)
- [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md)
- [**QueryContextAttributes (geral)**](querycontextattributes--general.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

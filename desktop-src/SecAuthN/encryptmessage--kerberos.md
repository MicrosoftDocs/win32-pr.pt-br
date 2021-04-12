---
description: Criptografa uma mensagem para fornecer privacidade usando o Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: Função EncryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 9413bc61739d67d7462e7e1257727e0401967ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171272"
---
# <a name="encryptmessage-kerberos-function"></a>Função EncryptMessage (Kerberos)

A função **EncryptMessage (Kerberos)** criptografa uma mensagem para fornecer [*privacidade*](../secgloss/p-gly.md). **EncryptMessage (Kerberos)** permite que um aplicativo escolha entre [*algoritmos de criptografia*](../secgloss/c-gly.md) com suporte no mecanismo escolhido. A função **EncryptMessage (Kerberos)** usa o [*contexto de segurança*](../secgloss/s-gly.md) referenciado pelo identificador de contexto. Alguns pacotes não têm mensagens a serem criptografadas ou descriptografadas, mas fornecem um [*hash*](../secgloss/h-gly.md) de integridade que pode ser verificado.

> [!Note]  
> **EncryptMessage (Kerberos)** e [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ), se um thread estiver Criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

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

<dl> <dt>

*phContext* \[ no\]
</dt> <dd>

Um identificador para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para criptografar a mensagem.

</dd> <dt>

*fQOP* \[ no\]
</dt> <dd>

Sinalizadores específicos do pacote que indicam a qualidade da proteção. Um [*pacote de segurança*](../secgloss/s-gly.md) pode usar esse parâmetro para habilitar a seleção de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Esse parâmetro pode ser o sinalizador a seguir.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valor</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Produz um cabeçalho ou um trailer, mas não criptografa a mensagem.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</blockquote><br/></td></tr></tbody></table>

</dd> <dt>

*PMessage* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que podem ser do tipo \_ dados SecBuffer. Esse buffer contém a mensagem a ser criptografada. A mensagem é criptografada no local, substituindo o conteúdo original da estrutura.

A função não processa buffers com o \_ atributo ReadOnly SECBUFFER.

O comprimento da estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contém a mensagem não deve ser maior que **cbMaximumMessage**, que é obtido da função [**QueryContextAttributes (Kerberos**](querycontextattributes--kerberos.md) \_ attr tamanhos de fluxo SECPKG \_ \_ ).

Os aplicativos que não usam SSL devem fornecer um [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) do tipo \_ preenchimento SecBuffer.

</dd> <dt>

*MessageSeqNo* \[ no\]
</dt> <dd>

O número de sequência que o aplicativo de transporte atribuiu à mensagem. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.

Se a função falhar, ela retornará um dos seguintes códigos de erro.

| Código de retorno                                                                                                    | Descrição                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ buffer \_ muito \_ pequeno**</dt> </dl>      | O buffer de saída é muito pequeno. Para obter mais informações, consulte Comentários.                                                                                                                                                                 |
| <dl> <dt>**o \_ contexto s E \_ \_ expirou**</dt> </dl>        | O aplicativo está fazendo referência a um contexto que já foi fechado. Um aplicativo escrito corretamente não deve receber esse erro.                                                                                               |
| <dl> <dt>**s \_ E \_ sistema de criptografia \_ \_ inválidos**</dt> </dl> | Não há suporte para a [*codificação*](../secgloss/c-gly.md) escolhida para o [*contexto de segurança*](../secgloss/s-gly.md) .                                                                                                         |
| <dl> <dt>**s \_ E \_ memória insuficiente \_**</dt> </dl>    | Não há memória suficiente disponível para concluir a ação solicitada.                                                                                                                                                             |
| <dl> <dt>**s \_ E \_ \_ identificador inválido**</dt> </dl>         | Um identificador de contexto inválido foi especificado no parâmetro *phContext* .                                                                                                                                                     |
| <dl> <dt>**s \_ E \_ \_ token inválido**</dt> </dl>          | Nenhum \_ buffer de tipo de dados SECBUFFER foi encontrado.                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ QOP \_ não \_ têm suporte**</dt> </dl>     | Nenhuma confidencialidade nem [*integridade*](../secgloss/i-gly.md) têm suporte no [*contexto de segurança*](../secgloss/s-gly.md). |

## <a name="remarks"></a>Comentários

A função **EncryptMessage (Kerberos)** criptografa uma mensagem com base na mensagem e na [*chave de sessão*](../secgloss/s-gly.md) de um [*contexto de segurança*](../secgloss/s-gly.md).

Se o aplicativo de transporte criou o [*contexto de segurança*](../secgloss/s-gly.md) para dar suporte à detecção de sequência e o chamador fornecer um número de sequência, a função incluirá essas informações com a mensagem criptografada. A inclusão dessas informações protege contra reprodução, inserção e supressão de mensagens. O [*pacote de segurança*](../secgloss/s-gly.md) incorpora o número de sequência passado do aplicativo de transporte.

> [!Note]  
> Esses buffers devem ser fornecidos na ordem mostrada.

| Tipo de buffer                           | Descrição                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| < de cabeçalho de \_ fluxo de SECBUFFER \_  | Usado internamente. Nenhuma inicialização é necessária.                                                                       |
| dados do SECBUFFER \_            | Contém a mensagem de [*texto sem formatação*](../secgloss/s-gly.md) a ser criptografada. |
| \_trailer de fluxo de SECBUFFER \_ | Usado internamente. Nenhuma inicialização é necessária.                                                                        |
| SECBUFFER \_ vazio           | Usado internamente. Nenhuma inicialização é necessária. O tamanho pode ser zero.                                                      |

Para um desempenho ideal, as estruturas *PMessage* devem ser alocadas da memória contígua.

**Windows XP:** Essa função também era conhecida como **SealMessage**. Os aplicativos agora devem usar somente **EncryptMessage (Kerberos)** .

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|-------------------------------------------|
| Cliente mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows XP\]          |
| Servidor mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Server 2003\] |
| parâmetro                   | SSPI. h (incluir Security. h)               |
| Biblioteca                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)
</dt> <dt>

[**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)
</dt> <dt>

[**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

---
description: Criptografa uma mensagem para fornecer privacidade usando Negotiate.
ms.assetid: b80b3d64-9c0a-4602-9378-1e208f6593fc
title: Função EncryptMessage (Negotiate)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 037866088f58fa1d70939b84062161a6e4f610b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297269"
---
# <a name="encryptmessage-negotiate-function"></a>Função EncryptMessage (Negotiate)

A função **EncryptMessage (Negotiate)** criptografa uma mensagem para fornecer [*privacidade*](../secgloss/p-gly.md). **EncryptMessage (Negotiate)** permite que o aplicativo escolha entre [*algoritmos de criptografia*](../secgloss/c-gly.md) com suporte no mecanismo escolhido. A função **EncryptMessage (Negotiate)** usa o [*contexto de segurança*](../secgloss/s-gly.md) referenciado pelo identificador de contexto. Alguns pacotes não têm mensagens a serem criptografadas ou descriptografadas, mas fornecem um [*hash*](../secgloss/h-gly.md) de integridade que pode ser verificado.

> [!Note]  
> **EncryptMessage (Negotiate)** e [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ), se um thread estiver Criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

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

*phContext* \[ em \] um identificador para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para criptografar a mensagem.

*fQOP* \[ em \] sinalizadores específicos do pacote que indicam a qualidade da proteção. Um [*pacote de segurança*](../secgloss/s-gly.md) pode usar esse parâmetro para habilitar a seleção de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Esse parâmetro pode ser o sinalizador a seguir.

| Valor                  | Significado                                                     |
|------------------------|-------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | Produz um cabeçalho ou um trailer, mas não criptografa a mensagem. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.

*PMessage* \[ in, \] um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que podem ser do tipo \_ dados SecBuffer. Esse buffer contém a mensagem a ser criptografada. A mensagem é criptografada no local, substituindo o conteúdo original da estrutura.

A função não processa buffers com o \_ atributo ReadOnly SECBUFFER.

O comprimento da estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contém a mensagem não deve ser maior que **cbMaximumMessage**, que é obtido da função [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) (SECPKG de \_ fluxo de attr) \_ \_ .

Os aplicativos que não usam SSL devem fornecer um [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) do tipo \_ preenchimento SecBuffer.

*MessageSeqNo* \[ no \] número de sequência que o aplicativo de transporte atribuiu à mensagem. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser zero.

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.

Se a função falhar, ela retornará um dos seguintes códigos de erro.

| Código de retorno                         | Descrição                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ buffer \_ muito \_ pequeno**      | O buffer de saída é muito pequeno. Para obter mais informações, consulte Comentários.                                                                   |
| **o \_ contexto s E \_ \_ expirou**        | O aplicativo está fazendo referência a um contexto que já foi fechado. Um aplicativo escrito corretamente não deve receber esse erro. |
| **s \_ E \_ sistema de criptografia \_ \_ inválidos** | Não há suporte para a [*codificação*](../secgloss/c-gly.md) escolhida para o [*contexto de segurança*](../secgloss/s-gly.md) .                                |
| **s \_ E \_ memória insuficiente \_**    | Não há memória suficiente disponível para concluir a ação solicitada.                                                               |
| **s \_ E \_ \_ identificador inválido**         | Um identificador de contexto inválido foi especificado no parâmetro *phContext* .                                                       |
| **s \_ E \_ \_ token inválido**          | Nenhum \_ buffer de tipo de dados SECBUFFER foi encontrado.                                                                                            |
| **s \_ E \_ QOP \_ não \_ têm suporte**     | Nenhuma confidencialidade nem [*integridade*](../secgloss/i-gly.md) têm suporte no [*contexto de segurança*](../secgloss/s-gly.md).             |

## <a name="remarks"></a>Comentários

A função **EncryptMessage (Negotiate)** criptografa uma mensagem com base na mensagem e na [*chave de sessão*](../secgloss/s-gly.md) de um [*contexto de segurança*](../secgloss/s-gly.md).

Se o aplicativo de transporte criou o [*contexto de segurança*](../secgloss/s-gly.md) para dar suporte à detecção de sequência e o chamador fornecer um número de sequência, a função incluirá essas informações com a mensagem criptografada. A inclusão dessas informações protege contra reprodução, inserção e supressão de mensagens. O [*pacote de segurança*](../secgloss/s-gly.md) incorpora o número de sequência passado do aplicativo de transporte.

> [!Note]  
> Esses buffers devem ser fornecidos na ordem mostrada.

| Tipo de buffer                | Descrição                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| \_cabeçalho de fluxo de SECBUFFER \_  | Usado internamente. Nenhuma inicialização é necessária.                                                |
| dados do SECBUFFER \_            | Contém a mensagem de [*texto sem formatação*](../secgloss/s-gly.md) a ser criptografada. |
| \_trailer de fluxo de SECBUFFER \_ | Usado internamente. Nenhuma inicialização é necessária.                                                |
| SECBUFFER \_ vazio           | Usado internamente. Nenhuma inicialização é necessária. O tamanho pode ser zero.                              |

Para um desempenho ideal, as estruturas *PMessage* devem ser alocadas da memória contígua.

**Windows XP:** Essa função também era conhecida como **SealMessage**. Os aplicativos agora devem usar apenas **EncryptMessage (Negotiate)** .

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|-------------------------------------------------|
| Cliente mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows XP\]                |
| Servidor mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Server 2003\]       |
| parâmetro                   | SSPI. h (incluir Security. h)                     |
| Biblioteca                  | Secur32. lib                                     |
| DLL                      | Secur32.dll                                     |

## <a name="see-also"></a>Confira também

- [Funções SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (negociar)**](acceptsecuritycontext--negotiate.md)
- [**DecryptMessage (negociar)**](decryptmessage--negotiate.md)
- [**InitializeSecurityContext (negociar)**](initializesecuritycontext--negotiate.md)
- [**QueryContextAttributes (negociar)**](querycontextattributes--negotiate.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

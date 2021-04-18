---
description: Criptografa uma mensagem para fornecer privacidade usando Schannel.
ms.assetid: b02b38bd-f3dd-4bf8-a36e-44ff9fbbe550
title: Função EncryptMessage (Schannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 3075b2fe7e5b4167a5a8527a16009282b2fca1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785976"
---
# <a name="encryptmessage-schannel-function"></a>Função EncryptMessage (Schannel)

A função **EncryptMessage (Schannel)** criptografa uma mensagem para fornecer [*privacidade*](../secgloss/p-gly.md). **EncryptMessage (Schannel)** permite que um aplicativo escolha entre [*algoritmos de criptografia*](../secgloss/c-gly.md) com suporte no mecanismo escolhido. A função **EncryptMessage (Schannel)** usa o [*contexto de segurança*](../secgloss/s-gly.md) referenciado pelo identificador de contexto. Alguns pacotes não têm mensagens a serem criptografadas ou descriptografadas, mas fornecem um [*hash*](../secgloss/h-gly.md) de integridade que pode ser verificado.

Ao usar o SSP do Schannel, essa função criptografa mensagens usando uma [*chave de sessão*](../secgloss/s-gly.md) negociada com a parte remota que receberá a mensagem. O algoritmo de criptografia é determinado pelo [conjunto de [*codificação*](../secgloss/c-gly.md)]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) em uso.

> [!Note]  
> **EncryptMessage (Schannel)** e [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ), se um thread estiver Criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

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

Esse parâmetro pode ser o sinalizador a seguir.

| Valor                                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt>**SECQOP \_ encapsular \_ \_ dados OOB**</dt> </dl> | Envie uma mensagem de alerta Schannel. Nesse caso, o parâmetro *PMessage* deve conter um código de evento SSL/TLS padrão de dois bytes. Esse valor tem suporte apenas pelo SSP do Schannel.<br/> Por exemplo, começando com o Windows Vista, a mensagem "servidor Hello" enviada pelo servidor durante o protocolo de reautenticação deve ser criptografada como um alerta TLS.<br/> |

*PMessage* \[ entrada, saída\]

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Um deles pode ser do tipo dados de SECBUFFER \_ . Esse buffer contém a mensagem a ser criptografada. A mensagem é criptografada no local, substituindo o conteúdo original da estrutura.

A função não processa buffers com o \_ atributo ReadOnly SECBUFFER.

O comprimento da estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contém a mensagem não deve ser maior do que **cbMaximumMessage**, que é obtido da função [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) (SECPKG de \_ fluxo de attr) \_ \_ .

*MessageSeqNo* \[ no\]

O número de sequência que o aplicativo de transporte atribuiu à mensagem. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser zero.

Ao usar o SSP do Schannel, esse parâmetro deve ser definido como zero. O SSP do Schannel não usa números de sequência.

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.

Se a função falhar, ela retornará um dos seguintes códigos de erro.

| Código de retorno                                                                                                    | Descrição                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ buffer \_ muito \_ pequeno**</dt> </dl>      | O buffer de saída é muito pequeno. Para obter mais informações, consulte Comentários.<br/>                                                                               |
| <dl> <dt>**o \_ contexto s E \_ \_ expirou**</dt> </dl>        | O aplicativo está fazendo referência a um contexto que já foi fechado. Um aplicativo escrito corretamente não deve receber esse erro.<br/>             |
| <dl> <dt>**s \_ E \_ sistema de criptografia \_ \_ inválidos**</dt> </dl> | Não há suporte para a [*codificação*](../secgloss/c-gly.md) escolhida para o [*contexto de segurança*](../secgloss/s-gly.md) .<br/>                       |
| <dl> <dt>**s \_ E \_ memória insuficiente \_**</dt> </dl>    | Não há memória suficiente disponível para concluir a ação solicitada.<br/>                                                                           |
| <dl> <dt>**s \_ E \_ \_ identificador inválido**</dt> </dl>         | Um identificador de contexto inválido foi especificado no parâmetro *phContext* .<br/>                                                                   |
| <dl> <dt>**s \_ E \_ \_ token inválido**</dt> </dl>          | Nenhum \_ buffer de tipo de dados SECBUFFER foi encontrado.<br/>                                                                                                        |
| <dl> <dt>**s \_ E \_ QOP \_ não \_ têm suporte**</dt> </dl>     | Nenhuma confidencialidade nem [*integridade*](../secgloss/i-gly.md) têm suporte no [*contexto de segurança*](../secgloss/s-gly.md).<br/> |

## <a name="remarks"></a>Comentários

A função **EncryptMessage (Schannel)** criptografa uma mensagem com base na mensagem e na [*chave de sessão*](../secgloss/s-gly.md) de um [*contexto de segurança*](../secgloss/s-gly.md).

Se o aplicativo de transporte criou o [*contexto de segurança*](../secgloss/s-gly.md) para dar suporte à detecção de sequência e o chamador fornecer um número de sequência, a função incluirá essas informações com a mensagem criptografada. A inclusão dessas informações protege contra reprodução, inserção e supressão de mensagens. O [*pacote de segurança*](../secgloss/s-gly.md) incorpora o número de sequência passado do aplicativo de transporte.

Quando usado com o Schannel SSP, o parâmetro *PMessage* deve conter uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) com os buffers a seguir.

> [!Note]  
> Esses buffers devem ser fornecidos na ordem mostrada.

| Tipo de buffer                | Descrição                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------|
| \_cabeçalho de fluxo de SECBUFFER \_  | Usado internamente. Nenhuma inicialização é necessária.                                                                        |
| dados do SECBUFFER \_            | Contém a mensagem de [*texto sem formatação*](../secgloss/s-gly.md) a ser criptografada. |
| \_trailer de fluxo de SECBUFFER \_ | Usado internamente. Nenhuma inicialização é necessária.                                                                        |
| SECBUFFER \_ vazio           | Usado internamente. Nenhuma inicialização é necessária. O tamanho pode ser zero.                                                      |

Ao usar o SSP do Schannel, determine o tamanho máximo de cada um dos buffers chamando a função [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) e especificando o atributo de \_ tamanhos de fluxo SECPKG attr \_ \_ . Essa função retorna uma [**estrutura SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) cujos membros contêm os tamanhos máximos para os buffers de cabeçalho (membro **cbHeader** ), mensagem (membro **CbMaximumMessage** ) e trailer (membro **cbTrailer** ).

Para um desempenho ideal, as estruturas *PMessage* devem ser alocadas da memória contígua.

**Windows XP/2000:** Essa função também era conhecida como **SealMessage**. Os aplicativos agora devem usar apenas **EncryptMessage (Schannel)** .

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows XP\]          |
| Servidor mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Server 2003\] |
| parâmetro                   | SSPI. h (incluir Security. h)               |
| Biblioteca                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Confira também

- [Funções SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
- [**DecryptMessage (Schannel)**](decryptmessage--schannel.md)
- [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
- [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

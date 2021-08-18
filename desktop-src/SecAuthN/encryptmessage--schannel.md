---
description: Criptografa uma mensagem para fornecer privacidade usando o Schannel.
ms.assetid: b02b38bd-f3dd-4bf8-a36e-44ff9fbbe550
title: Função EncryptMessage (Schannel)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: de792e543a8cb67bd6b608d79832fd31a68267fc297a85e0e178d268bbc069d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008284"
---
# <a name="encryptmessage-schannel-function"></a>Função EncryptMessage (Schannel)

A **função EncryptMessage (Schannel)** criptografa uma mensagem para fornecer [*privacidade.*](../secgloss/p-gly.md) **EncryptMessage (Schannel)** permite que um aplicativo escolha entre [*algoritmos criptográficos*](../secgloss/c-gly.md) com suporte pelo mecanismo escolhido. A **função EncryptMessage (Schannel)** usa o [*contexto de segurança*](../secgloss/s-gly.md) referenciado pelo handle de contexto. Alguns pacotes não têm mensagens a serem criptografadas ou descriptografadas, mas fornecem um hash de [*integridade*](../secgloss/h-gly.md) que pode ser verificado.

Ao usar o SSP Schannel, essa função criptografa mensagens usando uma chave de sessão negociada com [*a*](../secgloss/s-gly.md) parte remota que receberá a mensagem. O algoritmo de criptografia é determinado pelo [ [*pacote de criptografia*](../secgloss/c-gly.md)]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) em uso.

> [!Note]  
> **EncryptMessage (Schannel)** e [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto de SSPI [*(interface*](../secgloss/s-gly.md) de provedor de suporte de segurança) se um thread estiver criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

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

Esse parâmetro pode ser o sinalizador a seguir.

| Valor                                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt>**SECQOP \_ WRAP \_ OOB \_ DATA**</dt> </dl> | Envie uma mensagem de alerta do Schannel. Nesse caso, o parâmetro *pMessage* deve conter um código de evento SSL/TLS de dois byte padrão. Esse valor só é suportado pelo SSP Schannel.<br/> Por exemplo, a partir do Windows Vista, a mensagem "server hello" enviada pelo servidor durante o protocolo de re autenticação deve ser criptografada como um alerta TLS.<br/> |

*pMessage* \[ in, out\]

Um ponteiro para uma [**estrutura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Na entrada, a estrutura faz referência a uma ou mais [**estruturas SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Um deles pode ser do tipo SECBUFFER \_ DATA. Esse buffer contém a mensagem a ser criptografada. A mensagem é criptografada no local, sobrescrevendo o conteúdo original da estrutura.

A função não processa buffers com o atributo SECBUFFER \_ READONLY.

O comprimento da estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contém a mensagem não deve ser maior que **cbMaximumMessage**, que é obtido da função [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) (SECPKG \_ ATTR \_ STREAM \_ SIZES).

*MessageSeqNo* \[ Em\]

O número de sequência que o aplicativo de transporte atribuiu à mensagem. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser zero.

Ao usar o SSP Schannel, esse parâmetro deve ser definido como zero. O SSP Schannel não usa números de sequência.

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função retornará SEC \_ E \_ OK.

Se a função falhar, ela retornará um dos códigos de erro a seguir.

| Código de retorno                                                                                                    | Descrição                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E BUFFER MUITO \_ \_ \_ PEQUENO**</dt> </dl>      | O buffer de saída é muito pequeno. Para obter mais informações, consulte Comentários.<br/>                                                                               |
| <dl> <dt>**CONTEXTO \_ SEC E \_ \_ EXPIRADO**</dt> </dl>        | O aplicativo está referenciando um contexto que já foi fechado. Um aplicativo escrito corretamente não deve receber esse erro.<br/>             |
| <dl> <dt>**SISTEMA \_ DE CRIPTOGRAFIA SEC E \_ \_ \_ INVÁLIDO**</dt> </dl> | Não [*há*](../secgloss/c-gly.md) suporte para a [*codificação*](../secgloss/s-gly.md) escolhida para o contexto de segurança.<br/>                       |
| <dl> <dt>**S \_ E \_ MEMÓRIA \_ INSUFICIENTE**</dt> </dl>    | Não há memória suficiente disponível para concluir a ação solicitada.<br/>                                                                           |
| <dl> <dt>**SEC \_ E \_ INVALID \_ HANDLE**</dt> </dl>         | Um alça de contexto que não é válido foi especificado no *parâmetro phContext.*<br/>                                                                   |
| <dl> <dt>**SEC \_ E \_ TOKEN \_ INVÁLIDO**</dt> </dl>          | Nenhum buffer de tipo \_ DE DADOS SECBUFFER foi encontrado.<br/>                                                                                                        |
| <dl> <dt>**SEC \_ E \_ QOP NÃO TEM \_ \_ SUPORTE**</dt> </dl>     | Não há suporte [*para*](../secgloss/i-gly.md) confidencialidade nem integridade no contexto de [*segurança*](../secgloss/s-gly.md).<br/> |

## <a name="remarks"></a>Comentários

A **função EncryptMessage (Schannel)** criptografa uma mensagem com base na mensagem e na chave de [*sessão*](../secgloss/s-gly.md) de um contexto [*de segurança*](../secgloss/s-gly.md).

Se o aplicativo [](../secgloss/s-gly.md) de transporte criou o contexto de segurança para dar suporte à detecção de sequência e o chamador fornece um número de sequência, a função inclui essas informações com a mensagem criptografada. Incluir essas informações protege contra reprodução, inserção e supressão de mensagens. O [*pacote de segurança*](../secgloss/s-gly.md) incorpora o número de sequência passado do aplicativo de transporte.

Quando usado com o SSP Schannel, o parâmetro *pMessage* deve conter uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) com os buffers a seguir.

> [!Note]  
> Esses buffers devem ser fornecidos na ordem mostrada.

| Tipo de buffer                | Descrição                                                                                                         |
|----------------------------|---------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ STREAM \_ HEADER  | Usado internamente. Nenhuma inicialização é necessária.                                                                        |
| DADOS \_ SECBUFFER            | Contém a [*mensagem de texto não*](../secgloss/s-gly.md) criptografado a ser criptografada. |
| SECBUFFER \_ STREAM \_ TRAILER | Usado internamente. Nenhuma inicialização é necessária.                                                                        |
| SECBUFFER \_ VAZIO           | Usado internamente. Nenhuma inicialização é necessária. O tamanho pode ser zero.                                                      |

Ao usar o SSP Schannel, determine o tamanho máximo de cada um dos buffers chamando a [**função QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md) e especificando o atributo SECPKG \_ ATTR \_ STREAM \_ SIZES. Essa função retorna uma estrutura [**SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) cujos membros contêm os tamanhos máximos para os buffers de header **(membro cbHeader),** mensagem (**membro cbMaximumMessage)** e trailer (**membro cbTrailer).**

Para obter um desempenho ideal, as *estruturas pMessage* devem ser alocadas da memória contígua.

**Windows XP/2000:** Essa função também era conhecida como **SealMessage.** Os aplicativos agora devem **usar somente EncryptMessage (Schannel).**

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte | Windows Somente \[ aplicativos da área de trabalho XP\]          |
| Servidor mínimo com suporte | Windows Somente aplicativos da área de trabalho server 2003 \[\] |
| Cabeçalho                   | Sspi.h (inclua Security.h)               |
| Biblioteca                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Confira também

- [Funções SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md)
- [**DecryptMessage (Schannel)**](decryptmessage--schannel.md)
- [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md)
- [**QueryContextAttributes (Schannel)**](querycontextattributes--schannel.md)
- [**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**Secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

---
description: Descriptografa uma mensagem usando o Kerberos.
ms.assetid: 9e699f7c-f738-4702-bdef-fb2c276c38fc
title: Função DecryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 62add8d4b33f356aeae5bbbf8fa16b19a0b5e419e0ab6c0a6847a3ed087ce726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008534"
---
# <a name="decryptmessage-kerberos-function"></a>Função DecryptMessage (Kerberos)

A função **DecryptMessage (Kerberos)** descriptografa uma mensagem. Alguns pacotes não criptografam e descriptografam mensagens, mas executam e verificam um [*hash*](../secgloss/h-gly.md)de integridade.

> [!Note]  
> [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md) e **DecryptMessage (Kerberos)** podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ), se um thread estiver Criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

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

Um identificador para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para descriptografar a mensagem.

*PMessage* \[ entrada, saída\]

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que podem ser do tipo \_ dados SecBuffer. O buffer contém a mensagem criptografada. A mensagem criptografada é descriptografada no local, substituindo o conteúdo original de seu buffer.

*MessageSeqNo* \[ no\]

O número de sequência esperado pelo aplicativo de transporte, se houver. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser definido como zero.

*pfQOP* \[ fora\]

Um ponteiro para uma variável do tipo **ULONG** que recebe sinalizadores específicos do pacote que indicam a qualidade da proteção.

Esse parâmetro pode ser o sinalizador a seguir.

| Valor                  | Significado                                                             |
|------------------------|---------------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | Ela não foi criptografada, mas um cabeçalho ou trailer foi produzido. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.

## <a name="return-value"></a>Valor retornado

Se a função verificar que a mensagem foi recebida na sequência correta, a função retornará s \_ E \_ OK.

Se a função falhar ao descriptografar a mensagem, ela retornará um dos seguintes códigos de erro.

| Código de retorno                     | Descrição                                                                                                                                                                      |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ mensagem incompleta \_** | Os dados no buffer de entrada estão incompletos. O aplicativo precisa ler mais dados do servidor e chamar [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) novamente. |
| **s \_ E \_ fora \_ de \_ sequência**   | A mensagem não foi recebida na sequência correta.                                                                                                                            |

## <a name="remarks"></a>Comentários

Às vezes, um aplicativo lerá os dados da parte remota, tentará descriptografá-los usando **DecryptMessage (Kerberos)** e descobrirá que o **DecryptMessage (Kerberos)** foi bem-sucedido, mas os buffers de saída estão vazios. Esse comportamento é normal e os aplicativos devem ser capazes de lidar com eles.

Para obter informações sobre a interoperação com o GSSAPI, consulte [interoperabilidade entre SSPI/Kerberos com GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).

**Windows XP:** Essa função também era conhecida como **UnsealMessage**. Os aplicativos agora devem usar somente **DecryptMessage (Kerberos)** .

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte | Windows \[Somente aplicativos da área de trabalho XP\]          |
| Servidor mínimo com suporte | Windows \[Somente aplicativos da área de trabalho do servidor 2003\] |
| Cabeçalho                   | SSPI. h (incluir Security. h)               |
| Biblioteca                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Confira também

- [Funções SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

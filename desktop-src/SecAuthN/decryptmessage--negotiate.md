---
description: Descriptografa uma mensagem usando Negotiate.
ms.assetid: 188341ff-4e67-481e-af30-7f9913b1d24e
title: Função DecryptMessage (Negotiate)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 7da05842fc5aba4dc9c19cd530b38e0d46b640aac10b4614981c30c8863d7e7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008514"
---
# <a name="decryptmessage-negotiate-function"></a>Função DecryptMessage (Negotiate)

A função **DecryptMessage (Negotiate)** descriptografa uma mensagem. Alguns pacotes não criptografam e descriptografam mensagens, mas executam e verificam um [*hash*](../secgloss/h-gly.md)de integridade.

> [!Note]  
> [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) e **DecryptMessage (Negotiate)** podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ), se um thread estiver Criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

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

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Pelo menos um deles deve ser do tipo dados SECBUFFER \_ . Esse buffer contém a mensagem criptografada. A mensagem criptografada é descriptografada no local, substituindo o conteúdo original de seu buffer.

*MessageSeqNo* \[ no\]

O número de sequência esperado pelo aplicativo de transporte, se houver. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser definido como zero.

*pfQOP* \[ fora\]

Um ponteiro para uma variável do tipo **ULONG** que recebe sinalizadores específicos do pacote que indicam a qualidade da proteção.

Esse parâmetro pode ser o sinalizador a seguir.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valor</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>A mensagem não foi criptografada, mas um cabeçalho ou trailer foi produzido.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Valor retornado

Se a função verificar que a mensagem foi recebida na sequência correta, a função retornará s \_ E \_ OK.

Se a função falhar ao descriptografar a mensagem, ela retornará um dos seguintes códigos de erro.

| Código de retorno                     | Descrição                                                                                                                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ mensagem incompleta \_** | Os dados no buffer de entrada estão incompletos. O aplicativo precisa ler mais dados do servidor e chamar [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) novamente. |
| **s \_ E \_ fora \_ de \_ sequência**   | A mensagem não foi recebida na sequência correta.                                                                                                                              |

## <a name="remarks"></a>Comentários

Às vezes, um aplicativo lerá os dados da parte remota, tentará descriptografá-los usando **DecryptMessage (Negotiate)** e descobrirá que o **DecryptMessage (Negotiate)** foi bem-sucedido, mas os buffers de saída estão vazios. Esse comportamento é normal e os aplicativos devem ser capazes de lidar com eles.

**Windows XP:** Essa função também era conhecida como **UnsealMessage**. Os aplicativos agora devem usar apenas **DecryptMessage (Negotiate)** .

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
- [**EncryptMessage (negociar)**](encryptmessage--negotiate.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

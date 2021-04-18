---
description: Descriptografa uma mensagem usando NTLM.
ms.assetid: 44c63152-507d-4769-9c0c-d275d2b0deac
title: Função DecryptMessage (NTLM)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 707f1bcd9ae697de0c3e23529fe2857f58d0e5e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780734"
---
# <a name="decryptmessage-ntlm-function"></a>Função DecryptMessage (NTLM)

A função **DecryptMessage (NTLM)** descriptografa uma mensagem. Alguns pacotes não criptografam e descriptografam mensagens, mas executam e verificam um [*hash*](../secgloss/h-gly.md)de integridade.

> [!Note]  
> [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md) e **DecryptMessage (NTLM)** podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ), se um thread estiver Criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

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

## <a name="return-value"></a>Retornar valor

Se a função verificar que a mensagem foi recebida na sequência correta, a função retornará s \_ E \_ OK.

Se a função falhar ao descriptografar a mensagem, ela retornará um dos seguintes códigos de erro.

| Código de retorno                     | Descrição                                                                                                                                                              |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ mensagem incompleta \_** | Os dados no buffer de entrada estão incompletos. O aplicativo precisa ler mais dados do servidor e chamar [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) novamente. |
| **s \_ E \_ fora \_ de \_ sequência**   | A mensagem não foi recebida na sequência correta.                                                                                                                    |

## <a name="remarks"></a>Comentários

Às vezes, um aplicativo lerá os dados da parte remota, tentará descriptografá-los usando **DecryptMessage (NTLM)** e descobrirá que o **DecryptMessage (NTLM)** foi bem-sucedido, mas os buffers de saída estão vazios. Esse comportamento é normal e os aplicativos devem ser capazes de lidar com eles.

**Windows XP:** Essa função também era conhecida como **UnsealMessage**. Os aplicativos agora devem usar somente **DecryptMessage (NTLM)** .

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
- [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

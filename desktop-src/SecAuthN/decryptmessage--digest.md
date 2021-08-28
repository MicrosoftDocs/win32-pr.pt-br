---
description: Descriptografa uma mensagem usando Digest.
ms.assetid: 46d45f59-33fa-434a-b329-20b6257c9a19
title: Função DecryptMessage (Digest)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f87828263766643a10cf5400e38cabe9d3096403
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480862"
---
# <a name="decryptmessage-digest-function"></a>Função DecryptMessage (Digest)

A função **DecryptMessage (Digest)** descriptografa uma mensagem. Alguns pacotes não criptografam e descriptografam mensagens, mas executam e verificam um [*hash*](../secgloss/h-gly.md)de integridade.

O SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) Digest fornece criptografia e confidencialidade para mensagens trocadas entre o cliente e o servidor como um mecanismo SASL apenas.

> [!Note]  
> [**EncryptMessage (Digest)**](encryptmessage--digest.md) e **DecryptMessage (Digest)** podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ) se um thread estiver Criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

## <a name="syntax"></a>Sintaxe

```C++
SECURITY_STATUS SEC_ENTRY DecryptMessage(
  PCtxtHandle    phContext,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo,
  unsigned long  *pfQOP
);
```

## <a name="parameters"></a>Parâmetros

*phContext* \[ no\]

Um identificador para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para descriptografar a mensagem.

*PMessage* \[ entrada, saída\]

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Pelo menos um deles deve ser do tipo dados SECBUFFER \_ . Esse buffer contém a mensagem criptografada. A mensagem criptografada é descriptografada no local, substituindo o conteúdo original de seu buffer.

Ao usar o SSP de resumo, na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Um deles deve ser do tipo SECBUFFER \_ data ou SECBUFFER \_ Stream e deve conter a mensagem criptografada.

*MessageSeqNo* \[ no\]

O número de sequência esperado pelo aplicativo de transporte, se houver. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser definido como zero.

Ao usar o SSP de resumo, esse parâmetro deve ser definido como zero. O SSP de resumo gerencia a numeração de sequência internamente.

*pfQOP* \[ fora\]

Um ponteiro para uma variável do tipo **ULONG** que recebe sinalizadores específicos do pacote que indicam a qualidade da proteção.

Esse parâmetro pode ser um dos sinalizadores a seguir.


| Valor | Significado | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | A mensagem não foi criptografada, mas um cabeçalho ou trailer foi produzido.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</blockquote><br /> | 
| <span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl><dt><strong>SIGN_ONLY</strong></dt></dl> | Ao usar o SSP de resumo, use esse sinalizador quando o [*contexto de segurança*](../secgloss/s-gly.md) for definido para verificar apenas a [*assinatura*](../secgloss/s-gly.md) . Para obter mais informações, consulte [qualidade de proteção](quality-of-protection.md).<br /> | 


## <a name="return-value"></a>Valor retornado

Se a função verificar que a mensagem foi recebida na sequência correta, a função retornará s \_ E \_ OK.

Se a função falhar ao descriptografar a mensagem, ela retornará um dos seguintes códigos de erro.

| Código de retorno                         | Descrição                                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ buffer \_ muito \_ pequeno**      | O buffer de mensagens é muito pequeno. Usado com o SSP de resumo.                                                                                                                   |
| **s \_ E \_ sistema de criptografia \_ \_ inválidos** | Não há suporte para a [*codificação*](../secgloss/c-gly.md) escolhida para o [*contexto de segurança*](../secgloss/s-gly.md) . Usado com o SSP de resumo.                                                                                       |
| **s \_ E \_ mensagem incompleta \_**     | Os dados no buffer de entrada estão incompletos. O aplicativo precisa ler mais dados do servidor e chamar [**DecryptMessage (Digest)**](decryptmessage--digest.md) novamente. |
| **s \_ E \_ \_ identificador inválido**         | Um identificador de contexto inválido foi especificado no parâmetro *phContext* . Usado com o SSP de resumo.                                                                     |
| **s \_ E \_ mensagem \_ alterada**        | A mensagem foi alterada. Usado com o SSP de resumo.                                                                                                                      |
| **s \_ E \_ fora \_ de \_ sequência**       | A mensagem não foi recebida na sequência correta.                                                                                                                        |
| **s \_ E \_ QOP \_ não \_ têm suporte**     | Nenhuma confidencialidade nem [*integridade*](../secgloss/i-gly.md) têm suporte no [*contexto de segurança*](../secgloss/s-gly.md). Usado com o SSP de resumo.                           |

## <a name="remarks"></a>Comentários

Às vezes, um aplicativo lerá os dados da parte remota, tentará descriptografá-los usando **DecryptMessage (Digest)** e descobrirá que o **DecryptMessage (Digest)** foi bem-sucedido, mas os buffers de saída estão vazios. Esse comportamento é normal e os aplicativos devem ser capazes de lidar com eles.

**Windows XP:** Essa função também era conhecida como **UnsealMessage**. Os aplicativos agora devem usar apenas **DecryptMessage (Digest)** .

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|-------------------------------------------|
| Cliente mínimo com suporte | Windows \[Somente aplicativos da área de trabalho XP\]          |
| Servidor mínimo com suporte | Windows \[Somente aplicativos da área de trabalho do servidor 2003\] |
| Cabeçalho                   | SSPI. h (incluir Security. h)               |
| Biblioteca                  | Secur32. lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Confira também

- [Funções SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (resumo)**](encryptmessage--digest.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

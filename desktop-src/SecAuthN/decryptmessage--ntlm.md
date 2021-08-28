---
description: Descriptografa uma mensagem usando NTLM.
ms.assetid: 44c63152-507d-4769-9c0c-d275d2b0deac
title: Função DecryptMessage (NTLM)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: f73159c1b6e9fbe3d6d9c282ffdb05271e29583b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481042"
---
# <a name="decryptmessage-ntlm-function"></a>Função DecryptMessage (NTLM)

A **função DecryptMessage (NTLM)** descriptografa uma mensagem. Alguns pacotes não criptografam e descriptografam mensagens, mas executam e verificam um [*hash de integridade*](../secgloss/h-gly.md).

> [!Note]  
> [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md) e **DecryptMessage (NTLM)** podem ser chamados ao mesmo tempo de dois threads diferentes em um contexto de SSPI [*(interface*](../secgloss/s-gly.md) de provedor de suporte de segurança única) se um thread estiver criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

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

*phContext* \[ Em\]

Um handle para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para descriptografar a mensagem.

*pMessage* \[ in, out\]

Um ponteiro para uma [**estrutura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Na entrada, a estrutura faz referência a uma ou mais [**estruturas SecBuffer.**](/windows/win32/api/sspi/ns-sspi-secbuffer) Pelo menos um deles deve ser do tipo SECBUFFER \_ DATA. Esse buffer contém a mensagem criptografada. A mensagem criptografada é descriptografada no local, sobrescrevendo o conteúdo original de seu buffer.

*MessageSeqNo* \[ Em\]

O número de sequência esperado pelo aplicativo de transporte, se for o caso. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser definido como zero.

*pfQOP* \[ out\]

Um ponteiro para uma variável do tipo **ULONG** que recebe sinalizadores específicos do pacote que indicam a qualidade da proteção.

Esse parâmetro pode ser o sinalizador a seguir.


| Valor | Significado | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | A mensagem não foi criptografada, mas um header ou um trailer foi produzido.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</blockquote><br /> | 


## <a name="return-value"></a>Valor retornado

Se a função verificar se a mensagem foi recebida na sequência correta, a função retornará SEC \_ E \_ OK.

Se a função não conseguir descriptografar a mensagem, ela retornará um dos códigos de erro a seguir.

| Código de retorno                     | Descrição                                                                                                                                                              |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MENSAGEM \_ INCOMPLETA DO SEC E \_ \_** | Os dados no buffer de entrada estão incompletos. O aplicativo precisa ler mais dados do servidor e chamar [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md) novamente. |
| **S \_ E FORA DE \_ \_ \_ SEQUÊNCIA**   | A mensagem não foi recebida na sequência correta.                                                                                                                    |

## <a name="remarks"></a>Comentários

Às vezes, um aplicativo lerá dados da parte remota, tentará descriptografá-los usando **DecryptMessage (NTLM)** e descobrirá que **DecryptMessage (NTLM)** foi bem-sucedido, mas os buffers de saída estão vazios. Esse é um comportamento normal e os aplicativos devem ser capazes de lidar com ele.

**Windows XP:** Essa função também era conhecida como **UnsealMessage.** Os aplicativos agora devem usar **apenas DecryptMessage (NTLM).**

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|-------------------------------------------|
| Cliente mínimo com suporte | Windows Somente \[ aplicativos da área de trabalho XP\]          |
| Servidor mínimo com suporte | Windows Somente aplicativos da área de trabalho server 2003 \[\] |
| Cabeçalho                   | Sspi.h (inclua Security.h)               |
| Biblioteca                  | Secur32.lib                               |
| DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Confira também

- [Funções SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)
- [**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**Secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)

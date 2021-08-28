---
description: Criptografa uma mensagem para fornecer privacidade usando Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: Função EncryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 89c6504fe8518e1c43d155ebce638dec1acfeb80
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476212"
---
# <a name="encryptmessage-kerberos-function"></a>Função EncryptMessage (Kerberos)

A **função EncryptMessage (Kerberos)** criptografa uma mensagem para fornecer [*privacidade.*](../secgloss/p-gly.md) **EncryptMessage (Kerberos)** permite que um aplicativo escolha entre [*algoritmos criptográficos*](../secgloss/c-gly.md) com suporte pelo mecanismo escolhido. A **função EncryptMessage (Kerberos)** usa o [*contexto de*](../secgloss/s-gly.md) segurança referenciado pelo handle de contexto. Alguns pacotes não têm mensagens a serem criptografadas ou descriptografadas, mas fornecem um hash de [*integridade*](../secgloss/h-gly.md) que pode ser verificado.

> [!Note]  
> **EncryptMessage (Kerberos)** e [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) podem ser chamados ao mesmo tempo de dois threads diferentes em um contexto de SSPI [*(interface*](../secgloss/s-gly.md) de provedor de suporte de segurança única) se um thread estiver criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

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

*phContext* \[ Em\]
</dt> <dd>

Um handle para o [*contexto de segurança*](../secgloss/s-gly.md) a ser usado para criptografar a mensagem.

</dd> <dt>

*fQOP* \[ Em\]
</dt> <dd>

Sinalizadores específicos do pacote que indicam a qualidade da proteção. Um [*pacote de segurança*](../secgloss/s-gly.md) pode usar esse parâmetro para habilitar a seleção de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Esse parâmetro pode ser o sinalizador a seguir.


| Valor | Significado | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Produza um header ou um trailer, mas não criptografe a mensagem.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT tem o mesmo valor e o mesmo significado.</blockquote><br /> | 


</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Um ponteiro para uma [**estrutura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que podem ser do tipo SECBUFFER \_ DATA. Esse buffer contém a mensagem a ser criptografada. A mensagem é criptografada no local, sobrescrevendo o conteúdo original da estrutura.

A função não processa buffers com o atributo SECBUFFER \_ READONLY.

O comprimento da estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contém a mensagem não deve ser maior que **cbMaximumMessage**, que é obtido da função [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) (SECPKG \_ ATTR \_ STREAM \_ SIZES).

Os aplicativos que não usam SSL devem fornecer [**um SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) do tipo SECBUFFER \_ PADDING.

</dd> <dt>

*MessageSeqNo* \[ Em\]
</dt> <dd>

O número de sequência que o aplicativo de transporte atribuiu à mensagem. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função retornará SEC \_ E \_ OK.

Se a função falhar, ela retornará um dos códigos de erro a seguir.

| Código de retorno                                                                                                    | Descrição                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ E BUFFER MUITO \_ \_ \_ PEQUENO**</dt> </dl>      | O buffer de saída é muito pequeno. Para obter mais informações, consulte Comentários.                                                                                                                                                                 |
| <dl> <dt>**CONTEXTO \_ SEC E \_ \_ EXPIRADO**</dt> </dl>        | O aplicativo está referenciando um contexto que já foi fechado. Um aplicativo escrito corretamente não deve receber esse erro.                                                                                               |
| <dl> <dt>**SISTEMA \_ DE CRIPTOGRAFIA SEC E \_ \_ \_ INVÁLIDO**</dt> </dl> | Não [*há*](../secgloss/c-gly.md) suporte para a [*codificação*](../secgloss/s-gly.md) escolhida para o contexto de segurança.                                                                                                         |
| <dl> <dt>**S \_ E \_ MEMÓRIA \_ INSUFICIENTE**</dt> </dl>    | Não há memória suficiente disponível para concluir a ação solicitada.                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ INVALID \_ HANDLE**</dt> </dl>         | Um alça de contexto que não é válido foi especificado no *parâmetro phContext.*                                                                                                                                                     |
| <dl> <dt>**SEC \_ E \_ TOKEN \_ INVÁLIDO**</dt> </dl>          | Nenhum buffer de tipo \_ DE DADOS SECBUFFER foi encontrado.                                                                                                                                                                                          |
| <dl> <dt>**SEC \_ E \_ QOP NÃO TEM \_ \_ SUPORTE**</dt> </dl>     | Não há suporte [*para*](../secgloss/i-gly.md) confidencialidade nem integridade no contexto de [*segurança*](../secgloss/s-gly.md). |

## <a name="remarks"></a>Comentários

A **função EncryptMessage (Kerberos)** criptografa uma mensagem com base na mensagem e na chave de [*sessão*](../secgloss/s-gly.md) de um contexto [*de segurança*](../secgloss/s-gly.md).

Se o aplicativo [](../secgloss/s-gly.md) de transporte criou o contexto de segurança para dar suporte à detecção de sequência e o chamador fornece um número de sequência, a função inclui essas informações com a mensagem criptografada. Incluir essas informações protege contra reprodução, inserção e supressão de mensagens. O [*pacote de segurança*](../secgloss/s-gly.md) incorpora o número de sequência passado do aplicativo de transporte.

> [!Note]  
> Esses buffers devem ser fornecidos na ordem mostrada.

| Tipo de buffer                           | Descrição                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| < SECBUFFER \_ STREAM \_  | Usado internamente. Nenhuma inicialização é necessária.                                                                       |
| DADOS \_ SECBUFFER            | Contém a [*mensagem de texto não*](../secgloss/s-gly.md) criptografado a ser criptografada. |
| SECBUFFER \_ STREAM \_ TRAILER | Usado internamente. Nenhuma inicialização é necessária.                                                                        |
| SECBUFFER \_ VAZIO           | Usado internamente. Nenhuma inicialização é necessária. O tamanho pode ser zero.                                                      |

Para obter um desempenho ideal, as *estruturas pMessage* devem ser alocadas da memória contígua.

**Windows XP:** Essa função também era conhecida como **SealMessage.** Os aplicativos agora devem **usar somente EncryptMessage (Kerberos).**

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|-------------------------------------------|
| Cliente mínimo com suporte | Windows Somente \[ aplicativos da área de trabalho XP\]          |
| Servidor mínimo com suporte | Windows Somente aplicativos da área de trabalho server 2003 \[\] |
| Cabeçalho                   | Sspi.h (inclua Security.h)               |
| Biblioteca                  | Secur32.lib                               |
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

[**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**Secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

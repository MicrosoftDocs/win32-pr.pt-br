---
description: Criptografa uma mensagem para fornecer privacidade usando Digest.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: Função EncryptMessage (Digest) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13bcaa5b91f165321d03e229416741b90a978dc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773921"
---
# <a name="encryptmessage-digest-function"></a>Função EncryptMessage (Digest)

A função **EncryptMessage (Digest)** criptografa uma mensagem para fornecer [*privacidade*](../secgloss/p-gly.md). **EncryptMessage (Digest)** permite que o aplicativo escolha entre [*algoritmos de criptografia*](../secgloss/c-gly.md) com suporte no mecanismo escolhido. A função **EncryptMessage (Digest)** usa o [*contexto de segurança*](../secgloss/s-gly.md) referenciado pelo identificador de contexto. Alguns pacotes não têm mensagens a serem criptografadas ou descriptografadas, mas fornecem um [*hash*](../secgloss/h-gly.md) de integridade que pode ser verificado.

Essa função está disponível apenas como um mecanismo SASL.

> [!Note]  
> **EncryptMessage (Digest)** e [**DecryptMessage (Digest)**](decryptmessage--digest.md) podem ser chamados ao mesmo tempo de dois threads diferentes em um único contexto SSPI ( [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) ) se um thread estiver Criptografando e o outro estiver descriptografando. Se mais de um thread estiver criptografando ou se mais de um thread estiver descriptografando, cada thread deverá obter um contexto exclusivo.

 

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
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

Ao usar o SSP de resumo, esse parâmetro deve ser definido como zero.

</dd> <dt>

*PMessage* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . Na entrada, a estrutura faz referência a uma ou mais estruturas [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que podem ser do tipo \_ dados SecBuffer. Esse buffer contém a mensagem a ser criptografada. A mensagem é criptografada no local, substituindo o conteúdo original da estrutura.

A função não processa buffers com o \_ atributo ReadOnly SECBUFFER.

O comprimento da estrutura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contém a mensagem não deve ser maior que **cbMaximumMessage**, que é obtido da função [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) (SECPKG de \_ fluxo de attr) \_ \_ .

Ao usar o SSP de resumo, deve haver um segundo buffer do tipo SECBUFFER \_ Padding ou \_ os dados de buffer de s \_ para manter as informações de [*assinatura*](../secgloss/d-gly.md#_security_digital_signature_gly) . Para obter o tamanho do buffer de saída, chame a função [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) e especifique os \_ tamanhos de attr SECPKG \_ . A função retornará uma estrutura [**de \_ tamanhos de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . O tamanho do buffer de saída é a soma dos valores nos membros **cbMaxSignature** e **cbBlockSize** .

Os aplicativos que não usam SSL devem fornecer um [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) do tipo \_ preenchimento SecBuffer.

</dd> <dt>

*MessageSeqNo* \[ no\]
</dt> <dd>

O número de sequência que o aplicativo de transporte atribuiu à mensagem. Se o aplicativo de transporte não mantiver números de sequência, esse parâmetro deverá ser zero.

Ao usar o SSP de resumo, esse parâmetro deve ser definido como zero. O SSP de resumo gerencia a numeração de sequência internamente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará s \_ E \_ OK.

Se a função falhar, ela retornará um dos seguintes códigos de erro.



| Código de retorno                                                                                                    | Description                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**s \_ E \_ buffer \_ muito \_ pequeno**</dt> </dl>      | O buffer de saída é muito pequeno. Para obter mais informações, consulte Comentários.<br/>                                                                                                                                                                 |
| <dl> <dt>**o \_ contexto s E \_ \_ expirou**</dt> </dl>        | O aplicativo está fazendo referência a um contexto que já foi fechado. Um aplicativo escrito corretamente não deve receber esse erro.<br/>                                                                                               |
| <dl> <dt>**s \_ E \_ sistema de criptografia \_ \_ inválidos**</dt> </dl> | Não há suporte para a [*codificação*](../secgloss/c-gly.md) escolhida para o [*contexto de segurança*](../secgloss/s-gly.md) .<br/>                                                                                                         |
| <dl> <dt>**s \_ E \_ memória insuficiente \_**</dt> </dl>    | Não há memória suficiente disponível para concluir a ação solicitada.<br/>                                                                                                                                                             |
| <dl> <dt>**s \_ E \_ \_ identificador inválido**</dt> </dl>         | Um identificador de contexto inválido foi especificado no parâmetro *phContext* .<br/>                                                                                                                                                     |
| <dl> <dt>**s \_ E \_ \_ token inválido**</dt> </dl>          | Nenhum \_ buffer de tipo de dados SECBUFFER foi encontrado.<br/>                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ QOP \_ não \_ têm suporte**</dt> </dl>     | Nenhuma confidencialidade nem [*integridade*](../secgloss/i-gly.md) têm suporte no [*contexto de segurança*](../secgloss/s-gly.md).<br/> |



 

## <a name="remarks"></a>Comentários

A função **EncryptMessage (Digest)** criptografa uma mensagem com base na mensagem e na [*chave de sessão*](../secgloss/s-gly.md) de um [*contexto de segurança*](../secgloss/s-gly.md).

Se o aplicativo de transporte criou o [*contexto de segurança*](../secgloss/s-gly.md) para dar suporte à detecção de sequência e o chamador fornecer um número de sequência, a função incluirá essas informações com a mensagem criptografada. A inclusão dessas informações protege contra reprodução, inserção e supressão de mensagens. O [*pacote de segurança*](../secgloss/s-gly.md) incorpora o número de sequência passado do aplicativo de transporte.

Ao usar o SSP de resumo, obtenha o tamanho do buffer de saída chamando a função [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) e especificando os \_ tamanhos de attr SECPKG \_ . A função retornará uma estrutura [**de \_ tamanhos de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . O tamanho do buffer de saída é a soma dos valores nos membros **cbMaxSignature** e **cbBlockSize** .

> [!Note]  
> Esses buffers devem ser fornecidos na ordem mostrada.

 



| Tipo de buffer                           | Description                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| \_cabeçalho de fluxo de SECBUFFER \_<br/>  | Usado internamente. Nenhuma inicialização é necessária.<br/>                                                                        |
| dados do SECBUFFER \_<br/>            | Contém a mensagem de [*texto sem formatação*](../secgloss/s-gly.md) a ser criptografada.<br/> |
| \_trailer de fluxo de SECBUFFER \_<br/> | Usado internamente. Nenhuma inicialização é necessária.<br/>                                                                        |
| SECBUFFER \_ vazio<br/>           | Usado internamente. Nenhuma inicialização é necessária. O tamanho pode ser zero.<br/>                                                      |



 

Para um desempenho ideal, as estruturas *PMessage* devem ser alocadas da memória contígua.

**Windows XP:** Essa função também era conhecida como **SealMessage**. Os aplicativos agora devem usar apenas **EncryptMessage (Digest)** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (resumo)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**DecryptMessage (resumo)**](decryptmessage--digest.md)
</dt> <dt>

[**InitializeSecurityContext (resumo)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**QueryContextAttributes (resumo)**](querycontextattributes--digest.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 

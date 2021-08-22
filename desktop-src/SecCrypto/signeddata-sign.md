---
description: Cria uma assinatura digital no conteúdo a ser assinado. Uma assinatura digital consiste em um hash do conteúdo a ser assinado que é criptografado usando a chave privada do signante.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: Método SignedData.Sign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6ead7fb1c96b05d6945bb67937b215fd6d5d2422041250bee18e4be26edb2f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899014"
---
# <a name="signeddatasign-method"></a>Método SignedData.Sign

\[O **método** Sign está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Em vez disso, use [**a Classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

O **método Sign** cria uma assinatura [*digital*](../secgloss/d-gly.md) no conteúdo a ser assinado. Uma assinatura digital consiste em [*um hash*](../secgloss/h-gly.md) do conteúdo a ser assinado que é criptografado usando a chave privada do signante. Esse método só pode ser usado depois que a [**propriedade SignedData.Content**](signeddata-content.md) tiver sido inicializada. Se o **método Sign** for chamado em um objeto que já tem uma assinatura, a assinatura antiga será substituída. A assinatura é criada usando o algoritmo de assinatura SHA1.

## <a name="syntax"></a>Sintaxe


```VB
SignedData.Sign( _
  [ ByVal Signer ], _
  [ ByVal bDetached ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Signer* \[ in, opcional\]
</dt> <dd>

Uma referência ao [**objeto Signer**](signer.md) do signante dos dados. O **objeto Signer** deve ter acesso à [*chave privada*](../secgloss/p-gly.md) do [*certificado*](../secgloss/c-gly.md) usado para assinar. Esse parâmetro pode ser **NULL;** Para obter mais informações, consulte Comentários.

</dd> <dt>

*bDetached* \[ in, opcional\]
</dt> <dd>

Se **True**, os dados a serem assinados serão desvinculados; ou seja, o conteúdo assinado não está incluído como parte do objeto assinado. Para verificar a assinatura no conteúdo desvinculado, um aplicativo deve ter uma cópia do conteúdo original. O conteúdo desvinculado geralmente é usado para diminuir o tamanho de um objeto assinado a ser enviado pela Web, se o destinatário da mensagem assinada tiver uma cópia original dos dados assinados. O valor padrão é **Falso**.

</dd> <dt>

*EncodingType* \[ in, opcional\]
</dt> <dd>

Um valor da [enumeração CAPICOM \_ ENCODING \_ TYPE](capicom-encoding-type.md) que indica como os dados assinados devem ser codificados. O valor padrão é CAPICOM \_ ENCODE \_ BASE64. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CODIFICAR QUALQUER \_ CAPICOM \_**</dt> </dl>          | Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido. Se esse valor for usado para especificar o tipo de codificação da saída, CAPICOM \_ ENCODE \_ BASE64 será usado. Introduzido no CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CODIFICAÇÃO CAPICOM \_ \_ BASE64**</dt> </dl> | Os dados são salvos como uma cadeia de caracteres codificada em base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**BINÁRIO DE CODIFICAÇÃO CAPICOM \_ \_**</dt> </dl> | Os dados são salvos como uma sequência binária pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna uma cadeia de caracteres que contém os dados codificados e assinados.

Se esse método falhar, um erro será lançado. O **objeto Err** conterá informações adicionais sobre o erro.

## <a name="remarks"></a>Comentários

> [!IMPORTANT]
> Quando esse método é chamado de um script Web, o script precisa usar sua chave privada para criar uma assinatura digital. Permitir que sites não confiáveis usem sua chave privada é um risco de segurança. Uma caixa de diálogo que pergunta se o site pode usar sua chave privada é exibida quando esse método é chamado pela primeira vez. Se você permitir que o script use sua chave privada para criar uma assinatura digital e selecionar "Não mostrar esta caixa de diálogo novamente", a caixa de diálogo não será mais exibida para nenhum script dentro desse domínio que use sua chave privada para criar uma assinatura digital. No entanto, scripts fora desse domínio que tentam usar sua chave privada para criar uma assinatura digital ainda fará com que essa caixa de diálogo apareça. Se você não permitir que o script use sua chave privada e selecionar "Não mostrar essa caixa de diálogo novamente", os scripts dentro desse domínio serão recusados automaticamente a capacidade de usar sua chave privada para criar assinaturas digitais.

 

Como a criação de uma assinatura [*digital*](../secgloss/d-gly.md) requer o uso de uma chave [*privada,*](../secgloss/p-gly.md)os aplicativos baseados na Web que tentam usar esse método exigirão prompts de interface do usuário que permitem que o usuário aprove o uso da chave privada, por motivos de segurança.

Os seguintes resultados se aplicam ao *valor do parâmetro Signer:*

-   Se o *parâmetro Signer* não for **NULL,** esse método usará a chave privada apontada pelo certificado associado para criptografar a assinatura. Se a chave privada apontada pelo certificado não estiver disponível, o método falhará.
-   Se o *parâmetro Signer* for **NULL** e houver exatamente um certificado no armazenamento MY DO USUÁRIO ATUAL que tenha acesso a uma chave privada, esse certificado será usado para \_ criar a assinatura.
-   Se o *parâmetro Signer* for **NULL,** o [**Configurações. O valor da propriedade EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) é true e há mais de um certificado no armazenamento MY DO USUÁRIO ATUAL com uma chave privada disponível, uma caixa de diálogo é exibida que permite que o usuário selecione qual certificado \_ é usado.
-   Se o *parâmetro Signer* for **NULL** e o [**Configurações. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) propriedade é false, o método falha.
-   Se o *parâmetro Signer* for **NULL** e não houver nenhum certificado no armazenamento MY DO USUÁRIO ATUAL com uma chave privada \_ disponível, o método falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 

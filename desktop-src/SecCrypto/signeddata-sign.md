---
description: Cria uma assinatura digital no conteúdo a ser assinado. Uma assinatura digital consiste em um hash do conteúdo a ser assinado que é criptografado usando a chave privada do Assinante.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: Método SignedData. Sign
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
ms.openlocfilehash: 9f885bb110b51264bc6108ca8c0f881cc48f7710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810506"
---
# <a name="signeddatasign-method"></a>Método SignedData. Sign

\[O método **Sign** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O método **Sign** cria uma [*assinatura digital*](../secgloss/d-gly.md) no conteúdo a ser assinado. Uma assinatura digital consiste em um [*hash*](../secgloss/h-gly.md) do conteúdo a ser assinado que é criptografado usando a chave privada do Assinante. Este método só pode ser usado depois que a propriedade [**SignedData. Content**](signeddata-content.md) tiver sido inicializada. Se o método **Sign** for chamado em um objeto que já tem uma assinatura, a assinatura antiga será substituída. A assinatura é criada usando o algoritmo de assinatura SHA1.

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

*Signatário* \[ em, opcional\]
</dt> <dd>

Uma referência ao objeto de [**signatário**](signer.md) do signatário dos dados. O objeto de **signatário** deve ter acesso à [*chave privada*](../secgloss/p-gly.md) do [*certificado*](../secgloss/c-gly.md) usado para assinar. Esse parâmetro pode ser **nulo**; para obter mais informações, consulte comentários.

</dd> <dt>

*bDetached* \[ em, opcional\]
</dt> <dd>

Se **for true**, os dados a serem assinados serão desanexados; ou seja, o conteúdo assinado não é incluído como parte do objeto assinado. Para verificar a assinatura no conteúdo desanexado, um aplicativo deve ter uma cópia do conteúdo original. O conteúdo desanexado é geralmente usado para diminuir o tamanho de um objeto assinado a ser enviado pela Web, se o destinatário da mensagem assinada tiver uma cópia original dos dados assinados. O valor padrão é **Falso**.

</dd> <dt>

*EncodingType* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [do \_ \_ tipo de codificação capicor](capicom-encoding-type.md) que indica como os dados assinados serão codificados. O valor padrão é CAPICOM de \_ codificação \_ base64. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ codificar \_ qualquer**</dt> </dl>          | Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido. Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar. Introduzido no CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ codificar \_ Base64**</dt> </dl> | Os dados são salvos como uma cadeia de caracteres codificada em base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**capicote de \_ codificação \_ binário**</dt> </dl> | Os dados são salvos como uma sequência binária pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma cadeia de caracteres que contém os dados codificados e assinados.

Se esse método falhar, um erro será gerado. O objeto **Err** conterá informações adicionais sobre o erro.

## <a name="remarks"></a>Comentários

> [!IMPORTANT]
> Quando esse método é chamado de um script da Web, o script precisa usar sua chave privada para criar uma assinatura digital. Permitir que sites não confiáveis usem sua chave privada é um risco de segurança. Uma caixa de diálogo que pergunta se o site pode usar sua chave privada é exibida quando esse método é chamado pela primeira vez. Se você permitir que o script Use sua chave privada para criar uma assinatura digital e selecionar "não mostrar esta caixa de diálogo novamente", a caixa de diálogo não será mais exibida para nenhum script dentro desse domínio que use sua chave privada para criar uma assinatura digital. No entanto, os scripts fora desse domínio que tentarem usar sua chave privada para criar uma assinatura digital ainda farão com que essa caixa de diálogo seja exibida. Se você não permitir que o script Use sua chave privada e selecionar "não mostrar esta caixa de diálogo novamente", os scripts nesse domínio serão recusados automaticamente a capacidade de usar sua chave privada para criar assinaturas digitais.

 

Como a criação de uma [*assinatura digital*](../secgloss/d-gly.md) requer o uso de uma [*chave privada*](../secgloss/p-gly.md), os aplicativos baseados na Web que tentarem usar esse método exigirão prompts de interface do usuário que permitam ao usuário aprovar o uso da chave privada, por motivos de segurança.

Os seguintes resultados se aplicam ao valor do parâmetro de *signatário* :

-   Se o parâmetro de *signatário* não for **nulo**, esse método usará a chave privada apontada pelo certificado associado para criptografar a assinatura. Se a chave privada apontada pelo certificado não estiver disponível, o método falhará.
-   Se o parâmetro de *signatário* for **nulo** e houver exatamente um certificado no usuário atual \_ meu repositório que tenha acesso a uma chave privada, esse certificado será usado para criar a assinatura.
-   Se o parâmetro de *signatário* for **nulo**, o valor da propriedade [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) for true e houver mais de um certificado no usuário atual \_ My Store com uma chave privada disponível, será exibida uma caixa de diálogo que permite ao usuário selecionar qual certificado será usado.
-   Se o parâmetro de *signatário* for **nulo** e a propriedade [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) for false, o método falhará.
-   Se o parâmetro de *signatário* for **nulo** e não houver nenhum certificado no \_ usuário atual, meu repositório com uma chave privada disponível, o método falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 

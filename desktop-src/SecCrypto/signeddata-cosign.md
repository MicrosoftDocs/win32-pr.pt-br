---
description: Cria uma assinatura digital no conteúdo assinado anteriormente.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: Método SignedData. cosign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ed4feb55420ebf9d3bc43496fe3004a4d1b55e1ae8add4e3d5b40ec2ac4ba4ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973886"
---
# <a name="signeddatacosign-method"></a>Método SignedData. cosign

\[O método de **coassinatura** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O método de **coassinatura** cria uma [*assinatura digital*](../secgloss/d-gly.md) no conteúdo assinado anteriormente.

## <a name="syntax"></a>Sintaxe


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Signatário* \[ em, opcional\]
</dt> <dd>

Uma referência ao objeto de [**signatário**](signer.md) do signatário dos dados. O objeto de **signatário** deve ter acesso à chave privada do certificado usado para assinar. Esse parâmetro pode ser **nulo**; para obter mais informações, consulte comentários.

</dd> <dt>

*EncodingType* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**do \_ \_ tipo de codificação capicor**](capicom-encoding-type.md) que indica como os dados assinados serão codificados. O valor padrão é CAPICOM de \_ codificação \_ base64. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ codificar \_ qualquer**</dt> </dl>          | Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido. Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar. Introduzido no CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ codificar \_ Base64**</dt> </dl> | Os dados são salvos como uma cadeia de caracteres codificada em base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**capicote de \_ codificação \_ binário**</dt> </dl> | Os dados são salvos como uma sequência binária pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna uma cadeia de caracteres que contém os dados codificados e assinados.

Se esse método falhar, um erro será gerado. O objeto **Err** conterá informações adicionais sobre o erro.

## <a name="remarks"></a>Comentários

> [!IMPORTANT]
> Quando esse método é chamado de um script da Web, o script precisa usar sua [*chave privada*](../secgloss/p-gly.md) para criar uma assinatura digital. Permitir que sites não confiáveis usem sua chave privada é um risco de segurança. Uma caixa de diálogo que pergunta se o site pode usar sua chave privada é exibida quando esse método é chamado pela primeira vez. Se você permitir que o script Use sua chave privada para criar uma assinatura digital e selecionar "não mostrar esta caixa de diálogo novamente", a caixa de diálogo não será mais exibida para nenhum script dentro desse domínio que use sua chave privada para criar uma assinatura digital. No entanto, os scripts fora desse domínio que tentarem usar sua chave privada para criar uma assinatura digital ainda farão com que essa caixa de diálogo seja exibida. Se você não permitir que o script Use sua chave privada e selecionar "não mostrar esta caixa de diálogo novamente", os scripts nesse domínio serão recusados automaticamente a capacidade de usar sua chave privada para criar assinaturas digitais.

 

Não há garantia de que os coassinados estejam em uma ordem específica.

Os seguintes resultados se aplicam ao valor do parâmetro de *signatário* :

-   Se o parâmetro de *signatário* não for **nulo**, esse método usará a chave privada apontada pelo certificado associado para criptografar a coassinatura. Se a chave privada apontada pelo certificado não estiver disponível, o método falhará.
-   Se o parâmetro de *signatário* for **nulo** e houver exatamente um certificado no usuário atual \_ meu repositório que tenha acesso a uma chave privada, esse certificado será usado para criar a coassinatura.
-   se o parâmetro de *signatário* for **nulo**, o [**Configurações.**](settings-enablepromptforcertificateui.md)O valor da propriedade EnablePromptForCertificateUI é true e há mais de um certificado no usuário atual \_ meu repositório com uma chave privada disponível, uma caixa de diálogo é exibida para permitir que o usuário selecione qual certificado será usado.
-   se o parâmetro de *signatário* for **nulo** e o [**Configurações.**](settings-enablepromptforcertificateui.md)A propriedade EnablePromptForCertificateUI é false, o método falha.
-   Se o parâmetro de *signatário* for **nulo** e não houver nenhum certificado no \_ usuário atual, meu repositório com uma chave privada disponível, o método falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 

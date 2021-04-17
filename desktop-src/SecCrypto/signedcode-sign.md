---
description: Cria uma assinatura digital Authenticode e assina o arquivo executável especificado na propriedade SignedCode. FileName.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: Método SignedCode. Sign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779941"
---
# <a name="signedcodesign-method"></a>Método SignedCode. Sign

\[O método **Sign** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) da API do Win32 para assinar conteúdo com uma assinatura digital Authenticode. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O método **Sign** cria uma assinatura digital Authenticode e assina o arquivo executável especificado na propriedade [**SignedCode. FileName**](signedcode-filename.md) .

## <a name="syntax"></a>Sintaxe


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Signatário* \[ em, opcional\]
</dt> <dd>

Um objeto de [**signatário**](signer.md) que tem acesso à chave privada do certificado usado para assinar o código. O valor padrão é **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Antes que o método **Sign** seja chamado, o arquivo que contém o código deve ser especificado na propriedade [**filename**](signedcode-filename.md) .

Se o arquivo executável já estiver assinado, esse método substituirá a assinatura existente.

Os seguintes resultados se aplicam ao valor do parâmetro de *signatário* :

-   Se o parâmetro de *signatário* não for **nulo**, esse método usará a chave privada apontada pelo certificado associado para criptografar a assinatura. Se a chave privada apontada pelo certificado não estiver disponível, o método falhará.
-   Se o parâmetro de *signatário* for **nulo** e houver exatamente um certificado no usuário atual \_ meu repositório que tenha acesso a uma chave privada com capacidade de assinatura de código, esse certificado será usado para criar a assinatura.
-   Se o parâmetro de *signatário* for **nulo**, o valor da propriedade [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) for true e houver mais de um certificado no usuário atual \_ My Store com uma chave privada disponível com o recurso de assinatura de código, será exibida uma caixa de diálogo que permite ao usuário selecionar qual certificado será usado.
-   Se o parâmetro de *signatário* for **nulo** e a propriedade [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) for false, o método falhará.
-   Se o parâmetro de *signatário* for **nulo** e não houver certificados no usuário atual \_ meu repositório com uma chave privada disponível com capacidade de assinatura de código, o método falhará.

Esse método usa o algoritmo de hash SHA-1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

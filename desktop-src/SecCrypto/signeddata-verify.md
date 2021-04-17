---
description: Determina se as assinaturas em dados assinados no objeto SignedData são válidas.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: Método SignedData. Verify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3cb48943a826296c13df80130171442fc29435f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769271"
---
# <a name="signeddataverify-method"></a>Método SignedData. Verify

\[O método **Verify** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O método **Verify** determina se as [*assinaturas*](../secgloss/d-gly.md) em dados assinados no objeto [**SignedData**](signeddata.md) são válidas. Para verificar uma assinatura, o [*hash*](../secgloss/h-gly.md) criptografado do conteúdo é descriptografado usando a chave pública do assinante do certificado do Assinante. O hash descriptografado é comparado com um novo hash do conteúdo de dados. Uma assinatura será válida se os hashes corresponderem. Além disso, esse método também cria uma cadeia de certificados para determinar a validade do certificado que fornece a [*chave pública*](../secgloss/p-gly.md) usada para descriptografar o hash.

## <a name="syntax"></a>Sintaxe


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SignedMessage* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que contém a mensagem assinada a ser verificada.

</dd> <dt>

*bDetached* \[ em, opcional\]
</dt> <dd>

Se **for true**, os dados a serem assinados serão desanexados; ou seja, o conteúdo assinado não é incluído como parte do objeto assinado. Para verificar a assinatura no conteúdo desanexado, um aplicativo deve ter uma cópia do conteúdo original. O conteúdo desanexado é geralmente usado para diminuir o tamanho de um objeto assinado a ser enviado pela Web, se o destinatário da mensagem assinada tiver uma cópia original dos dados assinados. O valor padrão é **Falso**.

</dd> <dt>

*VerifyFlag* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [de \_ \_ sinalizador de \_ verificação \_ de dados assinados capicor](capicom-signed-data-verify-flag.md) que indica a política de verificação. O valor padrão é capicot \_ verificar \_ assinatura \_ e \_ certificado. Usando esse valor, a validade do certificado e a validade da assinatura são verificadas. Esse parâmetro pode ser definido para verificar a assinatura e não o certificado. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                             | Significado                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <dt>**CAPICOM \_ verificar \_ \_ somente assinatura**</dt> </dl>                                   | Somente a assinatura é verificada.<br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <dt>**CAPICOM \_ verificar \_ assinatura \_ e \_ certificado**</dt> </dl> | A assinatura e a validade do certificado usado para criar a assinatura são verificadas.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma cadeia de caracteres que contém os dados codificados e assinados.

Se esse método falhar, um erro será gerado. O objeto **Err** conterá informações adicionais sobre o erro.

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

 

 

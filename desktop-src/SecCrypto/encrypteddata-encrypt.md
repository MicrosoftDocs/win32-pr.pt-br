---
description: Deriva uma chave de sessão do segredo e criptografa o valor da propriedade Content usando essa chave. Ele retorna o conteúdo criptografado como uma cadeia de caracteres codificada.
ms.assetid: aa6f6e6a-208b-4e9c-b530-08673ab9d794
title: Método EncryptedData. Encrypt (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 04d7bf8a337c1bcfa0a024b84304fe50c035f9dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757474"
---
# <a name="encrypteddataencrypt-method"></a>Método EncryptedData. Encrypt

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O método **Encrypt** deriva uma chave de sessão do segredo e criptografa o valor da propriedade [**Content**](encrypteddata-content.md) usando essa chave. Ele retorna o conteúdo criptografado como uma cadeia de caracteres codificada.

## <a name="syntax"></a>Sintaxe


```VB
EncryptedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EncodingType* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**do \_ \_ tipo de codificação capicor**](capicom-encoding-type.md) que indica o tipo de codificação usado para codificar os dados criptografados. O valor padrão é CAPICOM de \_ codificação \_ base64. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ codificar \_ qualquer**</dt> </dl>          | Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido. Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar. Introduzido no CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ codificar \_ Base64**</dt> </dl> | Os dados são salvos como uma cadeia de caracteres codificada em base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**capicote de \_ codificação \_ binário**</dt> </dl> | Os dados são salvos como uma sequência binária pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma cadeia de caracteres que contém os dados criptografados e codificados.

## <a name="remarks"></a>Comentários

Antes de chamar o método **Encrypt** , defina a propriedade [**Content**](encrypteddata-content.md) e chame o método [**setsecret**](encrypteddata-setsecret.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| parâmetro<br/>                | <dl> <dt>InfoCard. h</dt> </dl>  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 

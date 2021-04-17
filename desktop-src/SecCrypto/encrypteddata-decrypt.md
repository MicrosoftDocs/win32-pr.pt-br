---
description: Descriptografa uma cadeia de caracteres de dados criptografada e codificada.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: Método EncryptedData. Decrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aa702a5cefc46f6d0cbe5d7e0fba17ff03596b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747843"
---
# <a name="encrypteddatadecrypt-method"></a>Método EncryptedData. Decrypt

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O método **Decrypt** descriptografa uma cadeia de caracteres de dados criptografada e codificada. Os dados de texto sem formatação resultantes se tornam a propriedade [**Content**](encrypteddata-content.md) do objeto [**EncryptedData**](encrypteddata.md) . A descriptografia do conteúdo falha a menos que o segredo, definido pelo método [**setsecret**](encrypteddata-setsecret.md) , seja exatamente o mesmo que o segredo usado para derivar a chave usada para criptografar o conteúdo.

## <a name="syntax"></a>Sintaxe


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EncryptedMessage* \[ no\]
</dt> <dd>

Cadeia de caracteres que contém os dados codificados e criptografados a serem descriptografados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A chave de sessão derivada do segredo atual é usada para a descriptografia. Esse método não produzirá o texto não criptografado correto, a menos que o segredo atual corresponda exatamente ao segredo usado para criptografar a mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 

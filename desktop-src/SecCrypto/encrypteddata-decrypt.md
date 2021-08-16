---
description: Descriptografa uma cadeia de caracteres de dados criptografada e codificada.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: Método EncryptedData.Decrypt
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
ms.openlocfilehash: 8bf8a108efdc462a9f08a508a05b736817ec38ce43ee50dbd3fdd11aa2af9f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766692"
---
# <a name="encrypteddatadecrypt-method"></a>Método EncryptedData.Decrypt

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (Serviços de Invocação de Plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens. Para obter informações sobre o PInvoke, consulte [Tutorial de invocação de plataforma.](https://msdn.microsoft.com/library/aa288468.aspx) O .NET e a CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 e .NET e CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções da parte 2 de Estender a criptografia do .NET com [CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O **método Decrypt** descriptografa uma cadeia de caracteres de dados criptografada e codificada. Os dados de texto não criptografado resultantes se tornam [**a propriedade Content**](encrypteddata-content.md) do objeto [**EncryptedData.**](encrypteddata.md) A descriptografia do conteúdo falhará a menos que o segredo, definido pelo método [**SetSecret,**](encrypteddata-setsecret.md) seja exatamente o mesmo que o segredo usado para derivar a chave usada para criptografar o conteúdo.

## <a name="syntax"></a>Sintaxe


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EncryptedMessage* \[ Em\]
</dt> <dd>

Cadeia de caracteres que contém os dados codificados e criptografados a serem descriptografados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A chave de sessão derivada do segredo atual é usada para a descriptografia. Esse método não produzirá o texto não criptografado correto, a menos que o segredo atual corresponde exatamente ao segredo usado para criptografar a mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**Encrypteddata**](encrypteddata.md)
</dt> </dl>

 

 

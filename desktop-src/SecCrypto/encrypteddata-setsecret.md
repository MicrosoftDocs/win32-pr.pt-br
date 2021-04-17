---
description: Define o valor do segredo usado para derivar a chave de sessão criptográfica usada para criptografar e descriptografar dados.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: Método EncryptedData. setsecret
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787460"
---
# <a name="encrypteddatasetsecret-method"></a>Método EncryptedData. setsecret

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O método **setsecret** define o valor do segredo usado para derivar a [*chave de sessão*](../secgloss/s-gly.md) criptográfica usada para criptografar e descriptografar dados.

## <a name="syntax"></a>Sintaxe


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que contém um segredo usado para criar uma chave de criptografia de sessão.

</dd> <dt>

*Segredo* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**de \_ \_ tipo de segredo de CAPICOM**](capicom-secret-type.md) que indica o tipo de segredo usado para gerar a chave de sessão. O valor padrão é CAPICOM de \_ senha de segredo \_ . Esse parâmetro pode ser o valor a seguir.



| Valor                                                                                                                                                                                        | Significado                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <dt>**CAPICOM \_ \_ senha secreta**</dt> </dl> | A chave de criptografia deve ser derivada de uma senha.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O segredo é usado para criar a chave de sessão para criptografia ou descriptografia. O mesmo segredo deve ser usado para ambas as operações. Se o segredo usado para criptografar dados for perdido, os dados criptografados não poderão ser descriptografados.

Se apropriado para seu aplicativo, considere o uso de [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) ou [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) para proteger o segredo antes e depois do uso. Limpe a memória associada ao segredo quando terminar.

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

 

 

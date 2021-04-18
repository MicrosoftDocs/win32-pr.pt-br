---
description: Fornece propriedades e métodos para criptografar e descriptografar dados usando uma chave de sessão derivada de um segredo.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: Objeto EncryptedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 123e0973343e4990dd2d49cfb321d739085358f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764623"
---
# <a name="encrypteddata-object"></a>Objeto EncryptedData

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (serviços de invocação de plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens. Para obter informações sobre PInvoke, consulte [tutorial de invocação de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). O [.net e o CryptoAPI via p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.net e CryptoAPI via p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções de [estender a criptografia .NET com capicor e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O objeto **EncryptedData** fornece propriedades e métodos para criptografar e descriptografar dados usando uma [*chave de sessão*](../secgloss/s-gly.md) derivada de um segredo.

> [!Note]  
> O CAPICOM não oferece suporte ao \# tipo de conteúdo ENCRYPTEDDATA PKCS 7, mas usa uma estrutura ASN não padrão para **EncryptedData**. Portanto, somente o capicor pode descriptografar um objeto capicot **EncryptedData** .

 

## <a name="members"></a>Membros

O objeto **EncryptedData** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **EncryptedData** tem esses métodos.



| Método                                       | Descrição                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Descriptografar**](encrypteddata-decrypt.md)     | Descriptografa o conteúdo criptografado usando o segredo.<br/>                                 |
| [**Encrypt**](encrypteddata-encrypt.md)     | Criptografa o conteúdo usando o segredo atual e o algoritmo de criptografia.<br/>      |
| [**Setsecret**](encrypteddata-setsecret.md) | Define o segredo do qual a chave de sessão de criptografia/descriptografia é derivada.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **EncryptedData** tem essas propriedades.



| Propriedade                                                | Tipo de acesso           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](encrypteddata-algorithm.md)<br/> | Somente leitura<br/>  | Algoritmo usado para criptografia/descriptografia.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Disputa**](encrypteddata-content.md)<br/>     | Leitura/gravação<br/> | O conteúdo a ser criptografado ou descriptografado. A definição dessa propriedade deve ser feita antes que o método [**Encrypt**](encrypteddata-encrypt.md) seja chamado. <br/> Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido e qualquer conteúdo criptografado no objeto é perdido.<br/> Essa é a propriedade padrão.<br/> |



 

## <a name="remarks"></a>Comentários

O objeto **EncryptedData** pode ser criado e é seguro para scripts. O ProgID do objeto **EncryptedData** é CAPICOM. EncryptedData. 1.

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
</dt> </dl>

 

 

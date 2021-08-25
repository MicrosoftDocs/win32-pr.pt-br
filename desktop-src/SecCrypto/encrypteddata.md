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
ms.openlocfilehash: 15a66640ccdf794e88ae9cff04854a40fcfa6b763259da191bcdc6b07f11f449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874486"
---
# <a name="encrypteddata-object"></a>Objeto EncryptedData

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (Serviços de Invocação de Plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens. Para obter informações sobre o PInvoke, consulte [Tutorial de invocação de plataforma.](https://msdn.microsoft.com/library/aa288468.aspx) O .NET e a CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 e .NET e CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções da parte 2 de Estender a criptografia do .NET com [CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O **objeto EncryptedData** fornece propriedades e métodos para criptografar e descriptografar dados usando uma chave [*de*](../secgloss/s-gly.md) sessão derivada de um segredo.

> [!Note]  
> CAPICOM não dá suporte ao tipo de conteúdo PKCS 7 EncryptedData, mas usa uma estrutura ASN não padrão \# **para EncryptedData.** Portanto, somente CAPICOM pode descriptografar um objeto CAPICOM **EncryptedData.**

 

## <a name="members"></a>Membros

O **objeto EncryptedData** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto EncryptedData** tem esses métodos.



| Método                                       | Descrição                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Descriptografar**](encrypteddata-decrypt.md)     | Descriptografa o conteúdo criptografado usando o segredo.<br/>                                 |
| [**Encrypt**](encrypteddata-encrypt.md)     | Criptografa o conteúdo usando o segredo atual e o algoritmo de criptografia.<br/>      |
| [**SetSecret**](encrypteddata-setsecret.md) | Define o segredo do qual a chave de sessão de criptografia/descriptografia é derivada.<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto EncryptedData** tem essas propriedades.



| Propriedade                                                | Tipo de acesso           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](encrypteddata-algorithm.md)<br/> | Somente leitura<br/>  | Algoritmo usado para criptografia/descriptografia.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Conteúdo**](encrypteddata-content.md)<br/>     | Leitura/gravação<br/> | O conteúdo a ser criptografado ou descriptografado. A definição dessa propriedade deve ser feita antes que [**o método Encrypt**](encrypteddata-encrypt.md) seja chamado. <br/> Quando o valor dessa propriedade é redefinido, [](../secgloss/s-gly.md) direta ou indiretamente, todo o estado do objeto é redefinido e qualquer conteúdo criptografado no objeto é perdido.<br/> Essa é a propriedade padrão.<br/> |



 

## <a name="remarks"></a>Comentários

O **objeto EncryptedData** pode ser criado e é seguro para scripts. O ProgID para o **objeto EncryptedData** é CAPICOM. EncryptedData.1.

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
</dt> </dl>

 

 

---
description: Define ou recupera o comprimento da chave.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Propriedade Algorithm. KeyLength
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aa5dbaeeebe2daaf925b5d5f3aa82b36053fc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761398"
---
# <a name="algorithmkeylength-property"></a>Propriedade Algorithm. KeyLength

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

A propriedade **KeyLength** define ou recupera o comprimento da chave.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a>Valor da propriedade

Um valor da enumeração [**de \_ \_ \_ comprimento da chave de criptografia capicor**](capicom-encryption-key-length.md) que especifica o comprimento da chave. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                                                        | Significado                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <dt>**\_ \_ \_ comprimento máximo da chave de criptografia CAPICOM \_**</dt> </dl>     | Use o comprimento máximo de chave disponível com o algoritmo de criptografia indicado.<br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <dt>**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 40 \_ bits**</dt> </dl>    | Use chaves de 40 bits.<br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <dt>**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 56 \_ bits**</dt> </dl>    | Use chaves de 56 bits, se disponíveis.<br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <dt>**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 128 \_ bits**</dt> </dl> | Use chaves de 128 bits, se disponíveis.<br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <dt>**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 192 \_ bits**</dt> </dl> | Use chaves de 192 bits. Esse comprimento de chave está disponível apenas para AES.<br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <dt>**CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 256 \_ bits**</dt> </dl> | Use chaves de 256 bits. Esse comprimento de chave está disponível apenas para AES.<br/>                  |



 

## <a name="remarks"></a>Comentários

Quando algoritmos de criptografia DES e 3DES são usados, os comprimentos de chave são padrão e a propriedade **KeyLength** é ignorada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Algoritmo**](algorithm.md)
</dt> </dl>

 

 

---
description: Define ou recupera o tipo de algoritmo de hash usado.
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: Propriedade HashedData.Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 16562f3b954c9968899b7af63729a105956c7f809d094bdfa6c508a160a6d51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006644"
---
# <a name="hasheddataalgorithm-property"></a>Propriedade HashedData.Algorithm

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use [**a Classe HashAlgorithm**](/previous-versions/windows/) no namespace [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

A **propriedade Algorithm** define ou recupera o tipo de algoritmo de hash usado.

## <a name="syntax"></a>Syntax


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a>Valor da propriedade

Um valor da [**enumeração DE \_ ALGORITMO DE HASH \_ CAPICOM**](capicom-hash-algorithm.md) que define um algoritmo de hash. O valor padrão é \_ SHA1 DO ALGORITMO DE HASH CAPICOM. \_ \_ A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                               | Significado                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <dt>**ALGORITMO DE HASH CAPICOM \_ \_ \_ SHA1**</dt> </dl>           | Algoritmo de hash SHA1.<br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <dt>**ALGORITMO DE HASH CAPICOM \_ \_ \_ MD2**</dt> </dl>              | Algoritmo de hash MD2.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <dt>**ALGORITMO DE HASH CAPICOM \_ \_ \_ MD4**</dt> </dl>              | Algoritmo de hash MD4.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <dt>**ALGORITMO DE HASH CAPICOM \_ \_ \_ MD5**</dt> </dl>              | Algoritmo de hash MD5.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <dt>**ALGORITMO DE HASH CAPICOM \_ \_ SHA \_ \_ 256**</dt> </dl> | Algoritmo de hash SHA-256.<br/> **CAPICOM 2.0.0.3 e versões anteriores:** Não há suporte para esse valor.<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <dt>**ALGORITMO DE HASH CAPICOM \_ \_ SHA \_ \_ 384**</dt> </dl> | Algoritmo de hash SHA-384.<br/> **CAPICOM 2.0.0.3 e versões anteriores:** Não há suporte para esse valor.<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <dt>**ALGORITMO DE HASH CAPICOM \_ \_ SHA \_ \_ 512**</dt> </dl> | Algoritmo de hash SHA-512.<br/> **CAPICOM 2.0.0.3 e versões anteriores:** Não há suporte para esse valor.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 

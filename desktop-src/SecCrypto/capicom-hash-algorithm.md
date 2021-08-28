---
description: A enumeração do algoritmo capicor \_ hash \_ define um algoritmo de hash.
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: Enumeração de CAPICOM_HASH_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_HASH_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: df312c7e1ed578150069ff335527a20a2185c721b67a9e0e02cc1d57938b1cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879136"
---
# <a name="capicom_hash_algorithm-enumeration"></a>Enumeração de algoritmo capicor \_ hash \_

A enumeração do **\_ \_ algoritmo capicor hash** define um algoritmo de hash.

## <a name="members"></a>Membros



| Membro                                 | DESCRIÇÃO                                                                                                                                                                 | Valor |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **Algoritmo de hash de capico \_ \_ \_ SHA1**     | Sha ( [*algoritmo de hash seguro*](../secgloss/s-gly.md) ) que gera um resumo de mensagens de 160 bits.<br/> | 0     |
| **Algoritmo de hash de CAPICOM \_ \_ \_ MD2**      | Algoritmo de hash MD2.<br/>                                                                                                                                           | 1     |
| **Algoritmo de hash de CAPICOM \_ \_ \_ MD4**      | Algoritmo de hash MD4.<br/>                                                                                                                                           | 2     |
| **Algoritmo de hash de capico \_ \_ \_ MD5**      | Algoritmo de hash MD5.<br/>                                                                                                                                           | 3     |
| **CAPICOM do \_ algoritmo de hash \_ \_ Sha \_ 256** | Algoritmo de hash SHA-256.<br/> **CAPICOM 2.0.0.3 e anteriores:** Não há suporte para esse valor.<br/>                                                                 | 4     |
| **CAPICOM do \_ algoritmo de hash \_ \_ Sha \_ 384** | Algoritmo de hash SHA-384.<br/> **CAPICOM 2.0.0.3 e anteriores:** Não há suporte para esse valor.<br/>                                                                 | 5     |
| **CAPICOM do \_ algoritmo de hash \_ \_ Sha \_ 512** | Algoritmo de hash SHA-512.<br/> **CAPICOM 2.0.0.3 e anteriores:** Não há suporte para esse valor.<br/>                                                                 | 6     |



## <a name="remarks"></a>Comentários

A enumeração do **\_ \_ algoritmo de hash capicor** é usada pela propriedade [**HashedData. Algorithm**](hasheddata-algorithm.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 

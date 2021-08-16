---
description: Define o comprimento da chave a ser usada na criptografia.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: Enumeração de CAPICOM_ENCRYPTION_KEY_LENGTH (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 2957bd644fdf405fec7e82a487bf83af2cbae35ae305f10b9b168628a30b0749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772471"
---
# <a name="capicom_encryption_key_length-enumeration"></a>\_Enumeração de \_ comprimento de chave de criptografia CAPICOM \_

O tipo de enumeração de **comprimento da chave de \_ criptografia \_ \_ capicor** define o [*comprimento da chave*](../secgloss/k-gly.md) a ser usada na criptografia.

## <a name="members"></a>Membros



| Membro                                          | DESCRIÇÃO                                                                               | Valor     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| **\_ \_ \_ comprimento máximo da chave de criptografia CAPICOM \_**   | Usa o comprimento máximo de chave disponível com o algoritmo de criptografia indicado.<br/> | 0         |
| **CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 40 \_ bits**  | Usa chaves de 40 bits.<br/>                                                              | 1         |
| **CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 56 \_ bits**  | Usa chaves de 56 bits, se disponíveis.<br/>                                                 | 2         |
| **CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 128 \_ bits** | Usa chaves de 128 bits, se disponíveis.<br/>                                                | 3         |
| **CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 192 \_ bits** | Usa chaves de 192 bits. Esse comprimento de chave está disponível apenas para AES.<br/>                  | 4//v 2.0 |
| **CAPICOM o \_ comprimento da chave de criptografia \_ \_ \_ 256 \_ bits** | Usa chaves de 256 bits. Esse comprimento de chave está disponível apenas para AES.<br/>                  | 5//v 2.0 |



## <a name="remarks"></a>Comentários

O tipo de enumeração de **\_ comprimento da \_ chave \_ de criptografia capicor** é usado pelo [**algoritmo. Propriedade KeyLength**](algorithm-keylength.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 

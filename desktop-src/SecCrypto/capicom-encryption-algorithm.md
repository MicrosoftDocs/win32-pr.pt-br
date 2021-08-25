---
description: Define os algoritmos a serem usados na criptografia e na descriptografia.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: Enumeração de CAPICOM_ENCRYPTION_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d0f66c1e8ec59819f4f01c5f46989e1f904930f3699f978b26c6ab7c5107154c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879336"
---
# <a name="capicom_encryption_algorithm-enumeration"></a>Enumeração do algoritmo de \_ criptografia CApicom \_

O tipo de enumeração do **\_ \_ algoritmo de criptografia capicor** define os algoritmos a serem usados na criptografia e na descriptografia.

## <a name="members"></a>Membros



| Membro                                   | DESCRIÇÃO                                                                                                                                                                                              | Valor     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **Algoritmo de criptografia CAPICOM \_ \_ \_ RC2**  | Use a criptografia RSA RC2.<br/>                                                                                                                                                                       | 0         |
| **Algoritmo de criptografia capicor \_ \_ \_ RC4**  | Use a criptografia RSA RC4.<br/>                                                                                                                                                                       | 1         |
| **algoritmo de criptografia CAPICOM \_ \_ \_ des**  | Use a criptografia DES.<br/>                                                                                                                                                                           | 2         |
| **Algoritmo de criptografia CAPICOM \_ \_ \_ 3DES** | Use a criptografia triple DES.<br/>                                                                                                                                                                    | 3         |
| **algoritmo de criptografia capicor \_ \_ \_ AES**  | Use o algoritmo [*criptografia AES*](../secgloss/a-gly.md) (AES). Esse valor é válido somente para o objeto [**EncryptedData**](encrypteddata.md) .<br/> | 4//v 2.0 |



## <a name="remarks"></a>Comentários

O tipo de enumeração de **\_ \_ algoritmo de criptografia capicor** é usado pela propriedade [**Algorithm.Name**](algorithm-name.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 

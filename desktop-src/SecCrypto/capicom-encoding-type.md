---
description: Indica o tipo de codificação usado.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: CAPICOM_ENCODING_TYPE enumeração (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1ec9a9ea1de4e3f501c94394ec9038d39c9b881c1e2bb1f41322d4f08c2db922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772481"
---
# <a name="capicom_encoding_type-enumeration"></a>Enumeração CAPICOM \_ ENCODING \_ TYPE

O **tipo de enumeração CAPICOM \_ ENCODING \_ TYPE** indica o tipo de codificação usado.

## <a name="members"></a>Membros



| Membro                      | DESCRIÇÃO                                                                                                                                                                                 | Valor      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CODIFICAR QUALQUER \_ CAPICOM \_**    | Os dados são salvos como uma cadeia de caracteres codificada em base64 ou uma sequência binária pura. Esse tipo de codificação é usado somente para dados de entrada que têm um tipo de codificação desconhecido. Introduzido no CAPICOM 2.0.<br/> | 0xffffffff |
| **CODIFICAÇÃO CAPICOM \_ \_ BASE64** | Os dados são salvos como uma cadeia de caracteres codificada em base64.<br/>                                                                                                                                        | 0          |
| **BINÁRIO DE CODIFICAÇÃO CAPICOM \_ \_** | Os dados são salvos como uma sequência binária pura.<br/>                                                                                                                                         | 1          |



## <a name="remarks"></a>Comentários

Esse tipo de enumeração é usado pelos seguintes métodos e propriedades CAPICOM:

-   [**Método Certificate.Export**](certificate-export.md)
-   [**Propriedade EncodedData.Value**](encodeddata-value.md)
-   [**Método EncryptedData.Encrypt**](encrypteddata-encrypt.md)
-   [**Método EnvelopedData.Encrypt**](envelopeddata-encrypt.md)
-   [**Propriedade ExtendedProperty.Value**](extendedproperty-value.md)
-   [**Método SignedData.Sign**](signeddata-sign.md)
-   [**Método SignedData.CoSign**](signeddata-cosign.md)
-   [**Método Store.Export**](store-export.md)
-   [**Método Utilities.GetRandom**](utilities-getrandom.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 





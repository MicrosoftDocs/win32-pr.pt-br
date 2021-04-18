---
description: Indica o tipo de codificação usado.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: Enumeração de CAPICOM_ENCODING_TYPE (CAPICOM. h)
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
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756379"
---
# <a name="capicom_encoding_type-enumeration"></a>Enumeração do tipo de \_ codificação CApicom \_

O tipo de enumeração de **\_ \_ tipo de codificação capicor** indica o tipo de codificação usado.

## <a name="members"></a>Membros



| Membro                      | DESCRIÇÃO                                                                                                                                                                                 | Valor      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ codificar \_ qualquer**    | Os dados são salvos como uma cadeia de caracteres codificada em base64 ou uma sequência binária pura. Esse tipo de codificação é usado somente para dados de entrada que têm um tipo de codificação desconhecido. Introduzido no CAPICOM 2,0.<br/> | 0xFFFFFFFF |
| **CAPICOM \_ codificar \_ Base64** | Os dados são salvos como uma cadeia de caracteres codificada em base64.<br/>                                                                                                                                        | 0          |
| **capicote de \_ codificação \_ binário** | Os dados são salvos como uma sequência binária pura.<br/>                                                                                                                                         | 1          |



## <a name="remarks"></a>Comentários

Esse tipo de enumeração é usado pelos seguintes métodos e propriedades CAPICOM:

-   Método [**Certificate. Export**](certificate-export.md)
-   Propriedade [**EncodedData. Value**](encodeddata-value.md)
-   Método [**EncryptedData. Encrypt**](encrypteddata-encrypt.md)
-   Método [**EnvelopedData. Encrypt**](envelopeddata-encrypt.md)
-   Propriedade [**Extended. Value**](extendedproperty-value.md)
-   Método [**SignedData. Sign**](signeddata-sign.md)
-   Método [**SignedData. cosign**](signeddata-cosign.md)
-   Método [**Store. Export**](store-export.md)
-   Método [**Utilities. Getaleatório**](utilities-getrandom.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                |
| parâmetro<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 





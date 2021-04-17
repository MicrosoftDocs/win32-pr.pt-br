---
description: Decodifica uma cadeia de caracteres de Base64.
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Método Utilities. Base64Decode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Decode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df0a0e2a0400ef2000ce5e54e1a76a1a4bd8eebd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757996"
---
# <a name="utilitiesbase64decode-method"></a>Método Utilities. Base64Decode

\[O método **Base64Decode** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]

O método **Base64Decode** decodifica uma cadeia de caracteres de Base64.

## <a name="syntax"></a>Sintaxe


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EncodedString* \[ no\]
</dt> <dd>

A cadeia de caracteres codificada em base64 a ser decodificada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A cadeia de caracteres decodificada.

## <a name="remarks"></a>Comentários

A codificação Base64 é o esquema usado para transmitir dados binários. A base64 processa dados como grupos de 24 bits, mapeando esses dados para quatro caracteres codificados. A codificação Base64 é, às vezes, chamada de codificação 3 para 4. Cada 6 bits do grupo de 24 bits é usado como um índice em uma tabela de mapeamento (o alfabeto Base64) para obter um caractere para os dados codificados. Os dados codificados têm comprimentos de linha limitados a 76 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Utilitários**](utilities.md)
</dt> </dl>

 

 





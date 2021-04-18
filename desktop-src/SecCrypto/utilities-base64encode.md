---
description: Codifica uma cadeia de caracteres como Base64.
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Método Utilities. Base64Encode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800072"
---
# <a name="utilitiesbase64encode-method"></a>Método Utilities. Base64Encode

\[O método **Base64Encode** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]

O método **Base64Encode** codifica uma cadeia de caracteres como Base64.

## <a name="syntax"></a>Sintaxe


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SrcString* \[ no\]
</dt> <dd>

A cadeia de caracteres para codificar como Base64.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A cadeia de caracteres codificada em base64.

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

 

 





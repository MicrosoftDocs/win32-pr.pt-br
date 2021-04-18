---
description: Um alias para UInt16 \_ t empacotado com um número de ponto flutuante de 16 bits que consiste em um bit de sinal, um expoente com tendência de 5 bits e um mantissa de 10 bits.
ms.assetid: E84E0EBA-5C34-41AA-84DB-7A65EBDCAD15
title: Tipo de metade de dados (DirectXPackedVector. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651b84675be68bd433fdeaaae588cb01dc745ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814402"
---
# <a name="half-data-type"></a>MEIO tipo de dados

Um alias para **UInt16 \_ t** empacotado com um número de ponto flutuante de 16 bits que consiste em um bit de sinal, um expoente com tendência de 5 bits e um mantissa de 10 bits.


```C++
typedef uint16_t HALF;
```



## <a name="remarks"></a>Comentários

O tipo de metade de dados é equivalente ao formato IEEE 754 binary16.

HALF \_ min = 6.10352 e-5F

HALF \_ Max = 65504. f

Para obter mais informações sobre o tipo de dados HALF, consulte [formato de ponto flutuante de meia precisão](https://en.wikipedia.org/wiki/Half_precision_floating-point_format).

**Namespace**: Use DirectX::P ackedvector

### <a name="platform-requirements"></a>Requisitos de plataforma

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8. Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DirectXPackedVector. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de biblioteca DirectXMath](ovw-xnamath-reference-types.md)
</dt> </dl>

 

 





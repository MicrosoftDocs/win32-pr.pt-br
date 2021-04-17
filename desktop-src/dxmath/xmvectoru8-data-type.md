---
description: Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar \_ valores t uint8 em uma instância do tipo XMVECTOR.
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: Tipo de dados XMVECTORU8 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4428cdd78206bfa17c295a9578653bb0a66f0c6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782448"
---
# <a name="xmvectoru8-data-type"></a>Tipo de dados XMVECTORU8

Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar \_ valores t uint8 em uma instância do tipo [**XMVECTOR**](xmvector-data-type.md) .


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a>Comentários

Para obter uma lista de funcionalidades adicionais, como construtores e operadores, disponíveis usando XMVECTORU8 ao programar em C++, consulte [extensões de XMVECTORU8](ovw-xmvectoru8-extensions.md).

As estruturas [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)e **XMVECTORU8** são fornecidas como um mecanismo para criar [**XMVECTOR**](xmvector-data-type.md) de tipos de dados constantes diferentes (ponto flutuante, inteiro sem sinal, inteiro e byte) usando inicializadores.

Isso é necessário para dar suporte a [**XMVECTOR**](xmvector-data-type.md), pois ele não oferece suporte a inicializadores, por motivos de portabilidade e otimização.

Por exemplo:

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

**Namespace**: usar DirectX

### <a name="platform-requirements"></a>Requisitos de plataforma

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8. Com suporte para aplicativos de área de trabalho Win32, aplicativos da Windows Store e aplicativos Windows Phone 8.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DirectXMath. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de biblioteca DirectXMath](ovw-xnamath-reference-types.md)
</dt> <dt>

[**Tipo de dados XMVECTOR**](xmvector-data-type.md)
</dt> <dt>

[**Tipo de dados XMVECTORF32**](xmvectorf32-data-type.md)
</dt> <dt>

[**Tipo de dados XMVECTORI32**](xmvectori32-data-type.md)
</dt> <dt>

[**Tipo de dados XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[Extensões XMVECTORU8](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 





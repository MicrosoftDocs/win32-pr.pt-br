---
description: Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar valores inteiros em uma instância do tipo XMVECTOR.
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: Tipo de dados XMVECTORI32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b4bb03dffb4c77575aab8c2a2680ecd821fea627f49325c6748ede607ef81f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739748"
---
# <a name="xmvectori32-data-type"></a>Tipo de dados XMVECTORI32

Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar valores inteiros em uma instância do tipo [**XMVECTOR**](xmvector-data-type.md) .


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a>Comentários

Para obter uma lista de funcionalidades adicionais, como construtores e operadores, disponíveis usando `XMVECTORI32` ao programar em C++, consulte [extensões de XMVECTORI32](ovw-xmvectori32-extensions.md).

As estruturas [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32** e [**XMVECTORU8**](xmvectoru8-data-type.md) são fornecidas como um mecanismo para criar [**XMVECTOR**](xmvector-data-type.md) de tipos de dados constantes diferentes (ponto flutuante, inteiro sem sinal, inteiro e byte) usando inicializadores.

Isso é necessário para dar suporte a [**XMVECTOR**](xmvector-data-type.md), pois ele não oferece suporte a inicializadores, por motivos de portabilidade e otimização.

Por exemplo:


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
```



**Namespace**: usar DirectX

### <a name="platform-requirements"></a>Requisitos de plataforma

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8. com suporte para aplicativos de área de trabalho do Win32, aplicativos da Windows store e aplicativos Windows Phone 8.

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

[**Tipo de dados XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Tipo de dados XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Tipo de dados XMVECTORI32**](xmvectori32-data-type.md)
</dt> </dl>

 

 





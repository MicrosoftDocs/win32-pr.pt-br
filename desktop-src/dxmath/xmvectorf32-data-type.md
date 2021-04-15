---
description: Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar valores de ponto flutuante em uma instância do tipo XMVECTOR.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: Tipo de dados XMVECTORF32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e56e79ea678ede0afcac3523c09da725ede00d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747457"
---
# <a name="xmvectorf32-data-type"></a>Tipo de dados XMVECTORF32

Um tipo opaco e portátil para dar suporte ao uso da sintaxe do inicializador C/C++ para carregar valores de ponto flutuante em uma instância do tipo [**XMVECTOR**](xmvector-data-type.md) .


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a>Comentários

Para obter uma lista de funcionalidades adicionais, como construtores e operadores, disponíveis usando `XMVECTORF32` ao programar em C++, consulte [extensões de XMVECTORF32](ovw-xmvectorf32-extensions.md).

As estruturas **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)e [**XMVECTORU8**](xmvectoru8-data-type.md) são fornecidas como um mecanismo para criar [**XMVECTOR**](xmvector-data-type.md) de tipos de dados constantes diferentes (ponto flutuante, inteiro sem sinal, inteiro e byte) usando inicializadores.

Isso é necessário para dar suporte a [**XMVECTOR**](xmvector-data-type.md), pois ele não oferece suporte a inicializadores, por motivos de portabilidade e otimização.

Por exemplo:


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
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

[**Tipo de dados XMVECTORI32**](xmvectori32-data-type.md)
</dt> <dt>

[**Tipo de dados XMVECTOR**](xmvector-data-type.md)
</dt> <dt>

[**Tipo de dados XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Tipo de dados XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Tipo de dados XMVECTORF32**](xmvectorf32-data-type.md)
</dt> </dl>

 

 





---
description: Um tipo portátil usado para representar um vetor de ponto flutuante de 4 32 bits ou componentes inteiros, cada um alinhado de forma ideal e mapeado para um registro de vetor de hardware.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Tipo de dados XMVECTOR (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c62cab01098cd95f904ac2e2ee33d420309e8e99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765673"
---
# <a name="xmvector-data-type"></a>Tipo de dados XMVECTOR

Um tipo portátil usado para representar um vetor de ponto flutuante de 4 32 bits ou componentes inteiros, cada um alinhado de forma ideal e mapeado para um registro de vetor de hardware.

## <a name="remarks"></a>Comentários

Para obter uma lista de funcionalidades adicionais, como construtores e operadores, disponíveis usando `XMVECTOR` ao programar em C++, consulte [extensões de XMVECTOR](ovw-xmvector-extensions.md).

Na biblioteca DirectXMath, para dar suporte total à portabilidade e otimização, `XMVECTOR` é, por design, um tipo opaco. A implementação real do `XMVECTOR` é dependente da plataforma.

Em geral, o código não deve contar com as especificidades de uma determinada implementação específica da plataforma do `XMVECTOR` . Implementações específicas da plataforma têm estas características:

-   Eles não são portáteis.
-   Eles podem ser alterados entre as versões.
-   O uso incriterioso de detalhes de implementação pode ser inferior.

Os desenvolvedores devem usar as funções [acessador](ovw-xnamath-reference-functions-accessors.md), [carga](ovw-xnamath-reference-functions-load.md)e [armazenamento](ovw-xnamath-reference-functions-storage.md) da biblioteca DirectXMath para obter e definir os vetores e as [funções de vetor 4D da biblioteca DirectXMath](ovw-xnamath-reference-functions-vector4.md) para manipulá-los.

Para projetos que precisam de informações detalhadas sobre como implementar `XMVECTOR` em diferentes plataformas, consulte [elementos internos da biblioteca](pg-xnamath-internals.md).

### <a name="compiler-aliases"></a>Aliases do compilador

O arquivo de cabeçalho DirectXMath. h usa aliases para o `XMVECTOR` objeto, especificamente **CXMVECTOR** e **FXMVECTOR**. O cabeçalho usa esses aliases para obedecer às convenções de chamada internas ideais de compiladores diferentes. Para a maioria dos projetos que usam DirectXMath, é suficiente tratar esses tipos como um alias exato para `XMVECTOR` .

Por exemplo:


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



Para projetos que precisam de informações detalhadas sobre como diferentes plataformas manipulam suas convenções de chamada, consulte [elementos internos da biblioteca](pg-xnamath-internals.md).

Para XNAMATH 2. x, o `XMVECTOR` tipo de dados tem os membros do elemento. x,. y,. z,. e. w, o que geralmente causa baixo desempenho. O uso do tipo XM \_ estrito \_ VECTOR4 fornece uma aceitação da definição de DirectXMath de um tipo de dados opaco.

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

[**Tipo de dados XMVECTORF32**](xmvectorf32-data-type.md)
</dt> <dt>

[**Tipo de dados XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Tipo de dados XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Tipo de dados XMVECTOR**](xmvector-data-type.md)
</dt> </dl>

 

 





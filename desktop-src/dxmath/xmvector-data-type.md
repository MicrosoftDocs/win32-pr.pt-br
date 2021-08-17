---
description: Um tipo portátil usado para representar um vetor de quatro componentes inteiros ou de ponto flutuante de 32 bits, cada um alinhado de forma ideal e mapeado para um registro de vetor de hardware.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Tipo de dados XMVECTOR (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0a65c7da346163c3cbfaab7c68982f56eb6c424b7f74a3ec01c754eb4104a5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094476"
---
# <a name="xmvector-data-type"></a>Tipo de dados XMVECTOR

Um tipo portátil usado para representar um vetor de quatro componentes inteiros ou de ponto flutuante de 32 bits, cada um alinhado de forma ideal e mapeado para um registro de vetor de hardware.

## <a name="remarks"></a>Comentários

Para obter uma lista de funcionalidades adicionais, como construtores e operadores, disponíveis ao programar em `XMVECTOR` C++, consulte [Extensões XMVECTOR](ovw-xmvector-extensions.md).

Na Biblioteca DirectXMath, para dar suporte completo à portabilidade e à otimização, `XMVECTOR` é, por design, um tipo opaco. A implementação real de `XMVECTOR` depende da plataforma.

Em geral, o código não deve depender das especificações de qualquer implementação específica da plataforma específica de `XMVECTOR` . Implementações específicas da plataforma têm estas características:

-   Eles não são portáteis.
-   Eles podem mudar entre as versões.
-   O uso indevido de detalhes de implementação pode ser abaixo do ideal.

Os desenvolvedores devem usar o acessador [](ovw-xnamath-reference-functions-load.md)da [](ovw-xnamath-reference-functions-storage.md) Biblioteca DirectXMath, [](ovw-xnamath-reference-functions-accessors.md)carregar e armazenar funções para obter e definir os vetores e as Funções de Vetor 4D da Biblioteca [DirectXMath](ovw-xnamath-reference-functions-vector4.md) para manipulá-los.

Para projetos que precisam de informações detalhadas sobre como implementar em `XMVECTOR` diferentes plataformas, consulte [Biblioteca Internas](pg-xnamath-internals.md).

### <a name="compiler-aliases"></a>Aliases do compilador

O arquivo de header DirectXMath.h usa aliases para o objeto , especificamente `XMVECTOR` **CXMVECTOR** e **FXMVECTOR**. O header usa esses aliases para atender às convenções de chamada em linha ideais de compiladores diferentes. Para a maioria dos projetos que usam o DirectXMath, é suficiente tratar esses tipos como um alias exato para `XMVECTOR` .

Por exemplo:


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



Para projetos que precisam de informações detalhadas sobre como diferentes plataformas lidam com suas convenções de chamada, consulte [Biblioteca Internas](pg-xnamath-internals.md).

Para XNAMATH 2.x, o tipo de dados tem membros de elemento `XMVECTOR` .x, .y, .z, .e .w, o que geralmente causa baixo desempenho. O uso do tipo VECTOR4 STRICT XM fornece uma aceitação da definição \_ \_ directXMath de um tipo de dados opaco.

**Namespace**: usar o DirectX

### <a name="platform-requirements"></a>Requisitos de plataforma

Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 com o SDK do Windows para Windows 8. Com suporte para aplicativos da área de trabalho win32, aplicativos Windows Store e Windows Phone 8 aplicativos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



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

 

 





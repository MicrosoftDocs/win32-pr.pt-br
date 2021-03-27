---
title: Tipo de buffer
description: Use a sintaxe a seguir para declarar uma variável de buffer.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Tipo de buffer HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e36030f3dd31f1bdada238e89c1048e4971cd45c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007748"
---
# <a name="buffer-type"></a>Tipo de buffer

Use a sintaxe a seguir para declarar uma variável de buffer.



| Nome do *tipo* de<de buffer >  ; |
|------------------------------|



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Completo**
</dt> <dd>

Palavra-chave required.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Escreva*
</dt> <dd>

Um dos tipos de HLSL [escalar](dx-graphics-hlsl-scalar.md), de [vetor](dx-graphics-hlsl-vector.md)e de [matriz](dx-graphics-hlsl-matrix.md) . Você pode declarar uma variável de buffer com uma matriz, desde que ela caiba em quantidades de 4 32 bits. Portanto, você pode escrever `Buffer<float2x2>` . Mas `Buffer<float4x4>` é muito grande, e o compilador irá gerar um erro.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*
</dt> <dd>

Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.

</dd> </dl>

## <a name="example"></a>Exemplo

Aqui está um exemplo de uma declaração de buffer do arquivo PipesGS. FX no [exemplo PipesGS](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).


```
Buffer<float4> g_Buffer;
```



Os dados são lidos de um buffer usando uma versão sobrecarregada da função intrínseca [**Load**](dx-graphics-hlsl-to-load.md) HLSL que usa um parâmetro de entrada (um índice de número inteiro). Um buffer é acessado como uma matriz de elementos; Portanto, este exemplo lê o segundo elemento.


```
float4 bufferData = g_Buffer.Load( 1 );
```



Use o [estágio Stream-output](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) para gerar dados de saída para um buffer.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 
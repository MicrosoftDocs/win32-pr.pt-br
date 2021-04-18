---
description: Invoca outro sombreador de dentro de um sombreador.
ms.assetid: ''
title: Função CallShader
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: 8c5cdf4e0a71430d6375fd75ca553f92ca9539b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812091"
---
# <a name="callshader-function"></a>Função CallShader

Invoca outro sombreador de dentro de um sombreador.

## <a name="syntax"></a>Sintaxe
Essa definição de função intrínseca é equivalente ao seguinte modelo de função:

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a>Parâmetros

`ShaderIndex`

Um inteiro sem sinal representando o índice na tabela de [sombreador callable](callable-shader.md) especificada na chamada para [**DispatchRays**] (/Windows/Desktop/API/d3d12/NF-d3d12-id3d12graphicscommandlist4-dispatchrays.

`Parameter`

Os parâmetros definidos pelo usuário a serem passados para o sombreador que possa ser chamado.  Essa estrutura de parâmetro deve corresponder à estrutura de parâmetro usada no sombreador callable apontado na tabela de sombreador.


## <a name="return-value"></a>Valor Retornado

**void**

## <a name="remarks"></a>Comentários

Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador resgatável**](callable-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de resolução**](miss-shader.md)
* [**Sombreador da geração de raio**](ray-generation-shader.md)



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





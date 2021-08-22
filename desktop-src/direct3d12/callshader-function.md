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
ms.openlocfilehash: e411ef61c34eafcef71f3e68f6700651e4b3073423afd40451f139f02826e504
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119280346"
---
# <a name="callshader-function"></a>Função CallShader

Invoca outro sombreador de dentro de um sombreador.

## <a name="syntax"></a>Syntax
Essa definição de função intrínseca é equivalente ao seguinte modelo de função:

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a>Parâmetros

`ShaderIndex`

Um inteiro sem sinal que [](callable-shader.md) representa o índice na tabela de sombreador que pode ser chamada especificada na chamada para [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays.

`Parameter`

Os parâmetros definidos pelo usuário a passar para o sombreador que pode ser chamado.  Essa estrutura de parâmetros deve corresponder à estrutura de parâmetro usada no sombreador que pode ser chamado apontado na tabela do sombreador.


## <a name="return-value"></a>Valor Retornado

**Vazio**

## <a name="remarks"></a>Comentários

Essa função pode ser chamada dos seguintes tipos de sombreador de raio:

* [**Sombreador resgatável**](callable-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de resolução**](miss-shader.md)
* [**Sombreador da geração de raio**](ray-generation-shader.md)



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





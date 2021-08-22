---
description: Um sombreador que é invocado de outro sombreador com o intrínseco CallShader.
ms.assetid: ''
title: Sombreador resgatável
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: b84ec6ea58fbc456db1747259f687a2fb6c8cb0fe3374b3d32396861dcd2f9b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461066"
---
# <a name="callable-shader"></a>Sombreador resgatável

Um sombreador que é invocado de outro sombreador com o intrínseco [**CallShader**](callshader-function.md) .

Há uma estrutura de parâmetro fornecida no site de chamada **CallShader** que deve corresponder à estrutura de parâmetro usada no sombreador callable apontado pelo índice solicitado para a tabela de sombreador callable fornecida por meio do método [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) .  O sombreador callable deve declarar esse parâmetro como *Inout*.  Além disso, o sombreador callable pode ler as entradas de índice e de dimensão de inicialização. Para obter mais informações, consulte [**intrínsecos de valor do sistema**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md). 


## <a name="shader-type-attribute"></a>Atributo de tipo de sombreador


```
[shader("callable")]
```



## <a name="example"></a>Exemplo

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 





---
description: Um sombreador que é invocado quando nenhuma interseção de Ray é encontrada ou aceita.
ms.assetid: ''
title: Sombreador de resolução
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: fe8e2ec9cdbb8ef7567b9327ae5af1128597a601
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764101"
---
# <a name="miss-shader"></a>Sombreador de resolução

Um sombreador que é invocado quando nenhuma interseção de Ray é encontrada ou aceita. Isso é útil para o sombreamento em segundo plano ou céu.  O sombreador de erros pode usar [**CallShader**](callshader-function.md) e **TraceRay** para agendar mais trabalho.

O sombreador ausente deve incluir um parâmetro de carga digitado de estrutura definida pelo usuário correspondente ao fornecido para [**TraceRay**](traceray-function.md).


## <a name="shader-type-attribute"></a>Atributo de tipo de sombreador


```
[shader("miss")]
```



## <a name="example"></a>Exemplo

```
[shader("anyhit")]
void miss_main(inout MyPayload payload)
{
    // Use ray system values to compute contributions of background, sky, etc...
    // Combine contributions into ray payload
    CallShader( ... );  // if desired
    TraceRay( ... );    // if desired
    // this ray query is now complete
}

```

 

 





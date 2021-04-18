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
# <a name="miss-shader"></a><span data-ttu-id="eb152-103">Sombreador de resolução</span><span class="sxs-lookup"><span data-stu-id="eb152-103">Miss Shader</span></span>

<span data-ttu-id="eb152-104">Um sombreador que é invocado quando nenhuma interseção de Ray é encontrada ou aceita.</span><span class="sxs-lookup"><span data-stu-id="eb152-104">A shader that is invoked when no ray intersections are found or accepted.</span></span> <span data-ttu-id="eb152-105">Isso é útil para o sombreamento em segundo plano ou céu.</span><span class="sxs-lookup"><span data-stu-id="eb152-105">This is useful for background or sky shading.</span></span>  <span data-ttu-id="eb152-106">O sombreador de erros pode usar [**CallShader**](callshader-function.md) e **TraceRay** para agendar mais trabalho.</span><span class="sxs-lookup"><span data-stu-id="eb152-106">The miss shader may use [**CallShader**](callshader-function.md) and **TraceRay** to schedule more work.</span></span>

<span data-ttu-id="eb152-107">O sombreador ausente deve incluir um parâmetro de carga digitado de estrutura definida pelo usuário correspondente ao fornecido para [**TraceRay**](traceray-function.md).</span><span class="sxs-lookup"><span data-stu-id="eb152-107">The miss shader must include a user-defined structure typed payload parameter matching the one supplied to [**TraceRay**](traceray-function.md).</span></span>


## <a name="shader-type-attribute"></a><span data-ttu-id="eb152-108">Atributo de tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="eb152-108">Shader Type attribute</span></span>


```
[shader("miss")]
```



## <a name="example"></a><span data-ttu-id="eb152-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="eb152-109">Example</span></span>

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

 

 





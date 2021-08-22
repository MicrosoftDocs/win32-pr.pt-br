---
description: Um sombreador que é invocado quando Ray interseções não são opacas.
ms.assetid: ''
title: Sombreador de todos os cliques
ms.date: 05/31/2018
ms.topic: reference
ms.localizationpriority: low
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 127c12c6d87ca76ddac5b5c5e013414c96651e56ee762156e7435811ff275a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124381"
---
# <a name="any-hit-shader"></a>Sombreador de todos os cliques

Um sombreador que é invocado quando Ray interseções não são opacas. 

Qualquer sombreador de acesso deve declarar um parâmetro de carga seguido por um parâmetro Attributes. Cada um desses parâmetros deve ser um tipo de estrutura definido pelo usuário tipos de correspondência usados para [**TraceRay**](traceray-function.md) e [**ReportHit**](reporthit-function.md) , respectivamente, ou a [**estrutura de atributos de interseção**](intersection-attributes.md) quando a interseção de triângulo de função fixa é usada.

Qualquer sombreador de acesso pode executar os seguintes tipos de operações:

*   Ler e modificar a carga do Ray: (Inout payload_t rayPayload)
*   Ler os atributos de interseção: (em atributos de attr_t)
*   Chame [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), que aceita a visita atual, termina o [sombreador de qualquer clique](any-hit-shader.md), termina o [sombreador de interseção](intersection-shader.md) se houver um presente e executa o [sombreador de pressionamentos mais próximo](closest-hit-shader.md) no próximo acesso até o momento, se estiver ativo.
*   Chame [**IgnoreHit**](ignorehit-function.md), que termina o sombreador de qualquer clique e informa ao sistema para continuar pesquisando ocorrências, incluindo o controle de retorno para um sombreador de interseção, se estiver em execução no momento, retornando false do site de chamada [**ReportHit**](reporthit-function.md)*. 
*   Return sem chamar nenhum desses intrínsecos, que aceita a ocorrência atual e informa ao sistema para continuar pesquisando ocorrências, incluindo o controle de retorno para o sombreador de interseção, se houver um, retornando true no site de chamada [**ReportHit**](reporthit-function.md) para indicar que o acerto foi aceito.

Mesmo que uma invocação de sombreador de clique seja encerrada por [**IgnoreHit**](ignorehit-function.md) ou [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), todas as modificações feitas na carga de Ray até o momento ainda devem ser retidas.

## <a name="shader-type-attribute"></a>Atributo de tipo de sombreador

```
[shader("anyhit")]
```

## <a name="example"></a>Exemplo

```
[shader("anyhit")]
void anyhit_main( inout MyPayload payload, in MyAttributes attr )
{
    float3 hitLocation = ObjectRayOrigin() + ObjectRayDirection() * RayTCurrent();
    float alpha = computeAlpha(hitLocation, attr, ...);

    // Processing shadow and only care if a hit is registered?
    if (TerminateShadowRay(alpha))
        AcceptHitAndEndSearch(); // aborts function

    // Save alpha contribution and ignoring hit?
    if (SaveAndIgnore(payload, RayTCurrent(), alpha, attr, ...))
        IgnoreHit(); // aborts function

    // do something else
    // return to accept and update closest hit
}
```

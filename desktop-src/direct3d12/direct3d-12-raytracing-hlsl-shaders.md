---
title: Sombreadores HLSL de raytracing do Direct3D 12
description: Veja links para artigos que descrevem sombreadores de HLSL (linguagem de sombreador de alto nível) que suportam o pipeline de raytracing do Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2321511be2ef912a6dce6710b233cb59dcc7712e9e8f63db890d8707822c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733769"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a>Sombreadores HLSL de raytracing do Direct3D 12

Os sombreadores HLSL a seguir são suportados pelo pipeline de raytracing do Direct3D 12. Esses sombreadores são funções compiladas em uma biblioteca, com o modelo de destino lib_6_3 e identificadas por um atributo *[shader("shadertype")]* na função de sombreador. Consulte **Intrínsecos** **e Valores do Sistema** para ver o que é permitido para cada tipo de sombreador.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                       | Descrição                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Sombreador de todos os cliques**](any-hit-shader.md)<br/>                              | Um sombreador que é invocado quando interseções de raio não são opacas.<br/>                                                                                                                                                                                                                                              |
| [**Sombreador resgatável**](callable-shader.md)<br/>                              | Um sombreador que é invocado de outro sombreador com o **intrínseco CallShader.**<br/>                                                                                                                                                                                                                                              |
| [**Sombreador do clique mais próximo**](closest-hit-shader.md)<br/>                              | Um sombreador que é invocado quando está habilitado e o acerto mais próximo foi determinado ou a pesquisa de interseção de raio terminou.<br/>                                                                                                                                                                                                                                              |
| [**Sombreador de interseção**](intersection-shader.md)<br/>                              | Um sombreador usado para implementar primitivos de interseção personalizados para raios intersecção de um volume delimitador associado (caixa delimitador).<br/>                                                                                                                                                                                                                                              |
| [**Sombreador de resolução**](miss-shader.md)<br/>                              | Um sombreador que é invocado quando nenhuma interseção de raio é encontrada ou aceita.<br/>                                                                                                                                                                                                                                              |
| [**Sombreador da geração de raio**](ray-generation-shader.md)<br/>                              | Um sombreador que chama [**TraceRay para**](traceray-function.md) gerar raios.<br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência principal](direct3d-12-core-reference.md)
</dt> <dt>

[Referência do Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 






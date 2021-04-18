---
title: Sombreadores HLSL de raytracing do Direct3D 12
description: Os seguintes sombreadores HLSL dão suporte ao pipeline do Direct3D 12 raytracing.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1dd545532208095781f6fbca25480a6dbfd31e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105749500"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a>Sombreadores HLSL de raytracing do Direct3D 12

Os seguintes sombreadores HLSL dão suporte ao pipeline do Direct3D 12 raytracing. Esses sombreadores são funções compiladas em uma biblioteca, com o modelo de destino lib_6_3 e identificados por um atributo *[Shader ("shadertype")]* na função de sombreador. Consulte **intrínsecos** e **valores do sistema** para ver o que é permitido para cada tipo de sombreador.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                       | Descrição                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Sombreador de todos os cliques**](any-hit-shader.md)<br/>                              | Um sombreador que é invocado quando Ray interseções não são opacas.<br/>                                                                                                                                                                                                                                              |
| [**Sombreador resgatável**](callable-shader.md)<br/>                              | Um sombreador que é invocado de outro sombreador com o intrínseco **CallShader** .<br/>                                                                                                                                                                                                                                              |
| [**Sombreador do clique mais próximo**](closest-hit-shader.md)<br/>                              | Um sombreador que é invocado quando está habilitado e a visita mais próxima foi determinada ou Ray a pesquisa de interseção terminou.<br/>                                                                                                                                                                                                                                              |
| [**Sombreador de interseção**](intersection-shader.md)<br/>                              | Um sombreador que é usado para implementar primitivos de interseção personalizados para raios interseccionando um volume limitado associado (caixa delimitadora).<br/>                                                                                                                                                                                                                                              |
| [**Sombreador de resolução**](miss-shader.md)<br/>                              | Um sombreador que é invocado quando nenhuma interseção de Ray é encontrada ou aceita.<br/>                                                                                                                                                                                                                                              |
| [**Sombreador da geração de raio**](ray-generation-shader.md)<br/>                              | Um sombreador que chama [**TraceRay**](traceray-function.md) para gerar raios.<br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência principal](direct3d-12-core-reference.md)
</dt> <dt>

[Referência do Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 






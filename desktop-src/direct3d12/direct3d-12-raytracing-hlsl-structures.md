---
title: Raytracing HLSL structures (Direct3D 12)
description: As estruturas HLSL a seguir são suportadas pelo pipeline de raytracing do Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c4227c2a0a1c99929a1025d0410ba6c769c932a740d6ed0a6c4b5f721f3fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045544"
---
# <a name="raytracing-hlsl-structures-direct3d-12"></a>Raytracing HLSL structures (Direct3D 12)

As estruturas HLSL a seguir são suportadas pelo pipeline de raytracing do Direct3D 12.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                       | Descrição                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Estrutura do parâmetro de chamada**](call-parameter-structure.md)<br/>                              | Uma estrutura definida pelo usuário fornecida como um argumento de saída para uma chamada CallShader e como um parâmetro inout para o sombreador que pode ser chamado.<br/>                                                                                                                                                                                                                                              |
| [**Estrutura de atributos de interseção**](intersection-attributes.md)<br/>                              | Uma estrutura definida pelo usuário fornecida como um argumento de entrada em uma chamada [**TraceRay**](traceray-function.md) e como um parâmetro de entrada nos tipos de sombreador que podem acessar a carga de raio.<br/>                                                                                                                                                                                                                                              |
| [**Estrutura do conteúdo do raio**](ray-payload.md)<br/>                              | Uma estrutura definida pelo usuário fornecida como um argumento de entrada em uma chamada [**TraceRay**](traceray-function.md) e como um parâmetro de entrada nos tipos de sombreador que podem acessar a carga de raio.<br/>                                                                                                                                                                                                                                              |
| [**Estrutura RayDesc**](raydesc.md)<br/>                              | Sinalizadores passados para [**a função TraceRay**](traceray-function.md) para substituir o comportamento de transparência, rebaixamento e início.<br/>                                                                                                                                                                                                                                              |





 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência principal](direct3d-12-core-reference.md)
</dt> <dt>

[Referência do Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 






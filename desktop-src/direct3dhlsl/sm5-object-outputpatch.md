---
title: OutputPatch
description: OutputPatch
ms.assetid: 24841938-6c84-4e1f-ba8a-a81b589bdd51
keywords:
- OutputPatch HLSL
topic_type:
- apiref
api_name:
- OutputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea806da8fe9b4219490c26b84e5b77f6f92b324a72850c79080de6ca363ef4e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725235"
---
# <a name="outputpatch"></a>OutputPatch

Representa uma matriz de pontos de controle de saída que estão disponíveis para a função de constante patch do sombreador envoltória, bem como o sombreador de domínio.



| Método                                                       | Descrição                         |
|--------------------------------------------------------------|-------------------------------------|
| [**Operador\[\]**](sm5-object-outputpatch-operatorindex.md) | Obtém uma variável de recurso somente leitura. |



 

Além disso, a classe InputPatch dá suporte às seguintes propriedades:



| Propriedades | Tipo | Descrição                   |
|------------|------|-------------------------------|
| Comprimento     | uint | O número de pontos de controle. |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Este objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





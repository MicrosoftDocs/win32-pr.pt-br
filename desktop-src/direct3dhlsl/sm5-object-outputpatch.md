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
ms.openlocfilehash: 4c77a30a2ff23bdc292d45df6514ef00fab53463
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006388"
---
# <a name="outputpatch"></a>OutputPatch

Representa uma matriz de pontos de controle de saída que estão disponíveis para a função de constante patch do sombreador envoltória, bem como o sombreador de domínio.



| Método                                                       | Descrição                         |
|--------------------------------------------------------------|-------------------------------------|
| [**Operador\[\]**](sm5-object-outputpatch-operatorindex.md) | Obtém uma variável de recurso somente leitura. |



 

Além disso, a classe InputPatch dá suporte às seguintes propriedades:



| Propriedades | Tipo | Description                   |
|------------|------|-------------------------------|
| Comprimento     | uint | O número de pontos de controle. |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Este objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





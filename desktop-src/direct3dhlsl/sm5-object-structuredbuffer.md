---
title: StructuredBuffer
description: Um buffer somente leitura, que pode usar um tipo T que é uma estrutura.
ms.assetid: fe2ec0b8-0e19-42b6-9dad-c992ecdeb19e
keywords:
- StructuredBuffer HLSL
topic_type:
- apiref
api_name:
- StructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524078780ac28d691c4999491bed146a04d34439
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988665"
---
# <a name="structuredbuffer"></a>StructuredBuffer

Um buffer somente leitura, que pode usar um tipo T que é uma estrutura.



| Método                                                             | Descrição                            |
|--------------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-structuredbuffer-getdimensions.md) | Obtém as dimensões do recurso.          |
| [**Carregamento**](structuredbuffer-load.md)                              | Lê dados de buffer.                     |
| [**Operador\[\]**](sm5-object-structuredbuffer-operatorindex.md)  | Retorna uma variável de recurso somente leitura. |



 

O formato UAV associado a esse recurso precisa ser criado com o formato \_ desconhecido de formato dxgi \_ .

Para saber mais sobre [buffers estruturados](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources), consulte o material de visão geral.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                                                                                                                                                            | Com suporte |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| O [Shader Model 5](d3d11-graphics-reference-sm5.md) e os modelos de sombreador superior modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponível para sombreadores de computação e pixel no Direct3D 11 em alguns dispositivos Direct3D 10).<br/> | sim       |



 

Esse objeto tem suporte para os seguintes tipos de sombreadores.



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 


---
title: Preciso
description: Desabilitação por instrução de refatoração aritmética.
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c7929a7ebab01b17aca3e11cb98de8796bf568cd08a3a7b04d8f3395f531d72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067906"
---
# <a name="precise"></a>Preciso

Desabilitação por instrução de refatoração aritmética.



| Preciso (máscara de componente) |
|--------------------------|



 

Este modificador requer o sinalizador de sombreador global "refatoração \_ permitida". Quando a refatoração \_ permitida estiver presente, os resultados de componentes individuais de instruções individuais poderão ser forçados a permanecerem precisos ou não podem ser refatoráveis por compiladores ou drivers. Se os componentes de uma instrução [**Mad**](mad--sm4---asm-.md) estiverem marcados como **precisos**, o hardware deverá executar uma instrução **Mad** ou o equivalente exato e não poderá dividi-lo em uma multiplicação seguida por um Add. Por outro lado, um multiplicado seguido por um Add, onde ou ambos são sinalizados como **precisos**, não podem ser mesclados em um **Mad** de fusível.

Se a refatoração \_ permitida não tiver sido especificada, o modificador **preciso** não será permitido. Isso não é necessário porque tudo é preciso. O modificador **preciso** afeta qualquer operação, não apenas aritmética.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse modificador tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de instrução do Shader Model 5](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 





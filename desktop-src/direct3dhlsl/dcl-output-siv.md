---
title: dcl_output_siv (sm4-ASM)
description: '\_ \_ SIV de saída DCL (sm4-ASM)'
ms.assetid: 5a87a113-7413-48ef-9a6a-13eb185650be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3035724a76aff71c2ba2b7500874365ea284f55b0bf16389b3d83c99205e606b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515673"
---
# <a name="dcl_output_siv-sm4---asm"></a>\_ \_ SIV de saída DCL (sm4-ASM)

Declara um registro de saída que contém um parâmetro [de valor do sistema](dx-graphics-hlsl-semantics.md) .



| DCL \_ \_ de saída SIV em \[ *. máscaras* \] , *systemvalue* |
|------------------------------------------------|



 



| Item                                                                                                                               | Descrição                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*<br/>                                                     | \[em \] um registro de dados de saída; *N* é um inteiro que denota o número do registro.<br/>                                                      |
| <span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*<br/>                                                         | \[em \] opcional. Uma máscara de componente (. xyzw) que especifica qual dos componentes de registro usar.<br/>                                        |
| <span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*<br/> | \[no \] nome do valor do sistema, que é uma cadeia de caracteres (consulte a [semântica do valor do sistema](dx-graphics-hlsl-semantics.md)) sem o prefixo "VA \_ ".<br/> |



 

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               |              |



 

Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.

## <a name="example"></a>Exemplo

Veja alguns exemplos.


```
dcl_output o[0].y
dcl_output_siv o[0].w, clipDistance
dcl_output_siv o[0].z, cullDistance
```



## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






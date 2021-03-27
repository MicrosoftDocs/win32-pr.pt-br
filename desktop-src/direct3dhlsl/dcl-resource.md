---
title: dcl_resource (sm4-ASM)
description: '\_recurso DCL (sm4-ASM)'
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb65a8ea83feaf2fec80403fc9ac6c2ab38c1936
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638892"
---
# <a name="dcl_resource-sm4---asm"></a>\_recurso DCL (sm4-ASM)

Declara um recurso de entrada de sombreador não multiamostrado.



| \_recurso DCL *TN*, *ResourceType*, *ReturnType (s)* |
|-----------------------------------------------------|



 

Declara um recurso de entrada de sombreador com uma amostra.



| \_recurso DCL *TN*, *tamanho do ResourceType \[ \] NN*, *ReturnType (s)* |
|---------------------------------------------------------------|



 



| Item                                                                                                                                                     | Descrição                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*<br/>                                                                           | \[no \] registro de textura, onde *N* é um inteiro que denota o número do registro.<br/>                                                                                                                                                                        |
| <span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*<br/>                                   | \[em \] qualquer tipo de objeto listado na página de [objeto de textura](dx-graphics-hlsl-to-type.md) .<br/>                                                                                                                                                                     |
| <span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*tamanho de resourceType \[ \] nn*<br/> | \[em \] um tipo de objeto Texture2D ou Texture2DArray (consulte a página [Texture-Object](dx-graphics-hlsl-to-type.md) ); *size* é um inteiro opcional que denota o número de elementos na matriz; *NN* é um inteiro que denota o número de multiamostras.<br/> |
| <span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType (s)*<br/>                               | \[no \] tipo de retorno por componente, que é um dos seguintes: UNORM, SNORM, Santo, uint ou float. O número de tipos de retorno pode ser de até 1 (se todos os componentes forem do mesmo tipo), mas puder ser de até quatro.<br/>                                          |



 

Um recurso é acessado no HLSL usando [Load](dx-graphics-hlsl-to-load.md); uma textura sem amostra também pode ser acessada usando qualquer um dos métodos de exemplo de [objeto de textura](dx-graphics-hlsl-to-type.md) HLSL.

Se um recurso estiver associado a um estágio do sombreador, o formato de recurso será validado em relação ao tipo de retorno.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.

## <a name="example"></a>Exemplo

Veja um exemplo.


```
dcl_resource t3, buffer, UNORM
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

 

 






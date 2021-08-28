---
title: dcl_resource (sm4 – asm)
description: recurso \_ dcl (sm4 – asm)
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f23fac2f6671584c69ecad045d13e885e86fb260164675da3bc51f7edf847f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515631"
---
# <a name="dcl_resource-sm4---asm"></a>recurso \_ dcl (sm4 – asm)

Declara um recurso de entrada de sombreador não multisampled.



| dcl \_ resource *tN*, *resourceType*, *returnType(s)* |
|-----------------------------------------------------|



 

Declara um recurso de entrada de sombreador multisampled.



| dcl \_ resource *tN*, *resourceType size \[ \] NN,* *returnType(s)* |
|---------------------------------------------------------------|



 



| Item                                                                                                                                                     | Descrição                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*<br/>                                                                           | \[em \] O registro de textura, em que *N* é um inteiro que indica o número do registro.<br/>                                                                                                                                                                        |
| <span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*Resourcetype*<br/>                                   | \[em \] Qualquer tipo de objeto listado na página [texture-object.](dx-graphics-hlsl-to-type.md)<br/>                                                                                                                                                                     |
| <span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType \[ size \] NN*<br/> | \[em \] Um tipo de objeto Texture2D ou Texture2DArray (consulte a página [texture-object);](dx-graphics-hlsl-to-type.md) *size* é um inteiro opcional que indica o número de elementos na matriz; *NN* é um inteiro que indica o número de multisamplos.<br/> |
| <span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType(s)*<br/>                               | \[em Tipo de retorno por componente, que é um \] dos seguintes: UNORM, SNORM, SINT, UINT ou FLOAT. O número de tipos de retorno pode ser tão poucos quanto 1 (se todos os componentes são do mesmo tipo), mas pode ser de até quatro.<br/>                                          |



 

Um recurso é acessado em HLSL usando [carregar](dx-graphics-hlsl-to-load.md); uma textura não multisampled também pode ser acessada [](dx-graphics-hlsl-to-type.md) usando qualquer um dos métodos de exemplo de objeto de textura HLSL.

Se um recurso estiver vinculado a um estágio de sombreador, o formato do recurso será validado em relação ao tipo de retorno.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Essa instrução é incluída para auxiliar na depuração de um sombreador no assembly; não é possível autor de um sombreador na linguagem de assembly usando o Modelo de Sombreador 4.

## <a name="example"></a>Exemplo

Veja um exemplo.


```
dcl_resource t3, buffer, UNORM
```



## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 






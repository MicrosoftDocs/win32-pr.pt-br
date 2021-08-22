---
title: descartar (sm4-ASM)
description: Sinaliza condicionalmente os resultados do sombreador de pixel a serem descartados quando o fim do programa for atingido.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6b5744ee8cf8d2953247711d95fe5d5ec6f96c36c700e1a38ce4e0cb1e1ff5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986596"
---
# <a name="discard-sm4---asm"></a>descartar (sm4-ASM)

Sinaliza condicionalmente os resultados do sombreador de pixel a serem descartados quando o fim do programa for atingido.



| descartar { \_ z \|\_NZ} src0. Select \_ componente |
|-------------------------------------------|



 



| Item                                                            | Descrição                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] valor que determina se deve-se descartar o pixel atual que está sendo processado.<br/> |



 

## <a name="remarks"></a>Comentários

Essa instrução sinaliza o pixel atual como encerrado, enquanto continua a execução, para que outros pixels em execução em paralelo possam obter derivações, se necessário. Embora a execução Continue, toda a saída do sombreador de pixel grava antes ou depois que a instrução de **descarte** é descartada.

Para **descarte \_ z**, se todos os bits no *\_ componente src0. Select* forem zero, o pixel será Descartado.

Para **descartar \_ NZ**, se qualquer um dos bits no *\_ componente src0. Select* for diferente de zero, o pixel será Descartado.

Além disso, a instrução de **descarte** pode estar presente dentro de qualquer construção de controle de fluxo.

Várias instruções de **descarte** podem estar presentes em um sombreador e, se alguma for executada, o pixel será encerrado.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 






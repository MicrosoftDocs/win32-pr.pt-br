---
title: Formato de efeito (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: 'Saiba mais sobre: Formato de efeito (Direct3D 11)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7644e433f6c19df20cb2417659cf575e0613f93b0d53f6494ad6ee1422a55b9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792066"
---
# <a name="effect-format-direct3d-11"></a>Formato de efeito (Direct3D 11)

Um efeito (que geralmente é armazenado em um arquivo com uma extensão de arquivo .fx) declara o estado do pipeline definido por um efeito. O estado de efeito pode ser dividido em três categorias:

-   [Variáveis](d3d11-effect-variable-syntax.md), que geralmente são declaradas na parte superior de um efeito.
-   Funções , que implementam código de sombreador ou são [usadas](d3d11-effect-function-syntax.md)como funções auxiliares por outras funções.
-   [Técnicas ,](d3d11-effect-technique-syntax.md)que podem ser organizadas em grupos de efeito e implementam sequências de renderização usando uma ou mais passagens de efeito. Cada passagem define um ou mais [grupos de estado](d3d11-effect-states.md) e chama funções de sombreador.

![diagrama das categorias de declarações para efeitos, incluindo variáveis na parte superior, funções no meio e técnicas na parte inferior](images/d3d10-effect-intro.png)

O diagrama anterior mostra as categorias de estado de efeito.

A definição do formato binário de efeito pode ser encontrada em \\ Binary EffectBinaryFormat.h no código-fonte de efeitos.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                   | Descrição                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Sintaxe de variável de efeito](d3d11-effect-variable-syntax.md)<br/>   | Uma variável de efeito é declarada com a sintaxe descrita nesta seção.<br/>                                 |
| [Sintaxe de anotação](d3d11-effect-annotation-syntax.md)<br/>      | Uma anotação é uma informação definida pelo usuário, declarada com a sintaxe descrita nesta seção.<br/> |
| [Sintaxe da função Effect](d3d11-effect-function-syntax.md)<br/>   | Uma função de efeito é escrita em HLSL e é declarada com a sintaxe descrita nesta seção.<br/>          |
| [Sintaxe da técnica de efeito](d3d11-effect-technique-syntax.md)<br/> | Uma técnica de efeito é declarada com a sintaxe descrita nesta seção.<br/>                                |
| [Grupos de estado de efeito](d3d11-effect-states.md)<br/>               | Estados de efeito são pares de valores de nome na forma de uma expressão.<br/>                                          |
| [Sintaxe do grupo de efeitos](d3d11-effect-group-syntax.md)<br/>         | Um grupo de efeitos é declarado com a sintaxe descrita nesta seção.<br/>                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de Efeitos 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 






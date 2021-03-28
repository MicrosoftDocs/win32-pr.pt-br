---
title: Formato de efeito (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: 'Saiba mais sobre: formato de efeito (Direct3D 11)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c08589fcb041591591d033b88e4fafe597e98520
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164011"
---
# <a name="effect-format-direct3d-11"></a>Formato de efeito (Direct3D 11)

Um efeito (que geralmente é armazenado em um arquivo com uma extensão de arquivo. FX) declara o estado do pipeline definido por um efeito. O estado do efeito pode ser basicamente dividido em três categorias:

-   [Variáveis](d3d11-effect-variable-syntax.md), que geralmente são declaradas na parte superior de um efeito.
-   [Funções](d3d11-effect-function-syntax.md), que implementam o código de sombreador ou são usadas como funções auxiliares por outras funções.
-   [Técnicas](d3d11-effect-technique-syntax.md), que podem ser organizadas em grupos de efeito e implementam sequências de renderização usando um ou mais efeitos aprovados. Cada passagem define um ou mais [grupos de Estados](d3d11-effect-states.md) e chama funções de sombreador.

![diagrama das categorias de declarações para efeitos, incluindo variáveis na parte superior, funções no meio e técnicas na parte inferior](images/d3d10-effect-intro.png)

O diagrama anterior mostra as categorias de estado de efeito.

A definição do formato binário de efeito pode ser encontrada em \\ EffectBinaryFormat. h binário no código-fonte de efeitos.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                   | Descrição                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Sintaxe da variável de efeito](d3d11-effect-variable-syntax.md)<br/>   | Uma variável de efeito é declarada com a sintaxe descrita nesta seção.<br/>                                 |
| [Sintaxe da anotação](d3d11-effect-annotation-syntax.md)<br/>      | Uma anotação é uma informação definida pelo usuário, declarada com a sintaxe descrita nesta seção.<br/> |
| [Sintaxe da função de efeito](d3d11-effect-function-syntax.md)<br/>   | Uma função de efeito é escrita em HLSL e é declarada com a sintaxe descrita nesta seção.<br/>          |
| [Sintaxe da técnica de efeito](d3d11-effect-technique-syntax.md)<br/> | Uma técnica de efeito é declarada com a sintaxe descrita nesta seção.<br/>                                |
| [Grupos de estado de efeito](d3d11-effect-states.md)<br/>               | Os Estados de efeito são pares de valor de nome na forma de uma expressão.<br/>                                          |
| [Sintaxe do grupo de efeitos](d3d11-effect-group-syntax.md)<br/>         | Um grupo de efeitos é declarado com a sintaxe descrita nesta seção.<br/>                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência dos efeitos 11](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 






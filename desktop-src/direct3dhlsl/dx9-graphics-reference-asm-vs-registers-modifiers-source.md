---
title: Modificadores de registro de origem do sombreador de vértice
description: Os modificadores de origem podem ser aplicados para modificar os dados lidos de um registro de origem antes que os dados sejam usados pela instrução.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c663741da50620e03cfde9f13d67a0c0063453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364210"
---
# <a name="vertex-shader-source-register-modifiers"></a>Modificadores de registro de origem do sombreador de vértice

Os modificadores de origem podem ser aplicados para modificar os dados lidos de um registro de origem antes que os dados sejam usados pela instrução.

## <a name="negate"></a>Negar

Negar o conteúdo do registro de origem.



| Modificador de componente | Description     |
|--------------------|-----------------|
| \- d               | Negação de origem |



 

O modificador de negação não pode ser usado no segundo registro de origem dessas instruções: [M3X2-vs](m3x2---vs.md), [m3x3-vs](m3x3---vs.md), [M3x4-vs](m3x4---vs.md), [m4x3-vs](m4x3---vs.md), [m4x4-vs](m4x4---vs.md).



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \-                     | x    | x    | x    | x     | x    | x     |



 

## <a name="absolute-value"></a>Valor absoluto

Pegue o valor absoluto do registro.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| abs                    |      |      |      |       | x    | x     |



 

Se qualquer sombreador da versão 3 ler um ou mais registros de flutuação constante (c \# ), um dos seguintes deve ser verdadeiro.

-   Todos os registros constantes de ponto flutuante devem usar o modificador ABS.
-   Nenhum dos registros constantes de ponto flutuante pode usar o modificador ABS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 





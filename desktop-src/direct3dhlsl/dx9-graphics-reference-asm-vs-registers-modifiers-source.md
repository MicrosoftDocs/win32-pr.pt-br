---
title: Modificadores de registro de origem do sombreador de vértice
description: Os modificadores de origem podem ser aplicados para modificar os dados lidos de um registro de origem antes que os dados sejam usados pela instrução .
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f50942d32691d9dc76aa30ddcef36df390fccfe058c31af3527c0eafe0d7df0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067976"
---
# <a name="vertex-shader-source-register-modifiers"></a>Modificadores de registro de origem do sombreador de vértice

Os modificadores de origem podem ser aplicados para modificar os dados lidos de um registro de origem antes que os dados sejam usados pela instrução .

## <a name="negate"></a>Negar

Negar o conteúdo do registro de origem.



| Modificador de componente | Descrição     |
|--------------------|-----------------|
| \- R               | Negação de origem |



 

O modificador de negação não pode ser usado no segundo registro de origem destas instruções: [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m3x4 - vs](m3x4---vs.md), [m4x3 - vs](m4x3---vs.md), [m4x4 - vs](m4x4---vs.md).



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| \-                     | x    | x    | x    | x     | x    | x     |



 

## <a name="absolute-value"></a>Valor absoluto

Pegue o valor absoluto do registro.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| abs                    |      |      |      |       | x    | x     |



 

Se qualquer sombreador da versão 3 ler de um ou mais registros float constantes (c), um dos seguintes deve \# ser true.

-   Todos os registros de ponto flutuante constante devem usar o modificador abs.
-   Nenhum dos registros de ponto flutuante constante pode usar o modificador abs.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro do sombreador de vértice](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 





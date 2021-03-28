---
title: Registro de predicado (referência de HLSL VS)
description: Este registro de saída do sombreador de vértice contém um valor booliano por canal.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f558a5fee10d0403eeaacab9dc29ff3ea52b427c
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104006940"
---
# <a name="predicate-register-hlsl-vs-reference"></a>Registro de predicado (referência de HLSL VS)

Este registro de saída do sombreador de vértice contém um valor booliano por canal.

Um registro de predicado tem suporte nas seguintes versões.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| registro de predicado     |      |      |       | x    | x    | x     |



 

Aqui estão as propriedades do registro.



| Tipo de registro | Contagem | R/W | \# Portas de leitura | \# Leituras/InStr | Dimensão | RelAddr | Padrões | Requer DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicado (p)  | 1     | R/W | 1             | 1             | 4         | N/D     | Nenhum     | N            |



 

O registro de predicado pode ser modificado com [setp \_ comp-vs](setp-comp---vs.md). Não há valores padrão para esse registro, um aplicativo precisa definir o registro antes de ser usado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 





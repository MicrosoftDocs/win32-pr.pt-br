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
ms.openlocfilehash: 28392f7bb9c2f59bd766e42ec21fb87a854b08bedd8336ebb6f7249b7eccb940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119570"
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

 

 





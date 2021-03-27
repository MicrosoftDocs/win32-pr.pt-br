---
title: Registro de predicado (referência do HLSL PS)
description: O registro de saída do sombreador de pixel contém um valor booliano por canal.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54c0706b110e04548c836bed8ae794f8da73747e
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103638912"
---
# <a name="predicate-register-hlsl-ps-reference"></a>Registro de predicado (referência do HLSL PS)

O registro de saída do sombreador de pixel contém um valor booliano por canal.

Um registro de predicado tem suporte nas seguintes versões:



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| registro de predicado    |      |      |      |      |      |       | x    | x    | x     |



 

Aqui estão as propriedades do registro.



| Tipo de registro | Contagem | R/W | \# Portas de leitura | \# Leituras/InStr | Dimensão | RelAddr | Padrões | Requer DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicado (p)  | 1     | R/W | 1             | 1             | 4         | N/D     | Nenhum     | N            |



 

O registro de predicado pode ser modificado com [setp \_ comp-PS](setp-comp---ps.md). Não há valores padrão para este registro; um aplicativo precisa definir o registro antes que ele seja usado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 





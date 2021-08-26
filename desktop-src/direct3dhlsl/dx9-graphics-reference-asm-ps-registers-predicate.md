---
title: Registro de predicado (referência de PS HLSL)
description: Esse registro de saída do sombreador de pixel contém um valor booliana por canal.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cc8404c9a6be87951142ff3473b283a57f4814b729a8ad5a462f9069b20f3ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950026"
---
# <a name="predicate-register-hlsl-ps-reference"></a>Registro de predicado (referência de PS HLSL)

Esse registro de saída do sombreador de pixel contém um valor booliana por canal.

Há suporte para um registro de predicado nas seguintes versões:



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| registro de predicado    |      |      |      |      |      |       | x    | x    | x     |



 

Aqui estão as propriedades de registro.



| Tipo de registro | Contagem | R/W | \# Ler portas | \# Leituras/inst | Dimensão | RelAddr | Padrões | Requer DCL |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| Predicado(p)  | 1     | R/W | 1             | 1             | 4         | N/D     | Nenhum     | N            |



 

O registro de predicado pode ser modificado [com setp \_ comp - ps](setp-comp---ps.md). Não há valores padrão para esse registro; um aplicativo precisa definir o registro antes de ser usado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 





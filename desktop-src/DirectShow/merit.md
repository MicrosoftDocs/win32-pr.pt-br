---
description: Os valores de valores de valor definem a ordem na qual o Gerenciador Graph Filtro tenta adicionar filtros durante a criação do grafo.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: ( Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a55c112f1a08d63e45d5385f525371ae9642c1b01a1b4af5d7747b042efffe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073010"
---
# <a name="merit"></a>Mérito

Os valores de valores de valor definem a ordem na qual o Gerenciador Graph Filtro tenta adicionar filtros durante a criação do grafo.

<dl> <span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**VALOR \_** <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> (0X800000) PREFERENCIAIS (0X600000) **PREFERÍVEL \_** (0X400000) NÃO USE <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **\_** <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> (0X200000) PREFERENCIAIS **\_ \_ \_** <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> (0X200000) **\_ \_** <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **0X100000) PREFERENCIAIS \_ \_** (0X100050)
</dl>

## <a name="remarks"></a>Comentários

Cada filtro é registrado com um valor de fundamento. Quando o gerenciador de grafo de filtro cria um grafo, ele enumera todos os filtros registrados com o tipo de mídia correto. Em seguida, ele os tenta em ordem de bem-estar, do mais alto ao mais baixo. (Ele usa critérios adicionais para escolher entre filtros com igualdade de igualdade.) Ele nunca tenta filtros com um valor de igualdade menor ou igual a **TAMBÉM \_ NÃO \_ \_ USE**.

Um filtro que nunca deve ser considerado para reprodução comum deve ter um fundamento **DE NÃO \_ \_ \_ USAR OU menos.** Os filtros podem ser registrados com valores intermediários não definidos por essa enumeração, como **SEMPRE \_ NORMAL** + 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes e GUIDs](constants-and-guids.md)
</dt> <dt>

[Diretrizes para registrar filtros](guidelines-for-registering-filters.md)
</dt> <dt>

[Inteligência Conexão](intelligent-connect.md)
</dt> </dl>

 

 





---
description: Os valores de mérito definem a ordem na qual o Gerenciador do grafo de filtro tenta adicionar filtros durante a criação do grafo.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Mérito (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758462"
---
# <a name="merit"></a>Núcleo

Os valores de mérito definem a ordem na qual o Gerenciador do grafo de filtro tenta adicionar filtros durante a criação do grafo.

<dl> <span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**Mérito \_ Preferível** (0x800000) <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **mérito \_ normal** (0x600000) mérito <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **\_ improvável** (0x400000) <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **mérito \_ \_ não \_ usa** (0x200000) ( <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **mérito \_ SW \_ compressor** <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **\_ \_** ) (0x100000) (núcleo de HW)
</dl>

## <a name="remarks"></a>Comentários

Cada filtro é registrado com um valor de mérito. Quando o Gerenciador de gráfico de filtro cria um grafo, ele enumera todos os filtros registrados com o tipo de mídia correto. Em seguida, ele os tenta em ordem de mérito, do mais alto para o mais baixo. (Ele usa critérios adicionais para escolher entre os filtros com o mesmo mérito.) Ele nunca tenta filtros com um valor de mérito menor ou igual a **mérito \_ não \_ é \_ usado**.

Um filtro que nunca deve ser considerado para reprodução comum deve ter um mérito de **mérito \_ \_ não \_ usar** ou menos. Os filtros podem ser registrados com valores intermediários não definidos por essa enumeração, como **mérito \_ normal** + 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes e GUIDs](constants-and-guids.md)
</dt> <dt>

[Diretrizes para o registro de filtros](guidelines-for-registering-filters.md)
</dt> <dt>

[Conexão inteligente](intelligent-connect.md)
</dt> </dl>

 

 





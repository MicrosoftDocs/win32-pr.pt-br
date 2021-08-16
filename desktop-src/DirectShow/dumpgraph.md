---
description: A função DumpGraph envia informações sobre um grafo de filtro para o local de saída de depuração. Ignorado em builds de varejo.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: Função DumpGraph (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac09cc3381ab1b5f85f523d1c822768b3e2f87b6bcf08f1877680349072c216
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820955"
---
# <a name="dumpgraph-function"></a>Função DumpGraph

A `DumpGraph` função envia informações sobre um grafo de filtro para o local de saída de depuração. Ignorado em builds de varejo.

## <a name="syntax"></a>Sintaxe


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGraph* 
</dt> <dd>

Ponteiro para a interface [**IFilterGraph no**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) gerenciador de grafo de filtro.

</dd> <dt>

*dwLevel* 
</dt> <dd>

Nível de registro em log. A função gera uma mensagem LOG \_ TRACE com o nível de log especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 





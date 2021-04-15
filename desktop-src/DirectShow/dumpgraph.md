---
description: A função DumpGraph envia informações sobre um grafo de filtro para o local de saída de depuração. Ignorado em compilações de varejo.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: Função DumpGraph (Wxdebug. h)
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
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747572"
---
# <a name="dumpgraph-function"></a>Função DumpGraph

A `DumpGraph` função envia informações sobre um grafo de filtro para o local de saída de depuração. Ignorado em compilações de varejo.

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

Ponteiro para a interface [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) no Gerenciador do grafo de filtro.

</dd> <dt>

*dwLevel* 
</dt> <dd>

Nível de log. A função gera uma \_ mensagem de rastreamento de log com o nível de log especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxdebug. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de saída de depuração](debug-output-functions.md)
</dt> </dl>

 

 





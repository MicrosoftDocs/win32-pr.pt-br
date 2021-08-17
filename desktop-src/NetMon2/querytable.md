---
description: A estrutura QUERYTABLE fornece uma lista dos computadores que estão usando o Monitor de Rede para capturar dados de rede.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: Estrutura QUERYTABLE (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 9b8f291f055bfba159309b6c75a54d95514ed9c7614eb0456a4870e657f04209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555366"
---
# <a name="querytable-structure"></a>Estrutura QUERYTABLE

A **estrutura QUERYTABLE** fornece uma lista dos computadores que estão usando o Monitor de Rede para capturar dados de rede.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a>Membros

<dl> <dt>

**nStationQueries**
</dt> <dd>

Na entrada, o número máximo de computadores que você Monitor de Rede retornar.

Na saída, o número de [estruturas STATIONQUERY](stationquery.md) retornadas por Monitor de Rede. Cada **estrutura STATIONQUERY** representa um computador que está capturando dados no momento.

</dd> <dt>

**StationQuery**
</dt> <dd>

Na entrada, uma matriz de estruturas [STATIONQUERY](stationquery.md) vazias que contém o número de elementos especificados em **nStationQueries**.

Na saída, uma estrutura [STATIONQUERY preenchida](stationquery.md) para cada computador que está capturando dados. O número de elementos preenchidos é retornado por **nStationQueries**.

</dd> </dl>

## <a name="remarks"></a>Comentários

A memória dessa estrutura e a [matriz STATIONQUERY](stationquery.md) devem ser alocadas pelo aplicativo de chamada e liberadas depois que as informações não são mais necessárias.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC::QueryStations](idelaydc-querystations.md)
</dt> <dt>

[I LTD::QueryStations](iesp-querystations.md)
</dt> <dt>

[IRTC::QueryStations](irtc-querystations.md)
</dt> <dt>

[IStats::QueryStations](istats-querystations.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 





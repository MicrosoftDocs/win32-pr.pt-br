---
description: A estrutura de QUERYTABLE fornece uma lista dos computadores que atualmente estão usando Monitor de Rede para capturar dados de rede.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: Estrutura de QUERYTABLE (Netmon. h)
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
ms.openlocfilehash: 2b2976a56b43c55fccb9acb0c593b0dfd37e4404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770141"
---
# <a name="querytable-structure"></a>Estrutura de QUERYTABLE

A estrutura de **QUERYTABLE** fornece uma lista dos computadores que atualmente estão usando monitor de rede para capturar dados de rede.

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

Na entrada, o número máximo de computadores que você deseja que Monitor de Rede retorne.

Na saída, o número de estruturas [STATIONQUERY](stationquery.md) retornadas pelo monitor de rede. Cada estrutura **STATIONQUERY** representa um computador que está capturando dados no momento.

</dd> <dt>

**StationQuery**
</dt> <dd>

Na entrada, uma matriz de estruturas [STATIONQUERY](stationquery.md) vazias que contém o número de elementos especificados em **nStationQueries**.

Na saída, uma estrutura [STATIONQUERY](stationquery.md) preenchida para cada computador que está capturando dados. O número de elementos preenchidos é retornado por **nStationQueries**.

</dd> </dl>

## <a name="remarks"></a>Comentários

A memória para essa estrutura e a matriz [STATIONQUERY](stationquery.md) devem ser alocadas pelo aplicativo de chamada e liberadas depois que as informações não forem mais necessárias.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC::QueryStations](idelaydc-querystations.md)
</dt> <dt>

[IESP::QueryStations](iesp-querystations.md)
</dt> <dt>

[IRTC::QueryStations](irtc-querystations.md)
</dt> <dt>

[IStats::QueryStations](istats-querystations.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 





---
description: A enumeração de sinalizadores de pesquisa do DEXTERF \_ Track \_ \_ especifica as condições de limite em uma pesquisa de um objeto na linha do tempo.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: Enumeração de DEXTERF_TRACK_SEARCH_FLAGS (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750279"
---
# <a name="dexterf_track_search_flags-enumeration"></a>\_Enumeração de \_ sinalizadores de pesquisa do DEXTERF Track \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `DEXTERF_TRACK_SEARCH_FLAGS` enumeração Especifica as condições de limite em uma pesquisa de um objeto na linha do tempo.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**limite de DEXTERF \_**
</dt> <dd>

Procure um objeto que abranja o tempo especificado.

</dd> <dt>

<span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF \_ exatamente \_ em**
</dt> <dd>

Pesquisar um objeto que inicia exatamente na hora especificada.

</dd> <dt>

<span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**\_encaminhamentos de DEXTERF**
</dt> <dd>

Pesquisar um objeto que inicia na hora especificada ou posteriormente.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essas condições de limite são resumidas na tabela a seguir.



| Valor de enumeração    | Condição de limite                        |
|----------------------|-------------------------------------------|
| limite de DEXTERF \_    | Iniciar <= tempo de > do TimeStop<br/> |
| DEXTERF \_ exatamente \_ em | Início = = hora                             |
| \_encaminhamentos de DEXTERF    | Iniciar >= hora                          |



 

-   Início: hora de início do objeto recuperado.
-   Stop: hora de parada do objeto recuperado.
-   Hora: tempo de pesquisa especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>QEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 





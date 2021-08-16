---
description: Um método de construtor que fornece o mapeamento entre tipos DWORD de formato multimídia de estilo antigo e subtipos GUID. Esse método não usa parâmetros.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: Construtor FOURCCMap::FOURCCMap (Fourcc.h) – Sem parâmetros
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d856589146103e599a1cf67d2090dd64af7107d1c221c46b9c93852f989ade9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015724"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a>Construtor FOURCCMap::FOURCCMap (Fourcc.h) – Sem parâmetros

Método do construtor. O constuctor fornece o mapeamento entre tipos **DWORD** de formato multimídia de estilo antigo e subtipos **GUID.**

## <a name="syntax"></a>Sintaxe


```C++
FOURCCMap();
```



## <a name="parameters"></a>Parâmetros

Esse construtor não tem parâmetros.

## <a name="remarks"></a>Comentários

Se esse objeto for construído com o código **FOURCC,** um **GUID** será criado para corresponder a ele. Se esse objeto for criado com um **GUID existente,** o valor **FOURCC** do objeto será definido como zero. Depois disso, o **valor FOURCC** pode ser definido ou recuperado usando as funções de membro [**Set SENIORCC**](fourccmap-setfourcc.md) e [**Get SENIORCC,**](fourccmap-getfourcc.md) respectivamente.

## <a name="requirements"></a>Requisitos


| Requisito | Valor |
|-|-|
| parâmetro  | Fourcc.h (incluir Fluxos.h) |
| Biblioteca | Strmbase.lib (builds de varejo); Strmbasd.lib (builds de depuração) |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 





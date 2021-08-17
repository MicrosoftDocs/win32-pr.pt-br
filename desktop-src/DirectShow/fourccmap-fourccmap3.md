---
description: Um método de construtor que fornece o mapeamento entre tipos DWORD de formato multimídia de estilo antigo e subtipos GUID. Esse método usa o parâmetro 'pguid'.
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: Construtor FOURCCMap::FOURCCMap (Fourcc.h) – parâmetro pguid
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
ms.openlocfilehash: 2c674791418a7668d7c7597e951e9a89613b9c8150865ff123263e9d0ef9ded2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330436"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a>Construtor FOURCCMap::FOURCCMap (Fourcc.h) – parâmetro pguid

Método do construtor. O constuctor fornece o mapeamento entre tipos **DWORD** de formato multimídia de estilo antigo e subtipos **GUID.**

## <a name="syntax"></a>Sintaxe


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pguid* 
</dt> <dd>

Ponteiro para o identificador global exclusivo (**GUID).**

</dd> </dl>

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

 

 





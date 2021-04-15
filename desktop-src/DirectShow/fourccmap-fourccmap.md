---
description: Um método de construtor que fornece o mapeamento entre os tipos DWORD de formato multimídia de estilo antigo e os subtipos GUID. Esse método não usa parâmetros.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: 'Construtor FOURCCMap:: FOURCCMap (FOURCC. h) – sem parâmetros'
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
ms.openlocfilehash: cd37ac842ab46c0d46fb3db1567d42274a026c47
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105760747"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a>Construtor FOURCCMap:: FOURCCMap (FOURCC. h) – sem parâmetros

Método de construtor. O constuctor fornece o mapeamento entre os tipos **DWORD** de formato multimídia de estilo antigo e os subtipos de **GUID** .

## <a name="syntax"></a>Sintaxe


```C++
FOURCCMap();
```



## <a name="parameters"></a>Parâmetros

Este construtor não tem parâmetros.

## <a name="remarks"></a>Comentários

Se esse objeto for construído com o código **FOURCC** , um **GUID** será criado para corresponder a ele. Se esse objeto for criado com um **GUID** existente, o valor **FOURCC** do objeto será definido como zero. Depois disso, o valor **FOURCC** pode ser definido ou recuperado usando as funções de membro [**SetFOURCC**](fourccmap-setfourcc.md) e [**GetFOURCC**](fourccmap-getfourcc.md) , respectivamente.

## <a name="requirements"></a>Requisitos


| Requisito | Valor |
|-|-|
| parâmetro  | FourCC. h (incluir fluxos. h) |
| Biblioteca | Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 





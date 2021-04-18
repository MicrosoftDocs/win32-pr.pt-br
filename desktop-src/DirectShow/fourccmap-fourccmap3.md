---
description: Um método de construtor que fornece o mapeamento entre os tipos DWORD de formato multimídia de estilo antigo e os subtipos GUID. Esse método usa o parâmetro ' pGuid '.
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: 'Construtor FOURCCMap:: FOURCCMap (FOURCC. h)-parâmetro pGuid'
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
ms.openlocfilehash: 3e36f0ea58c99930d4c6c2e0929f27a43184c6be
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105757299"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a>Construtor FOURCCMap:: FOURCCMap (FOURCC. h)-parâmetro pGuid

Método de construtor. O constuctor fornece o mapeamento entre os tipos **DWORD** de formato multimídia de estilo antigo e os subtipos de **GUID** .

## <a name="syntax"></a>Sintaxe


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pguid* 
</dt> <dd>

Ponteiro para o identificador global exclusivo (**GUID**).

</dd> </dl>

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

 

 





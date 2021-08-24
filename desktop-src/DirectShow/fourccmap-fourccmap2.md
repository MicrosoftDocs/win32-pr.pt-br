---
description: Um método de construtor que fornece o mapeamento entre os tipos DWORD de formato multimídia de estilo antigo e os subtipos GUID. Esse método usa o parâmetro ' FOURCC '.
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: 'Construtor FOURCCMap:: FOURCCMap (FOURCC. h) – parâmetro FOURCC'
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
ms.openlocfilehash: 9cfd9cbb93a4d517391be0afe591d3378d9ecef32a0013ab452d31b9eecb6d59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043206"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a>Construtor FOURCCMap:: FOURCCMap (FOURCC. h) – parâmetro FOURCC

Método de construtor. O constuctor fornece o mapeamento entre os tipos **DWORD** de formato multimídia de estilo antigo e os subtipos de **GUID** .

## <a name="syntax"></a>Sintaxe


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FOURCC* 
</dt> <dd>

**DWORD** que especifica o FOURCC.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se esse objeto for construído com o código **FOURCC** , um **GUID** será criado para corresponder a ele. Se esse objeto for criado com um **GUID** existente, o valor **FOURCC** do objeto será definido como zero. Depois disso, o valor **FOURCC** pode ser definido ou recuperado usando as funções de membro [**SetFOURCC**](fourccmap-setfourcc.md) e [**GetFOURCC**](fourccmap-getfourcc.md) , respectivamente.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro  | Fourcc. h (incluir Fluxos. h) |
| Biblioteca | Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 





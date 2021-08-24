---
description: Saiba mais sobre o método de Construtor CMediaPosition. CMediaPosition (Ctlutil. h). Este método usa os parâmetros ' pName ' e ' pUnk '.
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Construtor CMediaPosition. CMediaPosition (Ctlutil. h)-pName, pUnk parâmetros
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0df3337c07ed678354515bdf0c665a5d6157f158ac6c2370a8981d8e5028b27e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634787"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a>Construtor CMediaPosition. CMediaPosition (Ctlutil. h)-pName, pUnk parâmetros

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Ponteiro para o nome do objeto, para fins de depuração. Aloque esse parâmetro na memória estática.

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para o proprietário deste objeto ou **NULL** se o objeto não for agregado.

</dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Ctlutil. h (incluir Fluxos. h) |
| Biblioteca| Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 





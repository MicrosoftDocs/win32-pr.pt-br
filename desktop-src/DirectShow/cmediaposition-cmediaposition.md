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
ms.openlocfilehash: e65f034e5f8857b21bc706bce45aa74c3c3cf966
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105771853"
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
| parâmetro | Ctlutil. h (incluir fluxos. h) |
| Biblioteca| Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 





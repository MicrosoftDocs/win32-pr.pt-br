---
description: Saiba mais sobre o método de Construtor CMediaPosition. CMediaPosition (Ctlutil. h). Este método usa os parâmetros ' pName ', ' pUnk ' e ' PHR '.
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Construtor CMediaPosition. CMediaPosition (Ctlutil. h)
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
ms.openlocfilehash: 101678ebcb851ef0fcdc8eeaa202435ca80eb796555c81e5e5d95eb4998131c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655257"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a>Construtor CMediaPosition. CMediaPosition (Ctlutil. h)-pName, pUnk, PHR parâmetros

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
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

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** .

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

 

 





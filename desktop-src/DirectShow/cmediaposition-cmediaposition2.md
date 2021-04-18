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
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105757032"
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
| parâmetro | Ctlutil. h (incluir fluxos. h) |
| Biblioteca| Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 





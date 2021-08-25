---
description: O método CheckTargetRect determina se um retângulo de destino é válido.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Método CBaseControlVideo.CheckTargetRect (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8444764af729f9536471a6a9df221cc118edb7d043112eb0b5351f45982d87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057316"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a>Método CBaseControlVideo.CheckTargetRect

O `CheckTargetRect` método determina se um retângulo de destino é válido.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Ponteiro para o retângulo de destino a ser verificar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna E \_ INVALIDARG se não for válido; caso contrário, retorna NOERROR (S \_ OK).

## <a name="remarks"></a>Comentários

Essa função membro determina se o retângulo de destino solicitado é válido. Como o retângulo de destino especifica uma posição no cliente lógico da janela, as coordenadas podem ser negativas, embora a largura e a altura gerais não possam ser zero ou um valor negativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 





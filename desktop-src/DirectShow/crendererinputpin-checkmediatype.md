---
description: O método CheckMediaType determina se o pino aceita um tipo de mídia específico. Esse método substitui o método CBasePin::CheckMediaType.
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: Método CRendererInputPin.CheckMediaType (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d47f69c72ab2dab366b42d6dc80100508c0b1608d25abdcbfb1bb49c4177a278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687696"
---
# <a name="crendererinputpincheckmediatype-method"></a>Método CRendererInputPin.CheckMediaType

O `CheckMediaType` método determina se o pin aceita um tipo de mídia específico. Esse método substitui o [**método CBasePin::CheckMediaType.**](cbasepin-checkmediatype.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pgto* 
</dt> <dd>

Ponteiro para um objeto de tipo de mídia que contém o tipo de mídia proposto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 





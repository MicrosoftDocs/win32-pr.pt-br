---
description: O método CanSeekBackward determina se o fluxo pode ser buscado para trás. Esse método implementa o método IMediaPosition::CanSeekBackward.
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Método CPosPassThru.CanSeekBackward (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1d989acf074eb20e6ea3387c37129700320ce782e3c5d7c8bd4320641839ca1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108426"
---
# <a name="cpospassthrucanseekbackward-method"></a>Método CPosPassThru.CanSeekBackward

O `CanSeekBackward` método determina se o fluxo pode ser buscado para trás. Esse método implementa o [**método IMediaPosition::CanSeekBackward.**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCanSeekBackward* 
</dt> <dd>

Ponteiro para uma variável que recebe o valor OATRUE se o filtro puder buscar para trás ou OAFALSE caso contrário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o **valor HRESULT** do pino conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 





---
description: 'O método CanSeekBackward determina se o fluxo pode ser buscado retroativamente. Esse método implementa o método IMediaPosition:: CanSeekBackward.'
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Método CPosPassThru. CanSeekBackward (Ctlutil. h)
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
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775622"
---
# <a name="cpospassthrucanseekbackward-method"></a>Método CPosPassThru. CanSeekBackward

O `CanSeekBackward` método determina se o fluxo pode ser buscado retroativamente. Esse método implementa o método [**IMediaPosition:: CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) .

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

Ponteiro para uma variável que recebe o valor OATRUE se o filtro puder ser revertido ou OAFALSE caso contrário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor **HRESULT** do PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 





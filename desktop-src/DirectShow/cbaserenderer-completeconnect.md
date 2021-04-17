---
description: O método CompleteConnect conclui a conexão do pino de entrada com outro PIN.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Método CBaseRenderer. CompleteConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9d2d35f99a3b3b8dc5b668b8ee9a9f94f0a53dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751501"
---
# <a name="cbaserenderercompleteconnect-method"></a>Método CBaseRenderer. CompleteConnect

O `CompleteConnect` método conclui a conexão do pino de entrada com outro PIN.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O pino de entrada do filtro chama esse método de dentro de seu próprio `CompleteConnect` método, que é chamado para concluir uma conexão de PIN. (Para obter mais informações, consulte [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md).) O filtro chama o método [**CBaseRenderer:: SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) para habilitar os eventos [**\_ repaintes do EC**](ec-repaint.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





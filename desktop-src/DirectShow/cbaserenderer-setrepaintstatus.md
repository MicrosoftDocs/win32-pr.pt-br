---
description: O método SetRepaintStatus habilita ou desabilita os eventos redesenhados.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Método CBaseRenderer. SetRepaintStatus (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811747"
---
# <a name="cbaserenderersetrepaintstatus-method"></a>Método CBaseRenderer. SetRepaintStatus

O `SetRepaintStatus` método habilita ou desabilita os eventos redesenhados.

## <a name="syntax"></a>Sintaxe


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bRepaint* 
</dt> <dd>

Valor booliano que indica se os eventos redesenhados estão habilitados. Se **for true**, o filtro enviará eventos [**\_ Repaints do EC**](ec-repaint.md) para o Gerenciador do grafo de filtro. Caso contrário, ele não enviará \_ eventos de REdesenhos do EC.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método garante que o Gerenciador de gráficos de filtro não seja inundado com \_ eventos de REdesenhos de EC redundantes. Depois que o filtro envia um evento de [**\_ redesenho de EC**](ec-repaint.md) , ele chama esse método com o valor **true**. O filtro não envia mais eventos de \_ REdesenho de EC até receber mais dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





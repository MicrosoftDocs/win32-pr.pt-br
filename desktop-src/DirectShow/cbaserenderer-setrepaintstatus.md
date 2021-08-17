---
description: O método SetRepaintStatus habilita ou desabilita eventos de repaint.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Método CBaseRenderer.SetRepaintStatus (Renbase.h)
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
ms.openlocfilehash: 748d0091bd3d2eae11773a9f94b62ceeb92b2d3ca64049f1a1981e38bf222e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016844"
---
# <a name="cbaserenderersetrepaintstatus-method"></a>Método CBaseRenderer.SetRepaintStatus

O `SetRepaintStatus` método habilita ou desabilita eventos de repaint.

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

Valor booliano que indica se os eventos de repaint estão habilitados. Se **TRUE**, o filtro enviará [**eventos EC \_ REPAINT**](ec-repaint.md) para o gerenciador de grafo de filtro. Caso contrário, ele não enviará eventos \_ EC REPAINT.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método garante que o gerenciador de grafo de filtro não seja inundado com eventos \_ REPAINT de EC redundantes. Depois que o filtro envia [**um evento \_ EC REPAINT,**](ec-repaint.md) ele chama esse método com o valor **TRUE**. O filtro não envia mais eventos \_ EC REPAINT até receber mais dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 





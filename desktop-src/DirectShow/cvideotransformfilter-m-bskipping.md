---
description: Valor booliana que indica se o filtro está soltando quadros no momento. Se esse valor for TRUE, o filtro continuará a soltar quadros até atingir o próximo quadro-chave ou até receber 30 quadros delta em uma linha sem um quadro-chave.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: Membro CVideoTransformFilter::m_bSkipping (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f865bdc707b206a8528413a357a4e14bcfe88fff813e1f62a44d30e6f4843ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821911"
---
# <a name="cvideotransformfilterm_bskipping-member"></a>Membro CVideoTransformFilter::m \_ bSkipping

Valor booliana que indica se o filtro está soltando quadros no momento. Se esse valor for **TRUE,** o filtro continuará a soltar quadros até atingir o próximo quadro-chave ou até receber 30 quadros delta em uma linha sem um quadro-chave.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Vtrans.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 





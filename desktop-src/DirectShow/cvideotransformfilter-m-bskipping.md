---
description: Valor booliano que indica se o filtro está atualmente descartando quadros. Se esse valor for TRUE, o filtro continuará a descartar os quadros até atingir o próximo quadro-chave ou até receber 30 quadros Delta em uma linha sem um quadro-chave.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: 'Membro CVideoTransformFilter:: m_bSkipping (Vtrans. h)'
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
ms.openlocfilehash: 7beb4073052149e246a55ffbb1ff057e836704c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747580"
---
# <a name="cvideotransformfilterm_bskipping-member"></a>Membro de CVideoTransformFilter:: m \_ bSkipping

Valor booliano que indica se o filtro está atualmente descartando quadros. Se esse valor for **true**, o filtro continuará a descartar os quadros até atingir o próximo quadro-chave ou até receber 30 quadros Delta em uma linha sem um quadro-chave.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Vtrans. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 





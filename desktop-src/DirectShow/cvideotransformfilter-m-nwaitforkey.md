---
description: O número máximo atual de quadros Delta a serem descartados.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'Membro CVideoTransformFilter:: m_nWaitForKey (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757631"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a>Membro de CVideoTransformFilter:: m \_ nWaitForKey

O número máximo atual de quadros Delta a serem descartados. Embora essa variável seja maior que zero, o filtro removerá os quadros até atingir um quadro-chave. Para cada quadro descartado, o filtro decrementa essa variável por uma, o que impede que o filtro descarte um número excessivo de quadros. Depois de 30 quadros Delta em uma linha sem quadros-chave, o filtro começará a entregar quadros novamente.

## <a name="syntax"></a>Syntax


```C++
int m_nWaitForKey;
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

 

 





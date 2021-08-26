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
ms.openlocfilehash: 83cb78b233385e502d6508212492c54865aca28990ae079e4bf588776bd83fe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998536"
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
| parâmetro<br/>  | <dl> <dt>Vtrans. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 





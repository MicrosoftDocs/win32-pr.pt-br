---
description: Valor HRESULT que indica se o objeto aceitará amostras. Se o valor for S \_ OK, o objeto aceitará amostras. Caso contrário, ele rejeita amostras.
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'Membro COutputQueue:: m_hr (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749247"
---
# <a name="coutputqueuem_hr-member"></a>Membro de COutputQueue:: m \_ hr

Valor **HRESULT** que indica se o objeto aceitará amostras. Se o valor for S \_ OK, o objeto aceitará amostras. Caso contrário, ele rejeita amostras.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT m_hr;
```



## <a name="remarks"></a>Comentários

Essa variável de membro é usada para coordenar atividades entre threads. Se o pino de entrada downstream rejeitar um exemplo ou se o objeto começar a ser liberado, o valor será definido como S \_ false ou um código de erro. O objeto não fornecerá mais amostras até que a liberação seja concluída ou até que o método [**COutputQueue:: Reset**](coutputqueue-reset.md) seja chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 





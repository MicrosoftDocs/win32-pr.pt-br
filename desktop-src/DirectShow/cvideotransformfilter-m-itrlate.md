---
description: Indica o quão tarde os exemplos chegam ao renderizador, em unidades de tempo de referência. Sintaxe.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'Membro CVideoTransformFilter:: m_itrLate (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba2d14d19849768538184e54de5ca84b9495371783d57231ab9ad6aa7738718
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075946"
---
# <a name="cvideotransformfilterm_itrlate-member"></a>Membro de CVideoTransformFilter:: m \_ itrLate

Indica o quão tarde os exemplos chegam ao renderizador, em unidades de tempo de referência. Syntax

## <a name="syntax"></a>Sintaxe


```C++
int m_itrLate;
```



## <a name="remarks"></a>Comentários

Quando o filtro recebe uma mensagem de qualidade do downstream, ele armazena o valor de atraso nessa variável. Como o filtro descarta os quadros, ele atualiza esse valor subtraindo a duração de cada quadro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Vtrans. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 





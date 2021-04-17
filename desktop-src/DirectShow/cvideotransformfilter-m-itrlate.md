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
ms.openlocfilehash: a3ed93a4612d8fa5d4fe79239c6a7f4f5e479717
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748011"
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
| parâmetro<br/>  | <dl> <dt>Vtrans. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 





---
description: O \_ método Get Top recupera a coordenada da janela superior.
ms.assetid: 1e7910bd-e38e-4586-9dd6-701f69c0f6e7
title: Método de CBaseControlWindow.get_Top (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9861d930cdb2d93e5e0b73ffad625885c082cb6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747618"
---
# <a name="cbasecontrolwindowget_top-method"></a>CBaseControlWindow. obter o \_ método Top

O `get_Top` método recupera a coordenada da janela superior.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Top(
   long *pTop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTop* 
</dt> <dd>

Ponteiro para a coordenada superior, em pixels.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

A janela tem uma posição na área de trabalho. Isso é expresso em pixels por quatro coordenadas (esquerda, superior, direita e inferior). As interfaces automatizadas por OLE normalmente expressam essa posição por meio da esquerda, da parte superior, da largura e da altura; Essa é a convenção usada no DirectShow. Todas as coordenadas são expressas em pixels e a alteração de qualquer coordenada atualizará a janela imediatamente.

Definir as coordenadas esquerda ou superior move a janela para a esquerda ou para cima, respectivamente; essas coordenadas não têm efeito sobre a largura e a altura da janela. Da mesma forma, definir a largura e a altura não afeta as coordenadas esquerda e superior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 





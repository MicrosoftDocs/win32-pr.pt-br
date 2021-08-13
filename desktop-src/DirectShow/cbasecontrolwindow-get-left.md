---
description: O \_ método Get Left recupera a coordenada da janela esquerda atual.
ms.assetid: 9ee71bd3-1ff5-4574-8dcd-5ba6490d9785
title: Método de CBaseControlWindow.get_Left (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9317c1c061fe8528903bdd2e7129d0cfdc9e6dd67b9722841360d131e15cfb10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660519"
---
# <a name="cbasecontrolwindowget_left-method"></a>Método Left de CBaseControlWindow. get \_

O `get_Left` método recupera a coordenada da janela esquerda atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Left(
   long *pLeft
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pLeft* 
</dt> <dd>

Ponteiro para a coordenada esquerda, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

A janela tem uma posição na área de trabalho. Essa posição é expressa em pixels por quatro coordenadas (esquerda, superior, direita e inferior). As interfaces automatizadas por OLE normalmente expressam essa posição por meio da esquerda, da parte superior, da largura e da altura; Esta é a convenção usada em DirectShow. Todas as coordenadas são expressas em pixels e a alteração de qualquer coordenada atualizará a janela imediatamente.

Definir as coordenadas esquerda ou superior move a janela para a esquerda e para cima, respectivamente; essas coordenadas não têm efeito sobre a largura e a altura da janela. Da mesma forma, definir a largura e a altura não tem efeito nas coordenadas esquerda e superior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 





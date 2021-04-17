---
description: O \_ método obter largura recupera a largura da janela atual.
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: Método de CBaseControlWindow.get_Width (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56e863b8add52e1b98714e13466a48e3d0d52bba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755620"
---
# <a name="cbasecontrolwindowget_width-method"></a>Método de largura CBaseControlWindow. get \_

O `get_Width` método recupera a largura da janela atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Width(
   long *pWidth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWidth* 
</dt> <dd>

Ponteiro para a largura da janela, em pixels.

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

 

 





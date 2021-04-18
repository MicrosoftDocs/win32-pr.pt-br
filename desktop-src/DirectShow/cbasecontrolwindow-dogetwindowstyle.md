---
description: O método DoGetWindowStyle recupera os estilos de janela normais ou estendidos atuais.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Método CBaseControlWindow. DoGetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778648"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a>Método CBaseControlWindow. DoGetWindowStyle

O `DoGetWindowStyle` método recupera os estilos de janela normal ou estendida atuais.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStyle* 
</dt> <dd>

Ponteiro para uma variável que recebe as informações de estilo.

</dd> <dt>

*WindowLong* 
</dt> <dd>

Valor que especifica quais estilos recuperar. Deve ser uma destas opções:



|              |                                      |
|--------------|--------------------------------------|
| estilo de GWL \_   | Recupere os estilos de janela.          |
| GWL \_ FILEstyle | Recupere os estilos de janela estendida. |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro chama a função **GetWindowLong** do Win32 para recuperar o estilo da janela. Ele é chamado pelas funções membro [**CBaseControlWindow:: get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) e [**CBaseControlWindow:: get \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 





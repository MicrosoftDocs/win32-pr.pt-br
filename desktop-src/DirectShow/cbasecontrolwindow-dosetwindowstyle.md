---
description: O método DoSetWindowStyle altera os estilos de janela típicos ou estendidos.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Método CBaseControlWindow. DoSetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db88c5818d31d65f361ae1a805bd50c285d4a5c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909804"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a>Método CBaseControlWindow. DoSetWindowStyle

O `DoSetWindowStyle` método altera os estilos de janela típicos ou estendidos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Estilo* 
</dt> <dd>

Estilos de janela apropriados.

</dd> <dt>

*WindowLong* 
</dt> <dd>

Valor que especifica quais estilos definir. Deve ser uma destas opções:



| Label | Valor |
|--------------|--------------------------------------|
| estilo de GWL \_   | Recupere os estilos de janela.          |
| GWL \_ FILEstyle | Recupere os estilos de janela estendida. |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro chama a função **SetWindowLong** do Win32 para definir o estilo da janela e, em seguida, exibe novamente a janela na posição atual. Essa função de membro é chamada pelas funções de membro [**CBaseControlWindow::p UT \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) e [**CBaseControlWindow::p UT \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 





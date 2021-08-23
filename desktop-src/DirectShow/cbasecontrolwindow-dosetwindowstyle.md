---
description: O método DoSetWindowStyle altera os estilos de janela típicos ou estendidos.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Método CBaseControlWindow.DoSetWindowStyle (Ctlutil.h)
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
ms.openlocfilehash: d3b1f72ace792f13f88fbf0ce1e0edaf7b08789ecba88aede0b4094e9e75ae52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640876"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a>Método CBaseControlWindow.DoSetWindowStyle

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



| Rótulo | Valor |
|--------------|--------------------------------------|
| ESTILO \_ GWL   | Recupere os estilos de janela.          |
| GWL \_ EXSTYLE | Recupere os estilos de janela estendidos. |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro chama a função **Win32 SetWindowLong** para definir o estilo da janela e, em seguida, reprodução da janela na posição atual. Essa função membro é chamada pelas funções de membro [**CBaseControlWindow::p ut \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) e [**CBaseControlWindow::p ut \_ WindowStyleEx.**](cbasecontrolwindow-put-windowstyleex.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 





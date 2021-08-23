---
description: O método DoGetWindowStyle recupera os estilos de janela normais ou estendidos atuais.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Método CBaseControlWindow.DoGetWindowStyle (Ctlutil.h)
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
ms.openlocfilehash: 0fe158e4a17b898110a2555f87b469ee934aa791b6f0379f9054642810673389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793756"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a>Método CBaseControlWindow.DoGetWindowStyle

O `DoGetWindowStyle` método recupera os estilos de janela normais ou estendidos atuais.

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



| Rótulo | Valor |
|--------------|--------------------------------------|
| ESTILO \_ GWL   | Recupere os estilos de janela.          |
| GWL \_ EXSTYLE | Recupere os estilos de janela estendidos. |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

Essa função membro chama a função **Win32 GetWindowLong** para recuperar o estilo da janela. Ele é chamado pelas funções de membro [**CBaseControlWindow::get \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) e [**CBaseControlWindow::get \_ WindowStyleEx.**](cbasecontrolwindow-get-windowstyleex.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 





---
description: O \_ método Put WindowStyleEx define os estilos de janela estendidos.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: Método de CBaseControlWindow.put_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751277"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a>Método CBaseControlWindow. put \_ WindowStyleEx

O `put_WindowStyleEx` método define os estilos de janela estendidos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*WindowStyleEx* \[ no\]
</dt> <dd>

Valor que especifica o estilo da janela de controle.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna NOERROR.

## <a name="remarks"></a>Comentários

Esse método usa estilos de janela estendidos. Para obter uma lista completa de estilos de janela estendidos, consulte a função **CreateWindowEx** do Microsoft Win32. Para alterar o estilo da janela, recupere o estilo da janela atual e, em seguida, adicione ou remova os campos de bits necessários.

Não use os estilos de janela a seguir porque eles não são validados.

-   WS \_ desabilitado
-   WS \_ HSCROLL
-   WS \_ icônico
-   WS \_ maximize
-   \_minimizar WS
-   WS \_ VSCROLL

Com algumas exceções (anotadas aqui), os sinalizadores aceitáveis são os mesmos que os permitidos pela função **CreateWindow** do Win32.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 





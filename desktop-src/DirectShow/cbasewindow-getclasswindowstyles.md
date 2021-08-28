---
description: O método GetClassWindowStyles recupera estilos de classe e de janela da janela.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Método CBaseWindow.GetClassWindowStyles (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba7042069d4f1190a88b25ea4cc349e8230c149dd61d2d06fc91fa3439a9e55f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074621"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a>Método CBaseWindow.GetClassWindowStyles

O método recupera estilos de classe e estilos `GetClassWindowStyles` de janela da janela.

## <a name="syntax"></a>Sintaxe


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pClassStyles* 
</dt> <dd>

Ponteiro para uma variável que recebe os estilos de classe.

</dd> <dt>

*pWindowStyles* 
</dt> <dd>

Ponteiro para uma variável que recebe os estilos de janela.

</dd> <dt>

*pWindowStylesEx* 
</dt> <dd>

Ponteiro para uma variável que recebe os estilos de janela estendidos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna uma cadeia de caracteres de texto estático que contém o nome da classe.

## <a name="remarks"></a>Comentários

O [**método CBaseWindow::P repareWindow**](cbasewindow-preparewindow.md) chama esse método para recuperar estilos de classe e estilos de janela da janela.

Esse método é virtual puro; a classe derivada deve implementá-la. O exemplo a seguir mostra uma implementação possível:


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



O objeto usa o estilo de classe para o membro **lpszClassName** de uma estrutura WNDCLASS, que passa para a **função RegisterClass.** O objeto usa os estilos de janela para os parâmetros *dwExStyle* e *dwStyle* da **função CreateWindowEx.** Para obter mais informações, consulte o SDK da plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 





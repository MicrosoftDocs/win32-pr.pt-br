---
description: O método GetClassWindowStyles recupera estilos de classe e estilos de janela da janela.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Método CBaseWindow. GetClassWindowStyles (Winutil. h)
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
ms.openlocfilehash: a34332f84a91ee88d61ee5f29f0b6a0b0cc44714
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758700"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a>Método CBaseWindow. GetClassWindowStyles

O `GetClassWindowStyles` método recupera estilos de classe e estilos de janela da janela.

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

Ponteiro para uma variável que recebe os estilos de janela estendida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna uma cadeia de texto estática que contém o nome da classe.

## <a name="remarks"></a>Comentários

O método [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) chama esse método para recuperar os estilos de classe da janela e os estilos de janela.

Este método é virtual puro; a classe derivada deve implementá-la. O exemplo a seguir mostra uma possível implementação:


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



O objeto usa o estilo de classe para o membro **lpszClassName** de uma estrutura WNDCLASS, que ele passa para a função **registerClass** . O objeto usa os estilos de janela para os parâmetros *dwExStyle* e *DwStyle* da função **CreateWindowEx** . Para obter mais informações, consulte o SDK da plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 





---
description: O \_ método Put WindowStyle define os estilos de janela padrão.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: Método de CBaseControlWindow.put_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750684"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a>CBaseControlWindow. put o \_ método WindowStyle

O `put_WindowStyle` método define os estilos de janela padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*WindowStyle* 
</dt> <dd>

Novos estilos de janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Tome cuidado ao alterar os estilos de janela. Na maioria dos casos, um aplicativo deve recuperar o estilo atual e, em seguida, adicionar ou remover os bits inadequados. Esse procedimento permite que vários estilos de janela internos usados pelo Windows permaneçam intactos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 





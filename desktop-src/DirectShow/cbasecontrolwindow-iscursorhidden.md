---
description: O método IsCursorHidden recupera o estado atual do membro de \_ dados m bCursorHidden.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Método CBaseControlWindow. IsCursorHidden (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752307"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a>Método CBaseControlWindow. IsCursorHidden

O `IsCursorHidden` método recupera o estado atual do membro de dados **m \_ bCursorHidden** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CursorHidden* 
</dt> <dd>

Ponteiro para o valor de **m \_ bCursorHidden**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Quando chamado sem um parâmetro, retorna OATRUE se o cursor estiver oculto ou OAFALSE se o cursor estiver visível.

## <a name="remarks"></a>Comentários

Os objetos internos devem chamar essa função de membro sem o parâmetro *CursorHidden* para evitar o bloqueio da seção crítica. Os objetos externos acessam essa função de membro com o parâmetro *CursorHidden* por meio do método [**IVideoWindow:: IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 





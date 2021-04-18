---
description: Método de construtor.
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Construtor CBaseWindow. CBaseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1741f8596210afac676a7e81f57b46e18fbba9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748633"
---
# <a name="cbasewindowcbasewindow-constructor"></a>Construtor CBaseWindow. CBaseWindow

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bDoGetDC* 
</dt> <dd>

Valor booliano que especifica se o contexto do dispositivo deve ser recuperado.

</dd> <dt>

*bPostToDestroy* 
</dt> <dd>

Valor booliano que especifica a variável de membro [**CBaseWindow:: m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Depois de criar o objeto, chame o método [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) para criar a janela. **PrepareWindow** é um método virtual. Ele chama [**CBaseWindow:: InitialiseWindow**](cbasewindow-initialisewindow.md), também um método virtual. Esses métodos são separados do construtor para que as classes derivadas possam substituí-los, se necessário.

Se o valor do parâmetro *bDoGetDC* for **true**, o `CBaseWindow` objeto recuperará um identificador para o DC (contexto de dispositivo) da janela e o armazenará na variável de membro [**\_ HDC CBaseWindow:: m**](cbasewindow-m-hdc.md) . O objeto também cria um controlador de domínio de memória compatível, que ele armazena na variável de membro [**CBaseWindow:: m \_ MemoryDC**](cbasewindow-m-memorydc.md) . Essas ações ocorrem no método **InitialiseWindow** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 





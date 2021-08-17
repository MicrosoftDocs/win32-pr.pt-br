---
description: Construtor de CBaseWindow. CBaseWindow-método de construtor.
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
ms.openlocfilehash: d8873ee896d910d1596138a8d116c93ae0190534bac48b6ceb19165074f07b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016744"
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
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 





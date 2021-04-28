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
ms.openlocfilehash: 05205750810294076bf005d0e5b73fda6b2143d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095814"
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 





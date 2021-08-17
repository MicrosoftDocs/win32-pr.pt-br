---
description: Ocorre quando um usuário clica no controle InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: Evento InkEdit. Click (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f126035319c5d225da3fe57e075044c50f91f928277de89fce8e516e4723c701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718134"
---
# <a name="inkeditclick-event"></a>Evento InkEdit. Click

Ocorre quando um usuário clica no controle [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Sintaxe


```C++
void Click();
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Clicar em um controle gera eventos [**MouseDown**](inkedit-mousedown.md) e [**MouseUp**](inkedit-mouseup.md) além do evento de clique.

> [!Note]  
> Para distinguir entre os botões esquerdo, direito e do meio do mouse, use os eventos [**MouseDown**](inkedit-mousedown.md) e [**MouseUp**](inkedit-mouseup.md) .

 

Se houver código no evento de **clique** , o evento [**DblClick**](inkedit-dblclick.md) nunca será disparado, pois o evento de **clique** é o primeiro evento a ser disparado entre os dois. Como resultado, o clique do mouse é interceptado pelo evento de **clique** , portanto, o evento **DblClick** não ocorre.

Esse método de evento é definido na interface **\_ IInkEditEvents** . A interface **\_ IInkEditEvents** implementa a interface IDispatch com um identificador de **\_ IeeClick DISPID**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Inked. h (também requer Inked \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 





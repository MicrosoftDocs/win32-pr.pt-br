---
description: Ocorre quando um usuário clica no controle InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: Evento InkEdit. Click (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784178"
---
# <a name="inkeditclick-event"></a>Evento InkEdit. Click

Ocorre quando um usuário clica no controle [InkEdit](inkedit-control-reference.md) .

## <a name="syntax"></a>Sintaxe


```C++
void Click();
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Retornar valor

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
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Inked. h (também requer Inked \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 





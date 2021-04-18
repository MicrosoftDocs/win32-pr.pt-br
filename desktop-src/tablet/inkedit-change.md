---
description: Ocorre quando o conteúdo do controle InkEdit é alterado.
ms.assetid: 6c65fcca-c84a-414c-a4e5-c5fdffb13e51
title: Evento InkEdit. Change (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ad11ef335a397070001f1ae6be785d60fe9cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796137"
---
# <a name="inkeditchange-event"></a>Evento InkEdit. Change

Ocorre quando o conteúdo do controle [InkEdit](inkedit-control-reference.md) é alterado.

## <a name="syntax"></a>Sintaxe


```C++
void Change();
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse evento ocorre sempre que qualquer propriedade que afete o conteúdo da alteração do controle [InkEdit](inkedit-control-reference.md) .

Esse método de evento é definido na interface **\_ IInkEditEvents** . A interface **\_ IInkEditEvents** implementa a interface IDispatch com um identificador de **\_ IeeChange DISPID**.

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

 

 





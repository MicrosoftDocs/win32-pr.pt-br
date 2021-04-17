---
description: Ocorre quando a seleção atual de texto no controle InkEdit é alterada ou o ponto de inserção foi movido.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Evento InkEdit. SelChange (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748697"
---
# <a name="inkeditselchange-event"></a>Evento InkEdit. SelChange

Ocorre quando a seleção atual de texto no controle [InkEdit](inkedit-control-reference.md) é alterada ou o ponto de inserção foi movido.

## <a name="syntax"></a>Sintaxe


```C++
void SelChange();
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Você pode usar o evento **SelChange** para verificar as várias propriedades que fornecem informações sobre a seleção atual (como [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) para que você possa atualizar botões em uma barra de ferramentas, por exemplo.

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

 

 





---
description: Ocorre quando a seleção atual de texto no controle InkEdit foi alterada ou o ponto de inserção foi movido.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Evento InkEdit.SelChange (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9677aafa254de3d834e9b947ad1b858b893d6a42e53336dd11ad5c54157c13dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712645"
---
# <a name="inkeditselchange-event"></a>Evento InkEdit.SelChange

Ocorre quando a seleção atual de texto no controle [InkEdit](inkedit-control-reference.md) foi alterada ou o ponto de inserção foi movido.

## <a name="syntax"></a>Sintaxe


```C++
void SelChange();
```



## <a name="parameters"></a>Parâmetros

Esse evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Você pode usar o evento **SelChange** para verificar as várias propriedades que dão informações sobre a seleção atual (como [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) para que você possa atualizar botões em uma barra de ferramentas, por exemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Inked.h (também requer \_ i.c com tinta)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> </dl>

 

 





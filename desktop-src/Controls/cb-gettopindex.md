---
title: CB_GETTOPINDEX mensagem (Winuser.h)
description: Um aplicativo envia a mensagem CB GETTOPINDEX para recuperar o índice baseado em zero do primeiro item visível na parte da caixa de listagem de \_ uma caixa de combinação.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- CB_GETTOPINDEX controles de Windows mensagem
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2360b07c86d6d5bcbb8296d705e8ef65b3a81481a8fc647a362aedc729f38b42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089106"
---
# <a name="cb_gettopindex-message"></a>Mensagem \_ CB GETTOPINDEX

Um aplicativo envia a **mensagem CB \_ GETTOPINDEX** para recuperar o índice baseado em zero do primeiro item visível na parte da caixa de listagem de uma caixa de combinação. Inicialmente, o item com índice 0 está na parte superior da caixa de listagem, mas se o conteúdo da caixa de listagem tiver sido rolado, outro item poderá estar na parte superior.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, o valor de retorno será o índice do primeiro item visível na caixa de listagem da caixa de combinação.

Se a mensagem falhar, o valor de retorno será CB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CB \_ SDICEPINDEX**](cb-settopindex.md)
</dt> </dl>

 

 






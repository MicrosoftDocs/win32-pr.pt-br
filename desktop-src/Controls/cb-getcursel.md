---
title: Mensagem de CB_GETCURSEL (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de IScursel de CB para recuperar o índice do item atualmente selecionado, se houver, na caixa de listagem de uma caixa de combinação.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- Controles de CB_GETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fbc9aa1785738fb061696fbad64598747168269
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824871"
---
# <a name="cb_getcursel-message"></a>\_Mensagem de ISCURSE CB

Um aplicativo envia uma mensagem de **\_ iscursel de CB** para recuperar o índice do item atualmente selecionado, se houver, na caixa de listagem de uma caixa de combinação.

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

## <a name="return-value"></a>Retornar valor

O valor de retorno é o índice de base zero do item selecionado no momento. Se nenhum item for selecionado, será CB \_ Err.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**seleção do CB \_**](cb-selectstring.md)
</dt> <dt>

[**CB \_ SETcurseal**](cb-setcursel.md)
</dt> </dl>

 

 






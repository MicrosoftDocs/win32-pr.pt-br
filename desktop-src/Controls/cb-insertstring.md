---
title: Mensagem de CB_INSERTSTRING (WinUser. h)
description: Insere uma cadeia de caracteres ou dados de item na lista de uma caixa de combinação. Ao contrário da \_ mensagem de ADDSTRING CB, a mensagem de inserção de CB não faz com \_ que uma lista com o \_ estilo de classificação CBS seja classificada.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- Controles de CB_INSERTSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455124"
---
# <a name="cb_insertstring-message"></a>Mensagem de inserção de CB \_

Insere uma cadeia de caracteres ou dados de item na lista de uma caixa de combinação. Ao contrário da mensagem de [**\_ AddString CB**](cb-addstring.md) , a mensagem de **\_ inserção de CB** não faz com que uma lista com o estilo de [**\_ classificação CBS**](combo-box-styles.md) seja classificada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero da posição na qual inserir a cadeia de caracteres. Se esse parâmetro for-1, a cadeia de caracteres será adicionada ao final da lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo a ser inserida. Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o valor do parâmetro *lParam* será armazenado em vez da cadeia de caracteres para a qual ele apontaria de outra forma.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o índice da posição na qual a cadeia de caracteres foi inserida. Se ocorrer um erro, o valor de retorno será CB \_ Err. Se não houver espaço suficiente disponível para armazenar a nova cadeia de caracteres, ela será CB \_ ERRSPACE.

Se a caixa de combinação tiver o estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e você inserir uma cadeia de caracteres maior que a caixa de combinação, deverá enviar uma mensagem [**\_ SETHORIZONTALEXTENT de lb**](lb-sethorizontalextent.md) para garantir que a barra de rolagem horizontal seja exibida.

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

[**AddString CB \_**](cb-addstring.md)
</dt> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> <dt>

[**\_pasta CB**](cb-dir.md)
</dt> </dl>

 


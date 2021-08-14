---
title: Mensagem de WM_CUT (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de recorte do WM para um controle de edição ou caixa de combinação para excluir (recortar) a seleção atual, se houver, no controle de edição e copiar o texto excluído para a área de transferência no \_ formato de texto cf.
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- WM_CUT Exchange de dados da mensagem
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d117e0a942c0d9e24e1a9c40d3d66e605ab8d5cf26bbad0e287e9b03a9b25780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304482"
---
# <a name="wm_cut-message"></a>\_Mensagem de recorte do WM

Um aplicativo envia uma mensagem de **\_ recorte do WM** para um controle de edição ou caixa de combinação para excluir (recortar) a seleção atual, se houver, no controle de edição e copiar o texto excluído para a área de transferência no formato de [**\_ texto CF**](standard-clipboard-formats.md) .


```C++
#define WM_CUT                          0x0300
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

A exclusão realizada pela mensagem **de \_ recorte do WM** pode ser desfeita enviando o controle de edição uma mensagem em [**\_ desfazer**](../controls/em-undo.md) .

Para excluir a seleção atual sem colocar o texto excluído na área de transferência, use a mensagem de [**\_ limpeza do WM**](wm-clear.md) .

Quando enviado para uma caixa de combinação, a mensagem de **\_ recorte do WM** é tratada por seu controle de edição. Esta mensagem não tem nenhum efeito quando enviada para uma caixa de combinação com o estilo de [**CBS \_**](../controls/combo-box-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**limpeza do WM \_**](wm-clear.md)
</dt> <dt>

[**cópia do WM \_**](wm-copy.md)
</dt> <dt>

[**colar do WM \_**](wm-paste.md)
</dt> <dt>

[**desfazer o WM \_**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**em \_ desfazer**](../controls/em-undo.md)
</dt> </dl>

 


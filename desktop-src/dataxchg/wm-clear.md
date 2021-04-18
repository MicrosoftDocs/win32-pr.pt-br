---
title: Mensagem de WM_CLEAR (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de limpeza do WM para um controle de edição ou caixa de combinação para excluir (limpar) a seleção atual, se houver, do controle de edição.
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- Troca de dados de mensagem WM_CLEAR
topic_type:
- apiref
api_name:
- WM_CLEAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a8e325704d1e8b953fe59bfaf4e8fcee62cf40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789241"
---
# <a name="wm_clear-message"></a>Mensagem de limpeza do WM \_

Um aplicativo envia uma mensagem de **\_ limpeza do WM** para um controle de edição ou caixa de combinação para excluir (limpar) a seleção atual, se houver, do controle de edição.


```C++
#define WM_CLEAR                        0x0303
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

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

A exclusão executada pela mensagem **de \_ limpeza do WM** pode ser desfeita enviando o controle de edição uma mensagem em [**\_ desfazer**](../controls/em-undo.md) .

Para excluir a seleção atual e inserir o conteúdo excluído na área de transferência, use a mensagem de [**\_ recorte do WM**](wm-cut.md) .

Quando enviado para uma caixa de combinação, a mensagem de **\_ limpeza do WM** é manipulada por seu controle de edição. Esta mensagem não tem nenhum efeito quando enviada para uma caixa de combinação com o estilo de [**CBS \_**](../controls/combo-box-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**cópia do WM \_**](wm-copy.md)
</dt> <dt>

[**recorte do WM \_**](wm-cut.md)
</dt> <dt>

[**colar do WM \_**](wm-paste.md)
</dt> <dt>

[**desfazer o WM \_**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> </dl>

 


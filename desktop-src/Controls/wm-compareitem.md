---
title: Mensagem de WM_COMPAREITEM (WinUser. h)
description: Enviado para determinar a posição relativa de um novo item na lista classificada de uma caixa de combinação ou caixa de listagem desenhada pelo proprietário.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- Controles de WM_COMPAREITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454612"
---
# <a name="wm_compareitem-message"></a>Mensagem do WM \_ COMPAREITEM

Enviado para determinar a posição relativa de um novo item na lista classificada de uma caixa de combinação ou caixa de listagem desenhada pelo proprietário. Sempre que o aplicativo adiciona um novo item, o sistema envia essa mensagem ao proprietário de uma caixa de combinação ou caixa de listagem criada com o estilo [**de \_ classificação**](list-box-styles.md) [**CBS \_**](combo-box-styles.md) ou lbs.


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o identificador do controle que enviou a mensagem **de \_ COMPAREITEM do WM** .

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) que contém os identificadores e os dados fornecidos pelo aplicativo para dois itens na caixa de combinação ou de listagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno indica a posição relativa dos dois itens. Pode ser qualquer um dos valores mostrados na tabela a seguir.



| Código de retorno                                                                          | Descrição                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**Valor**</dt> </dl> | Significado<br/>                                           |
| <dl> <dt>**-1**</dt> </dl>    | O item 1 precede o item 2 na ordem classificada.<br/>       |
| <dl> <dt>**0**</dt> </dl>     | Os itens 1 e 2 são equivalentes na ordem classificada.<br/> |
| <dl> <dt>**1**</dt> </dl>     | O item 1 segue o item 2 na ordem classificada.<br/>        |



 

## <a name="remarks"></a>Comentários

Quando o proprietário de uma caixa de combinação ou caixa de listagem desenhada pelo proprietário recebe essa mensagem, o proprietário retorna um valor que indica qual dos itens especificados pela estrutura [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) aparecerá antes do outro. Normalmente, o sistema envia essa mensagem várias vezes até determinar a posição exata para o novo item.

Se um procedimento da caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado em um **bool** e retornar o valor diretamente. O \_ valor de MSGRESULT DWL definido pela [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

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

[**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 


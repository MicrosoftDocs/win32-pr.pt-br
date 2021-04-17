---
title: Mensagem de WM_PASTE (WinUser. h)
description: Um aplicativo envia uma mensagem de colagem do WM \_ para um controle de edição ou caixa de combinação para copiar o conteúdo atual da área de transferência para o controle de edição na posição atual do cursor. Os dados só serão inseridos se a área de transferência contiver dados no formato de texto do CF \_ .
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- Troca de dados de mensagem WM_PASTE
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369834"
---
# <a name="wm_paste-message"></a>Mensagem de colagem do WM \_

Um aplicativo envia uma mensagem de **\_ colagem do WM** para um controle de edição ou caixa de combinação para copiar o conteúdo atual da área de transferência para o controle de edição na posição atual do cursor. Os dados só serão inseridos se a área de transferência contiver dados no formato de [**\_ texto do CF**](standard-clipboard-formats.md) .


```C++
#define WM_PASTE                        0x0302
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

Quando enviado para uma caixa de combinação, a mensagem de **\_ colagem do WM** é tratada por seu controle de edição. Esta mensagem não tem nenhum efeito quando enviada para uma caixa de combinação com o estilo de [**CBS \_**](../controls/combo-box-styles.md) .

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

[**limpeza do WM \_**](wm-clear.md)
</dt> <dt>

[**cópia do WM \_**](wm-copy.md)
</dt> <dt>

[**recorte do WM \_**](wm-cut.md)
</dt> <dt>

[**desfazer o WM \_**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> </dl>

 


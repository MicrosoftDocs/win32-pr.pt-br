---
title: Mensagem de WM_COPY (WinUser. h)
description: Um aplicativo envia a mensagem de cópia do WM \_ para um controle de edição ou caixa de combinação para copiar a seleção atual para a área de transferência no formato de texto do CF \_ .
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- Troca de dados de mensagem WM_COPY
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "105773004"
---
# <a name="wm_copy-message"></a>Mensagem de cópia do WM \_

Um aplicativo envia a mensagem de **\_ cópia do WM** para um controle de edição ou caixa de combinação para copiar a seleção atual para a área de transferência no formato de [**\_ texto do CF**](standard-clipboard-formats.md) .


```C++
#define WM_COPY                         0x0301
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

Retorna um valor diferente de zero em caso de êxito, mais zero.

## <a name="remarks"></a>Comentários

Quando enviado para uma caixa de combinação, a mensagem de **\_ cópia do WM** é manipulada por seu controle de edição. Esta mensagem não tem nenhum efeito quando enviada para uma caixa de combinação com o estilo de [**CBS \_**](../controls/combo-box-styles.md) .

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

 


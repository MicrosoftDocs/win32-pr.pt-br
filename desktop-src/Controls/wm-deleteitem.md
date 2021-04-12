---
title: Mensagem de WM_DELETEITEM (WinUser. h)
description: Enviado ao proprietário de uma caixa de listagem ou caixa de combinação quando a caixa de listagem ou a caixa de combinação é destruída ou quando os itens são removidos pela \_ mensagem lb DeleteString, lb \_ RESETCONTENT, CB \_ excluirstring ou CB \_ RESETCONTENT.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- Controles de WM_DELETEITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455065"
---
# <a name="wm_deleteitem-message"></a>Mensagem do WM \_ DELETEITEM

Enviado ao proprietário de uma caixa de listagem ou caixa de combinação quando a caixa de listagem ou a caixa de combinação é destruída ou quando os itens são removidos pela mensagem [**lb \_ DeleteString**](lb-deletestring.md), [**lb \_ RESETCONTENT**](lb-resetcontent.md), [**CB \_ excluirstring**](cb-deletestring.md)ou [**CB \_ RESETCONTENT**](cb-resetcontent.md) . O sistema envia uma mensagem do **WM \_ DELETEITEM** para cada item excluído. O sistema envia a mensagem do **WM \_ DELETEITEM** para qualquer caixa de listagem ou item de caixa de combinação excluído com dados de item diferente de zero.


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o identificador do controle que enviou a mensagem **de \_ DELETEITEM do WM** .

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) que contém informações sobre o item excluído de uma caixa de listagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar **true** se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Microsoft Windows NT e posterior: o Windows envia uma mensagem do **WM \_ DELETEITEM** somente para itens excluídos de uma caixa de listagem desenhada pelo proprietário (com o estilo [**lbs \_ OwnerDrawFixed**](list-box-styles.md) ou [**lbs \_ OwnerDrawVariable**](list-box-styles.md) ) ou a caixa de combinação desenhada pelo proprietário (com o estilo [**CBS \_ OwnerDrawFixed**](combo-box-styles.md) ou [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) ).

Windows 95: o Windows envia a mensagem do **WM \_ DELETEITEM** para qualquer caixa de listagem ou item de caixa de combinação excluído com dados de item diferente de zero.

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

[**excluído de CB \_**](cb-deletestring.md)
</dt> <dt>

[**\_RESETCONTENT CB**](cb-resetcontent.md)
</dt> <dt>

[**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[**LB \_ DeleteString**](lb-deletestring.md)
</dt> <dt>

[**\_RESETCONTENT lb**](lb-resetcontent.md)
</dt> </dl>

 

 






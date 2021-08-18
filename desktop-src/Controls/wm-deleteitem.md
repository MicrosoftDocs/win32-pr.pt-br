---
title: WM_DELETEITEM mensagem (Winuser.h)
description: Enviado ao proprietário de uma caixa de listagem ou caixa de combinação quando a caixa de listagem ou caixa de combinação é destruída ou quando os itens são removidos pela mensagem LB \_ DELETESTRING, LB \_ RESETCONTENT, CB \_ DELETESTRING ou CB \_ RESETCONTENT.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- WM_DELETEITEM controles Windows mensagem
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
ms.openlocfilehash: 1f461b63d751822d9a4c602993314bf0677cff754881269ab44458ab17f3a439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018534"
---
# <a name="wm_deleteitem-message"></a>Mensagem WM \_ DELETEITEM

Enviado ao proprietário de uma caixa de listagem ou caixa de combinação quando a caixa de listagem ou caixa de combinação é destruída ou quando os itens são removidos pela mensagem [**LB \_ DELETESTRING,**](lb-deletestring.md) [**LB \_ RESETCONTENT,**](lb-resetcontent.md) [**CB \_ DELETESTRING**](cb-deletestring.md)ou [**CB \_ RESETCONTENT.**](cb-resetcontent.md) O sistema envia uma **mensagem WM \_ DELETEITEM** para cada item excluído. O sistema envia a **mensagem WM \_ DELETEITEM** para qualquer caixa de listagem excluída ou item de caixa de combinação com dados de item que não são zero.


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o identificador do controle que enviou a mensagem **WM \_ DELETEITEM.**

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) que contém informações sobre o item excluído de uma caixa de listagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deverá retornar **TRUE** se ele processa essa mensagem.

## <a name="remarks"></a>Comentários

Microsoft Windows NT e posterior: o Windows envia uma mensagem **WM \_ DELETEITEM** somente para itens excluídos de uma caixa de listagem desenhada pelo proprietário (com o estilo PROPRIETÁRIO DO [**\_ LBSDRAWFIXED**](list-box-styles.md) ou [**LBS \_ OWNERDRAWVARIABLE)**](list-box-styles.md) ou caixa de combinação desenhada pelo proprietário (com o estilo [**\_ OWNERDRAWFIXED**](combo-box-styles.md) ou [**CBS \_ OWNERDRAWVARIABLE).**](combo-box-styles.md)

Windows 95: Windows envia a mensagem **WM \_ DELETEITEM** para qualquer caixa de listagem excluída ou item de caixa de combinação com dados de item não zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CB \_ DELETESTRING**](cb-deletestring.md)
</dt> <dt>

[**CB \_ RESETCONTENT**](cb-resetcontent.md)
</dt> <dt>

[**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[**LB \_ DELETESTRING**](lb-deletestring.md)
</dt> <dt>

[**LB \_ RESETCONTENT**](lb-resetcontent.md)
</dt> </dl>

 

 






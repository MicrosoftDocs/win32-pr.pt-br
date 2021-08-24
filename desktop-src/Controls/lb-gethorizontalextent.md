---
title: LB_GETHORIZONTALEXTENT mensagem (Winuser.h)
description: Obtém a largura, em pixels, que uma caixa de listagem pode ser rolada horizontalmente (a largura rolável) se a caixa de listagem tiver uma barra de rolagem horizontal.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- LB_GETHORIZONTALEXTENT controles de Windows mensagem
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f754b62ad0f51a236662fdfba2304221d58e1288e2756c0330343c63a0699e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799506"
---
# <a name="lb_gethorizontalextent-message"></a>Mensagem \_ LB GETHORIZONTALEXTENT

Obtém a largura, em pixels, que uma caixa de listagem pode ser rolada horizontalmente (a largura rolável) se a caixa de listagem tiver uma barra de rolagem horizontal.

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

O valor de retorno é a largura rolável, em pixels, da caixa de listagem.

## <a name="remarks"></a>Comentários

Para responder à **mensagem \_ LB GETHORIZONTALEXTENT,** a caixa de listagem deve ter sido definida com o [**estilo \_ HSCROLL do WS.**](/windows/desktop/winmsg/window-styles)

Se o aplicativo não definir a extensão horizontal da caixa de listagem (usando [**LB \_ LB LBORIZONTALEXTENT),**](lb-sethorizontalextent.md)a extensão horizontal padrão será zero. Observe que a caixa de listagem não atualiza sua extensão horizontal dinamicamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LB \_ LB LBORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> </dl>

 


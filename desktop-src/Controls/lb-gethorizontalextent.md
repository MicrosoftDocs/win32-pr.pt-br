---
title: Mensagem de LB_GETHORIZONTALEXTENT (WinUser. h)
description: Obtém a largura, em pixels, que uma caixa de listagem pode ser rolada horizontalmente (a largura rolável) se a caixa de listagem tiver uma barra de rolagem horizontal.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- Controles de LB_GETHORIZONTALEXTENT de mensagens do Windows
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
ms.openlocfilehash: bf10f4f216e0c00fba256c1373fb9aae4f2a4ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919087"
---
# <a name="lb_gethorizontalextent-message"></a>GETHORIZONTALEXTENT de mensagens de LB \_

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

## <a name="return-value"></a>Retornar valor

O valor de retorno é a largura rolável, em pixels, da caixa de listagem.

## <a name="remarks"></a>Comentários

Para responder à mensagem **\_ GETHORIZONTALEXTENT de lb** , a caixa de listagem deve ter sido definida com o estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .

Se o aplicativo não definir a extensão horizontal da caixa de listagem (usando [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)), a extensão horizontal padrão será zero. Observe que a caixa de listagem não atualiza sua extensão horizontal dinamicamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> </dl>

 


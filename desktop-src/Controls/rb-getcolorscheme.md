---
title: Mensagem de RB_GETCOLORSCHEME (commctrl. h)
description: Recupera as informações do esquema de cores do controle rebar.
ms.assetid: 01f81c4b-bbc9-43ae-a1f5-1e289c6fa278
keywords:
- controles de Windows de mensagem de RB_GETCOLORSCHEME
topic_type:
- apiref
api_name:
- RB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918b46d1077c0074584be2d609d486097cc2e40f7a5c62a03db914fce58e320
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169616"
---
# <a name="rb_getcolorscheme-message"></a>\_Mensagem GETCOLORSCHEME RB

Recupera as informações do esquema de cores do controle rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que receberá as informações do esquema de cores. Você deve definir o membro **dwSize** dessa estrutura como **sizeof**(ColorScheme) antes de enviar esta mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETCOLORSCHEME RB**](rb-setcolorscheme.md)
</dt> </dl>

 

 






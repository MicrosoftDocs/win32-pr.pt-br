---
title: Mensagem de TB_SETWINDOWTHEME (commctrl. h)
description: Define o estilo visual de um controle ToolBar.
ms.assetid: 8b05c561-af66-47e7-8ef3-7f9f81da4840
keywords:
- controles de Windows de mensagem de TB_SETWINDOWTHEME
topic_type:
- apiref
api_name:
- TB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1f3f4ae5f6e7a3a05670a8ba9bfe533156e1ef3e6043ff2a039744da705da39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078120"
---
# <a name="tb_setwindowtheme-message"></a>TB de \_ mensagem SETWINDOWTHEME

Define o estilo visual de um controle ToolBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode que contém o estilo visual da barra de ferramentas a ser definido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

O envio dessa mensagem é equivalente a chamar [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) na barra de ferramentas e seu controle ToolTip, se houver.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






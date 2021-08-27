---
description: Instrui uma janela de remoção de imagem para atualizar usando as novas informações de DROPDESCRIPTION.
title: DDWM_UPDATEWINDOW mensagem
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a17e015d6dff2ae5133f3ce8245c5ead3c3381f8eb5c48e74946fdf9bcb46ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032834"
---
# <a name="ddwm_updatewindow-message"></a>\_Mensagem DDWM UPDATEWINDOW

Instrui uma janela de remoção de imagem para atualizar usando as novas informações de [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Não usado.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

DDWM \_ UPDATEWINDOW é definido como usuário do WM \_ + 3.

Quando o estado de uma operação de remoção é alterado, como em resposta a uma tecla modificadora,[**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) retorna um novo valor [**DROPEFFECT**](../com/dropeffect-constants.md) (esse valor **DROPEFFECT** também pode ser recebido por meio de [**IDropSource:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)). Em resposta, o aplicativo atualiza a estrutura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) da interface "soltar" com um novo valor [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) que indica a decoração a ser aplicada ao Visual da janela de arrastar; por exemplo, uma indicação de que o arquivo está sendo copiado em vez de movido ou que o objeto não pode ser Descartado para esse local. No entanto, os visuais não são atualizados até que o objeto receba uma mensagem **DDWM \_ UPDATEWINDOW** .

O formato de área de transferência [DragWindow](clipboard.md) fornece o **HWND** da janela de arrastar destinatário para o remetente da mensagem **DDWM \_ UPDATEWINDOW** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 

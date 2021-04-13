---
title: Mensagem de TVM_ENDEDITLABELNOW (commctrl. h)
description: Finaliza a edição de um rótulo de item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ EndEditLabelNow.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- Controles de TVM_ENDEDITLABELNOW de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499311"
---
# <a name="tvm_endeditlabelnow-message"></a>\_Mensagem TVM ENDEDITLABELNOW

Finaliza a edição de um rótulo de item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Variável que indica se a edição é cancelada sem ser salva no rótulo. Se esse parâmetro for **true**, o sistema cancelará a edição sem salvar as alterações. Caso contrário, o sistema salvará as alterações no rótulo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Essa mensagem faz com que o código de notificação [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) seja enviado para a janela pai do controle de exibição de árvore.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






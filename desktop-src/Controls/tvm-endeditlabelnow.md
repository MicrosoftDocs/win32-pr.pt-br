---
title: TVM_ENDEDITLABELNOW mensagem (Commctrl.h)
description: Encerra a edição do rótulo de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ EndEditLabelNow.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- TVM_ENDEDITLABELNOW controles de Windows mensagem
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
ms.openlocfilehash: 18355edc8efb18ea56a39e60c68361a7ef8d72e39af644707d6d102738fd60c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119387256"
---
# <a name="tvm_endeditlabelnow-message"></a>Mensagem TVM \_ ENDEDITLABELNOW

Encerra a edição do rótulo de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ EndEditLabelNow.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Variável que indica se a edição é cancelada sem ser salva no rótulo. Se esse parâmetro for **TRUE,** o sistema cancelará a edição sem salvar as alterações. Caso contrário, o sistema salvará as alterações no rótulo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

Essa mensagem faz com que o código de notificação [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) seja enviado para a janela pai do controle de exibição de árvore.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






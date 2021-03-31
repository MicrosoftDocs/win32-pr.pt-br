---
title: Mensagem de TVM_SETITEMHEIGHT (commctrl. h)
description: Define a altura dos itens de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetItemHeight.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- Controles de TVM_SETITEMHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114769f689cbf8d9475460e40d205c4282a1a787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918611"
---
# <a name="tvm_setitemheight-message"></a>\_Mensagem TVM SETITEMHEIGHT

Define a altura dos itens de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Nova altura de cada item no modo de exibição de árvore, em pixels. As alturas inferiores a 1 serão definidas como 1. Se esse argumento não for par e o controle de exibição de árvore não tiver o estilo de [**TVs \_ NONEVENHEIGHT**](tree-view-control-window-styles.md) , esse valor será arredondado para baixo até o valor par mais próximo. Se esse argumento for-1, o controle será revertido para usar sua altura de item padrão.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a altura anterior dos itens, em pixels.

## <a name="remarks"></a>Comentários

O controle de exibição de árvore usa esse valor para a altura de todos os itens. Para modificar a altura de itens individuais, consulte a descrição do membro **iIntegral** da estrutura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**TVM \_ GETITEMHEIGHT**](tvm-getitemheight.md)
</dt> </dl>

 

 






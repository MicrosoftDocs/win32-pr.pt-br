---
title: Mensagem de TTM_TRACKPOSITION (commctrl. h)
description: Define a posição de uma dica de ferramenta de rastreamento.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- Controles de TTM_TRACKPOSITION de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009519"
---
# <a name="ttm_trackposition-message"></a>\_Mensagem TTM TRACKPOSITION

Define a posição de uma dica de ferramenta de rastreamento.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a coordenada x do ponto no qual a dica de ferramenta de rastreamento será exibida, em coordenadas da tela. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a coordenada y do ponto no qual a dica de ferramenta de rastreamento será exibida, em coordenadas da tela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="remarks"></a>Comentários

O controle ToolTip escolhe onde exibir a janela de dica de ferramenta com base nas coordenadas fornecidas com essa mensagem. Isso faz com que a janela ToolTip apareça ao lado da ferramenta à qual ela corresponde. Para que as janelas de dica de ferramenta sejam exibidas em coordenadas específicas, inclua o sinalizador de TTF \_ Absolute no membro **uFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ao adicionar a ferramenta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Usando controles de dica de ferramenta](using-tooltip-contro.md)
</dt> </dl>

 


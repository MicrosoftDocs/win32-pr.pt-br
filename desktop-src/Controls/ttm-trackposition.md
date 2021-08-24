---
title: TTM_TRACKPOSITION mensagem (Commctrl.h)
description: Define a posição de uma dica de ferramenta de acompanhamento.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- TTM_TRACKPOSITION controles Windows mensagem
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
ms.openlocfilehash: 547af5014bbf897d320894c4924911b830997ec3d8532e2ce2c7b63f361a11da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542816"
---
# <a name="ttm_trackposition-message"></a>Mensagem \_ TRACKPOSITION TTM

Define a posição de uma dica de ferramenta de acompanhamento.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a coordenada x do ponto no qual a dica de ferramenta de acompanhamento será exibida, em coordenadas de tela. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a coordenada y do ponto no qual a dica de ferramenta de acompanhamento será exibida, em coordenadas de tela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa mensagem não é usado.

## <a name="remarks"></a>Comentários

O controle de dica de ferramenta escolhe onde exibir a janela de dica de ferramenta com base nas coordenadas fornecidas com essa mensagem. Isso faz com que a janela de dica de ferramenta apareça ao lado da ferramenta à qual ela corresponde. Para exibir janelas de dica de ferramenta em coordenadas específicas, inclua o sinalizador TTF ABSOLUTE no membro \_ **uFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ao adicionar a ferramenta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Usando controles de dica de ferramenta](using-tooltip-contro.md)
</dt> </dl>

 


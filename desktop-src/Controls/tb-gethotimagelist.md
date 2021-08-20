---
title: TB_GETHOTIMAGELIST mensagem (Commctrl.h)
description: Recupera a lista de imagens que um controle de barra de ferramentas usa para exibir botões a quente.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- TB_GETHOTIMAGELIST controles de Windows mensagem
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69d1c77377553ae19a008f80e692e3c87487bc9874593d5f3d1e692658c4ad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168509"
---
# <a name="tb_gethotimagelist-message"></a>Mensagem \_ GETHOTIMAGELIST de TB

Recupera a lista de imagens que um controle de barra de ferramentas usa para exibir botões a quente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para a lista de imagens que o controle usa para exibir botões de acesso ou **NULL** se nenhuma lista de imagens ativas estiver definida.

## <a name="remarks"></a>Comentários

Um botão fica quente quando o cursor está sobre ele. Os controles da barra de ferramentas devem ter o [**estilo TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) ou [**TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) para ter itens ativos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






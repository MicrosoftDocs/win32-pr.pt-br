---
title: Mensagem de TTM_GETDELAYTIME (commctrl. h)
description: Recupera as durações inicial, pop-up e Reexibir atualmente definidas para um controle ToolTip.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- controles de Windows de mensagem de TTM_GETDELAYTIME
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0e63eca126477a6f602e6e23be75495319d30aa2814d2d72b8426a96c078326
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769256"
---
# <a name="ttm_getdelaytime-message"></a>\_Mensagem GETdelaytime TTM

Recupera as durações inicial, pop-up e Reexibir atualmente definidas para um controle ToolTip.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador que especifica qual valor de duração será recuperado. Esse parâmetro pode ter um dos seguintes valores:



| Valor                                                                                                                                                      | Significado                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**TTDT \_ AUTOPOP**</dt> </dl> | Recupere a quantidade de tempo que a janela de dica de ferramenta permanece visível se o ponteiro é estático dentro do retângulo delimitador de uma ferramenta.<br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ inicial**</dt> </dl> | Recupere a quantidade de tempo que o ponteiro deve permanecer fixo dentro do retângulo delimitador de uma ferramenta antes que a janela de dica de ferramentas seja exibida.<br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**remostrar TTDT \_**</dt> </dl>    | Recupere a quantidade de tempo que leva para que janelas de dica de ferramenta subsequentes apareçam à medida que o ponteiro se move de uma das ferramentas para outra.<br/>         |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna e valor INT com a duração especificada em milissegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TTM \_ SETatrasartime**](ttm-setdelaytime.md)
</dt> </dl>

 

 






---
title: Mensagem de TTM_TRACKACTIVATE (commctrl. h)
description: Ativa ou desativa uma dica de ferramenta de rastreamento.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- Controles de TTM_TRACKACTIVATE de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918695"
---
# <a name="ttm_trackactivate-message"></a>\_Mensagem TTM TRACKACTIVATE

Ativa ou desativa uma dica de ferramenta de rastreamento.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica se o rastreamento está sendo ativado ou desativado. Este valor pode ser um dos seguintes:



| Valor                                                                                                                                | Significado                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**TRUE**</dt> </dl>    | Ativar o acompanhamento.<br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**FOR**</dt> </dl> | Desativar o acompanhamento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que identifica a ferramenta à qual essa mensagem se aplica. Os membros de **HWND** e **UID** identificam a ferramenta e o membro **cbSize** especifica o tamanho da estrutura. Todos os outros membros são ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

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

[**TTM \_ TRACKPOSITION**](ttm-trackposition.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Usando controles de dica de ferramenta](using-tooltip-contro.md)
</dt> </dl>

 

 






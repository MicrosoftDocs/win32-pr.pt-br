---
title: Mensagem de TBM_GETTOOLTIPS (commctrl. h)
description: Recupera o identificador para o controle de dica de ferramenta atribuído ao TrackBar, se houver.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- Controles de TBM_GETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824422"
---
# <a name="tbm_gettooltips-message"></a>\_Mensagem tbm GETtooltips

Recupera o identificador para o controle de dica de ferramenta atribuído ao TrackBar, se houver.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o controle de dica de ferramenta atribuído ao TrackBar, ou **NULL** se as dicas de ferramentas não estiverem em uso. Se o controle TrackBar não usar o estilo [**de \_ dicas de ferramenta TBS**](trackbar-control-styles.md) , o valor de retorno será **nulo**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






---
title: Mensagem de TTM_WINDOWFROMPOINT (commctrl. h)
description: Permite que um procedimento de subclasse faça com que uma dica de ferramenta exiba texto para uma janela diferente daquela abaixo do cursor do mouse.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- Controles de TTM_WINDOWFROMPOINT de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68679f6b6c2477a8279c22f11d0d300e44c8370d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644839"
---
# <a name="ttm_windowfrompoint-message"></a>\_Mensagem TTM WINDOWFROMPOINT

Permite que um procedimento de subclasse faça com que uma dica de ferramenta exiba texto para uma janela diferente daquela abaixo do cursor do mouse.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que define o ponto a ser verificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o identificador para a janela que contém o ponto, ou **NULL** se não existir nenhuma janela no ponto especificado.

## <a name="remarks"></a>Comentários

Essa mensagem destina-se a ser processada por um aplicativo que subfaz uma subclasse de ToolTip. Ele não se destina a ser enviado por um aplicativo. Uma dica de ferramenta envia essa mensagem para ela mesma antes de exibir o texto de uma janela. Ao alterar as coordenadas do ponto especificado por *lParam*, o procedimento de subclasse pode fazer com que a dica de ferramenta exiba texto para uma janela diferente daquela abaixo do cursor do mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 


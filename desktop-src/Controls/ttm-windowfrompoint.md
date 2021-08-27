---
title: Mensagem de TTM_WINDOWFROMPOINT (commctrl. h)
description: Permite que um procedimento de subclasse faça com que uma dica de ferramenta exiba texto para uma janela diferente daquela abaixo do cursor do mouse.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- controles de Windows de mensagem de TTM_WINDOWFROMPOINT
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
ms.openlocfilehash: 572ce204fd9f0056ef77d62c7909a7281c478c38f6abeb95089ce86b0bdb1b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109536"
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

## <a name="return-value"></a>Valor retornado

O valor de retorno é o identificador para a janela que contém o ponto, ou **NULL** se não existir nenhuma janela no ponto especificado.

## <a name="remarks"></a>Comentários

Essa mensagem destina-se a ser processada por um aplicativo que subfaz uma subclasse de ToolTip. Ele não se destina a ser enviado por um aplicativo. Uma dica de ferramenta envia essa mensagem para ela mesma antes de exibir o texto de uma janela. Ao alterar as coordenadas do ponto especificado por *lParam*, o procedimento de subclasse pode fazer com que a dica de ferramenta exiba texto para uma janela diferente daquela abaixo do cursor do mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 


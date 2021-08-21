---
title: Mensagem de TBM_GETCHANNELRECT (commctrl. h)
description: Recupera o tamanho e a posição do retângulo delimitador para o canal de um TrackBar.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- controles de Windows de mensagem de TBM_GETCHANNELRECT
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af2c9932782a150635365c1cdcb74b624f6863b27180136bc9483e8d0de3ba1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078100"
---
# <a name="tbm_getchannelrect-message"></a>\_Mensagem tbm GETCHANNELRECT

Recupera o tamanho e a posição do retângulo delimitador para o canal de um TrackBar. (O canal é a área sobre a qual o controle deslizante se move. Ele contém o realce quando um intervalo é selecionado.)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) . A mensagem preenche essa estrutura com o retângulo delimitador do canal, nas coordenadas do cliente da janela do TrackBar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 


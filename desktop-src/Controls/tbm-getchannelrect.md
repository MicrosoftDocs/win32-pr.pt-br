---
title: Mensagem de TBM_GETCHANNELRECT (commctrl. h)
description: Recupera o tamanho e a posição do retângulo delimitador para o canal de um TrackBar.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- Controles de TBM_GETCHANNELRECT de mensagens do Windows
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
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918163"
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

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 


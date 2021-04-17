---
title: Mensagem de ACM_PLAY (commctrl. h)
description: Reproduz um clipe AVI em um controle de animação. O controle reproduz o clipe em segundo plano enquanto o thread continua em execução. Você pode enviar essa mensagem explicitamente ou usando a macro de \_ reprodução de animação.
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- Controles de ACM_PLAY de mensagens do Windows
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454827"
---
# <a name="acm_play-message"></a>Mensagem de reprodução do ACM \_

Reproduz um clipe AVI em um controle de animação. O controle reproduz o clipe em segundo plano enquanto o thread continua em execução. Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ reprodução de animação**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **uint** que especifica o número de vezes para reproduzir o clipe AVI. Um valor de-1 significa repetir o clipe indefinidamente.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é o índice de base zero do quadro em que a execução é iniciada. O valor deve ser menor que 65.536. Um valor de zero significa começar com o primeiro quadro no clipe AVI.

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é o índice de base zero do quadro em que a execução termina. O valor deve ser menor que 65.536. Um valor de-1 significa terminar com o último quadro no clipe AVI.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

Você pode usar o [**Animate \_ Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) para direcionar o controle de animação para exibir um quadro específico do clipe AVI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 


---
title: Mensagem de MCM_GETMINREQRECT (commctrl. h)
description: Recupera o tamanho mínimo necessário para exibir um mês inteiro em um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetMinReqRect.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- Controles de MCM_GETMINREQRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6b2e2b16a70841836a277ffe55e030a6d6a241
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454931"
---
# <a name="mcm_getminreqrect-message"></a>\_Mensagem MCM GETMINREQRECT

Recupera o tamanho mínimo necessário para exibir um mês inteiro em um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que receberá informações de retângulo delimitador. Esse parâmetro deve ser um endereço válido e não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero e *lParam* recebe as informações delimitadoras aplicáveis, se bem-sucedidas. Caso contrário, a mensagem retornará zero.

## <a name="remarks"></a>Comentários

O tamanho mínimo necessário da janela para um controle de calendário mensal depende da fonte atualmente selecionada, dos estilos de controle, das métricas do sistema e das configurações regionais. Quando um aplicativo altera qualquer coisa que afete o tamanho mínimo da janela ou processa uma mensagem do [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) , ele deve enviar **MCM \_ GETMINREQRECT** para determinar o novo tamanho mínimo.

> [!Note]  
> O retângulo retornado por **MCM \_ GETMINREQRECT** não inclui a largura da cadeia de caracteres "Today", se estiver presente. Se o estilo [**MCS \_ nohoje**](month-calendar-control-styles.md) não estiver definido, seu aplicativo também deverá recuperar o retângulo que define a largura da cadeia de caracteres "hoje" enviando uma mensagem [**MCM \_ GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) . Use o maior dos dois retângulos para garantir que a cadeia de caracteres "hoje" não seja recortada.

 

Os membros **superior** e **esquerdo** da estrutura apontados por *lParam* serão sempre zero. Os membros **direito** e **inferior** representam o mínimo de *CX* e *CY* necessários para o controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 


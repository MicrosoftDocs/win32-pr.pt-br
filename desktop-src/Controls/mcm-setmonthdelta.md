---
title: Mensagem de MCM_SETMONTHDELTA (commctrl. h)
description: Define a taxa de rolagem para um controle de calendário mensal. A taxa de rolagem é o número de meses que o controle move sua exibição quando o usuário clica em um botão de rolagem. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetMonthDelta.
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- Controles de MCM_SETMONTHDELTA de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 123eddb55a7ee8ddf8e3f6d8136e9ee57dfc8681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750939"
---
# <a name="mcm_setmonthdelta-message"></a>\_Mensagem MCM SETMONTHDELTA

Define a taxa de rolagem para um controle de calendário mensal. A taxa de rolagem é o número de meses que o controle move sua exibição quando o usuário clica em um botão de rolagem. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que representa o número de meses a serem definidos como a taxa de rolagem do controle. Se esse valor for zero, o Delta do mês será redefinido para o padrão, que é o número de meses exibidos no controle.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor INT que representa a taxa de rolagem anterior. Se a taxa de rolagem não tiver sido definida anteriormente, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

As teclas PAGE UP e PAGE DOWN, VK \_ anterior e VK \_ Next, alteram o mês selecionado em um, independentemente do número de meses exibidos ou do valor definido por **MCM \_ SETMONTHDELTA**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






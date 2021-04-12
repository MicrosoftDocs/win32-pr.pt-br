---
title: Mensagem de MCM_GETCURSEL (commctrl. h)
description: Recupera a data atualmente selecionada. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Getcurseal calendário mensal.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- Controles de MCM_GETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455426"
---
# <a name="mcm_getcursel-message"></a>\_Mensagem GETcurseal MCM

Recupera a data atualmente selecionada. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ getcurseal calendário mensal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que receberá as informações de data atualmente selecionadas. Esse parâmetro deve ser um endereço válido e não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro. Esta mensagem sempre falhará quando aplicada aos controles de calendário de mês definidos como o estilo de [**\_ multiseleção MCS**](month-calendar-control-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Vezes no controle de calendário mensal](month-calendar-controls.md)
</dt> </dl>

 


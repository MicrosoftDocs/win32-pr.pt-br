---
title: Mensagem de MCM_SETMAXSELCOUNT (commctrl. h)
description: Define o número máximo de dias que podem ser selecionados em um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetMaxSelCount.
ms.assetid: 190453ab-e53b-4db7-82c1-f9d50188ad39
keywords:
- Controles de MCM_SETMAXSELCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c67bcb7191bb20b9688c2fe1ffc2b458ecb7b8a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824757"
---
# <a name="mcm_setmaxselcount-message"></a>\_Mensagem MCM SETMAXSELCOUNT

Define o número máximo de dias que podem ser selecionados em um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor do tipo **int** que será definido para representar o número máximo de dias que podem ser selecionados.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro. Esta mensagem falhará se for aplicada a um controle de calendário de mês que não usa o estilo de [**\_ multiseleção MCS**](month-calendar-control-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






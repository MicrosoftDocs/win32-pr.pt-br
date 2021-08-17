---
title: Mensagem de IPM_SETRANGE (commctrl. h)
description: Define o intervalo válido para o campo especificado no controle de endereço IP.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- controles de Windows de mensagem de IPM_SETRANGE
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d599619fa9a065a27a9721b890f6d52c496bf646504009e1950b7ca1279f8a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434466"
---
# <a name="ipm_setrange-message"></a>\_Mensagem IPM SETRANGE

Define o intervalo válido para o campo especificado no controle de endereço IP.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um índice de campo baseado em zero ao qual o intervalo será aplicado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um valor de **palavra** que contém o limite inferior do intervalo no byte de ordem inferior e o limite superior no byte de ordem superior. Esses dois valores são inclusivos. A macro [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) também pode ser usada para criar o intervalo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

Se o usuário inserir um valor no campo que está fora desse intervalo, o controle enviará a notificação [ \_ FieldChanged IPN](ipn-fieldchanged.md) com o valor inserido. Se o valor ainda estiver fora do intervalo após o envio da notificação, o controle tentará alterar o valor inserido para o limite de intervalo mais próximo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






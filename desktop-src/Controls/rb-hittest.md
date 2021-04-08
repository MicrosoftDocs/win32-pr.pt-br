---
title: Mensagem de RB_HITTEST (commctrl. h)
description: Determina qual parte de uma banda de rebar está em um determinado ponto na tela, se existir uma banda de rebar nesse ponto.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- Controles de RB_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008925"
---
# <a name="rb_hittest-message"></a>Mensagem de HITTEST de RB \_

Determina qual parte de uma banda de rebar está em um determinado ponto na tela, se existir uma banda de rebar nesse ponto.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) . Antes de enviar a mensagem, o membro **pt** dessa estrutura deve ser inicializado até o ponto que será testado, nas coordenadas do cliente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice de base zero da banda no ponto determinado, ou-1 se nenhuma banda do rebar estava no ponto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






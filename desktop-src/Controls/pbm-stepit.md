---
title: Mensagem de PBM_STEPIT (commctrl. h)
description: Avança a posição atual de uma barra de progresso pela etapa incremento e redesenha a barra para refletir a nova posição. Um aplicativo define o incremento de etapa enviando a \_ mensagem do PBM SetStep.
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- Controles de PBM_STEPIT de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918789"
---
# <a name="pbm_stepit-message"></a>Mensagem do STEPIT do PBM \_

Avança a posição atual de uma barra de progresso pela etapa incremento e redesenha a barra para refletir a nova posição. Um aplicativo define o incremento de etapa enviando a mensagem do [**PBM \_ SetStep**](pbm-setstep.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a posição anterior.

## <a name="remarks"></a>Comentários

Quando a posição excede o valor de intervalo máximo, essa mensagem redefine a posição atual para que o indicador de progresso comece novamente desde o início.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






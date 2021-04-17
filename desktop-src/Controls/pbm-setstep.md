---
title: Mensagem de PBM_SETSTEP (commctrl. h)
description: Especifica o incremento de etapa para uma barra de progresso. A etapa incremento é a quantidade pela qual a barra de progresso aumenta sua posição atual sempre que recebe uma \_ mensagem STEPIT do PBM. Por padrão, o incremento Step é definido como 10.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- Controles de PBM_SETSTEP de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1240d09aeadcd7994187704d0b5a4630ab1b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754809"
---
# <a name="pbm_setstep-message"></a>\_Mensagem de SETstep do PBM

Especifica o incremento de etapa para uma barra de progresso. A etapa incremento é a quantidade pela qual a barra de progresso aumenta sua posição atual sempre que recebe uma mensagem [**\_ STEPIT do PBM**](pbm-stepit.md) . Por padrão, o incremento Step é definido como 10.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Incremento de nova etapa.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o incremento da etapa anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






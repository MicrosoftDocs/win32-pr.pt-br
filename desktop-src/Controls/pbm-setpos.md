---
title: Mensagem de PBM_SETPOS (commctrl. h)
description: Define a posição atual de uma barra de progresso e redesenha a barra para refletir a nova posição.
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- Controles de PBM_SETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755654"
---
# <a name="pbm_setpos-message"></a>Mensagem do SETPOS do PBM \_

Define a posição atual de uma barra de progresso e redesenha a barra para refletir a nova posição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Inteiro assinado que se torna a nova posição.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a posição anterior.

## <a name="remarks"></a>Comentários

Se *wParam* estiver fora do intervalo do controle, a posição será definida como o limite mais próximo.

Não envie essa mensagem para um controle que tenha o estilo [**de \_ letreiro do PBS**](progress-bar-control-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






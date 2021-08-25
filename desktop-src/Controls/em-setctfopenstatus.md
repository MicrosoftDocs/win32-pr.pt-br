---
title: EM_SETCTFOPENSTATUS mensagem (Richedit.h)
description: Abre ou fecha o teclado Estrutura de Serviços de Texto (TSF).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- EM_SETCTFOPENSTATUS controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ac27017abbadeb038f5b881aefe1aff394036931529c84c9c5a34a36e556c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048626"
---
# <a name="em_setctfopenstatus-message"></a>Mensagem EM \_ SETCTFOPENSTATUS

Abre ou fecha o teclado Estrutura de Serviços de Texto (TSF).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Para ativar o teclado TSF, use **TRUE.** Para desligar o teclado TSF, use **FALSE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedida, essa mensagem retornará **TRUE.** Se não for bem-sucedida, essa mensagem **retornará FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ GETCTFOPENSTATUS**](em-getctfopenstatus.md)
</dt> </dl>

 

 






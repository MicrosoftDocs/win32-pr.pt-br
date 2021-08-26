---
title: UDM_GETRANGE32 mensagem (Commctrl.h)
description: Recupera o intervalo de 32 bits de um controle de cima para baixo.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- UDM_GETRANGE32 controles Windows mensagem
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72078327b7a580768321f14c1d512e097561ae3441667497a822dc8a8a28b4e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077096"
---
# <a name="udm_getrange32-message"></a>Mensagem GETRANGE32 do UDM \_

Recupera o intervalo de 32 bits de um controle de cima para baixo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ponteiro para um inteiro com sinal que recebe o limite inferior do intervalo de controle para cima para baixo. Esse parâmetro pode ser **NULL.**

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um inteiro com sinal que recebe o limite superior do intervalo de controle para cima para baixo. Esse parâmetro pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






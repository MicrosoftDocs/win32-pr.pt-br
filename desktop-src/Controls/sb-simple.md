---
title: SB_SIMPLE mensagem (Commctrl.h)
description: Especifica se uma janela de status exibe texto simples ou exibe todas as partes da janela definidas por uma mensagem SETPARTS SB \_ anterior.
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- SB_SIMPLE controles de Windows mensagem
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f0a896c9adcab6886151753761c62aefb8f4dc6ee21b7e85bb7507bda11f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132206"
---
# <a name="sb_simple-message"></a>Mensagem SB \_ SIMPLE

Especifica se uma janela de status exibe texto simples ou exibe todas as partes da janela definidas por uma mensagem [**\_ SETPARTS SB**](sb-setparts.md) anterior.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de tipo de exibição. Se esse parâmetro for **TRUE,** a janela exibirá texto simples. Se for **FALSE,** ele exibirá várias partes.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

Se a janela de status estiver sendo alterada de não simples para simples ou vice-versa, a janela será redesenhada imediatamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






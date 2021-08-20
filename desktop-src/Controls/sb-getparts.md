---
title: SB_GETPARTS mensagem (Commctrl.h)
description: Recupera uma contagem das partes em uma janela de status. A mensagem também recupera a coordenada da borda direita do número especificado de partes.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- SB_GETPARTS controles de Windows mensagem
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4318579b67adda9ab55a9dad4ad73949214758443c5e2151ce40cbb996fd90cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168752"
---
# <a name="sb_getparts-message"></a>Mensagem \_ GETPARTS do SB

Recupera uma contagem das partes em uma janela de status. A mensagem também recupera a coordenada da borda direita do número especificado de partes.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de partes para as quais recuperar coordenadas. Se esse parâmetro for maior que o número de partes na janela, a mensagem recuperará as coordenadas apenas para partes existentes.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de inteiros que tem o mesmo número de elementos que as partes especificadas por *wParam*. Cada elemento na matriz recebe a coordenada do cliente da borda direita da parte correspondente. Se um elemento for definido como -1, a posição da borda direita dessa parte se estenderá para a borda direita da janela. Para recuperar o número atual de partes, de definido esse parâmetro como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o número de partes na janela.

## <a name="remarks"></a>Comentários

Essa mensagem sempre retorna o número de partes na barra de status.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






---
title: Mensagem de SB_GETPARTS (commctrl. h)
description: Recupera uma contagem das partes em uma janela de status. A mensagem também recupera a coordenada da borda direita do número especificado de partes.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- Controles de SB_GETPARTS de mensagens do Windows
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
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499597"
---
# <a name="sb_getparts-message"></a>Mensagem da SB \_ GETparts

Recupera uma contagem das partes em uma janela de status. A mensagem também recupera a coordenada da borda direita do número especificado de partes.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de partes para as quais recuperar as coordenadas. Se esse parâmetro for maior que o número de partes na janela, a mensagem recuperará coordenadas somente para partes existentes.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de inteiros que tem o mesmo número de elementos que as partes especificadas por *wParam*. Cada elemento na matriz recebe a coordenada do cliente da borda direita da parte correspondente. Se um elemento for definido como-1, a posição da borda direita dessa parte se estenderá para a borda direita da janela. Para recuperar o número atual de partes, defina esse parâmetro como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de partes na janela.

## <a name="remarks"></a>Comentários

Essa mensagem sempre retorna o número de partes na barra de status.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






---
title: Mensagem de SB_GETBORDERS (commctrl. h)
description: Recupera as larguras atuais das bordas horizontais e verticais de uma janela de status.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- controles de Windows de mensagem de SB_GETBORDERS
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafa7a8c27b5c274a981e43edc5c55ec0cade67cac08a1d09a898916d792795c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169049"
---
# <a name="sb_getborders-message"></a>Mensagem da SB \_ GETborders

Recupera as larguras atuais das bordas horizontais e verticais de uma janela de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma matriz de inteiros que tem três elementos. O primeiro elemento recebe a largura da borda horizontal, a segunda recebe a largura da borda vertical e a terceira recebe a largura da borda entre retângulos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

As bordas determinam o espaçamento entre a borda externa da janela e os retângulos dentro da janela que contêm texto. As bordas também determinam o espaçamento entre retângulos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






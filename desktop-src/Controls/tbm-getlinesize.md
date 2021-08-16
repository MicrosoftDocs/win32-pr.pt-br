---
title: Mensagem de TBM_GETLINESIZE (commctrl. h)
description: Recupera o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado das teclas de direção, como as chaves ou. As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- controles de Windows de mensagem de TBM_GETLINESIZE
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6db69efda8a6836f8c366092871cbb6b54261021a69c80e2bb14abcd88d967
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046556"
---
# <a name="tbm_getlinesize-message"></a>TBM \_ GETlinhasize mensagem

Recupera o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado das teclas de direção, como as chaves ou. As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 32 bits que especifica o tamanho da linha para o TrackBar.

## <a name="remarks"></a>Comentários

A configuração padrão para o tamanho da linha é 1.

O TrackBar também envia uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) com os códigos de notificação da lista de TB \_ e TB \_ LINEDOWN para sua janela pai quando o usuário pressiona as teclas de direção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 






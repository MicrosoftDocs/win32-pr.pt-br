---
title: TBM_GETLINESIZE mensagem (Commctrl.h)
description: Recupera o número de posições lógicas que o controle deslizante da barra de faixa move em resposta à entrada do teclado das teclas de direção, como as teclas ou . As posições lógicas são os incrementos inteiros no intervalo da barra de faixa de posições mínimas para máximas do controle deslizante.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- TBM_GETLINESIZE controles de Windows mensagem
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
# <a name="tbm_getlinesize-message"></a>Mensagem \_ GETLINESIZE do TBM

Recupera o número de posições lógicas que o controle deslizante da barra de faixa move em resposta à entrada do teclado das teclas de direção, como as teclas ou . As posições lógicas são os incrementos inteiros no intervalo da barra de faixa de posições mínimas para máximas do controle deslizante.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 32 bits que especifica o tamanho da linha para a barra de faixa.

## <a name="remarks"></a>Comentários

A configuração padrão para o tamanho da linha é 1.

A barra de faixa também envia uma mensagem [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) com os códigos de notificação TBTB e TB LINEDOWN para sua janela pai quando o usuário pressiona as teclas de \_ \_ seta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






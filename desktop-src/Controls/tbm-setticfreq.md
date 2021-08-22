---
title: TBM_SETTICFREQ mensagem (Commctrl.h)
description: Define a frequência de intervalo para marcas de escala em uma barra de faixa.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- TBM_SETTICFREQ controles de Windows mensagem
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c1b3e029abc8027d8708da31698f44db85ec78e427ba9461f0a71a740fb05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078010"
---
# <a name="tbm_setticfreq-message"></a>Mensagem TBM \_ SETTICFREQ

Define a frequência de intervalo para marcas de escala em uma barra de faixa. Por exemplo, se a frequência for definida como dois, uma marca de escala será exibida para todos os outros incrementos no intervalo da barra de faixas. A configuração padrão para a frequência é uma; ou seja, cada incremento no intervalo é associado a uma marca de escala.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Frequência das marcas de escala.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A barra de faixa deve ter o [**estilo TBS \_ AUTOTICKS**](trackbar-control-styles.md) para usar essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 






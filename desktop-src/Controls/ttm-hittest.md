---
title: Mensagem de TTM_HITTEST (commctrl. h)
description: Testa um ponto para determinar se ele está dentro do retângulo delimitador da ferramenta especificada e, se for, recupera informações sobre a ferramenta.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- controles de Windows de mensagem de TTM_HITTEST
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105edd555a1da1ba037f7dda114e1d9f9ef53048c02a7cb11e1df1ff0c01ad2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060516"
---
# <a name="ttm_hittest-message"></a>\_Mensagem TTM HITTEST

Testa um ponto para determinar se ele está dentro do retângulo delimitador da ferramenta especificada e, se for, recupera informações sobre a ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) . Ao enviar a mensagem, o membro **HWND** deve especificar o identificador para uma ferramenta e o membro **pt** deve especificar as coordenadas de um ponto. Se o valor de retorno for **true**, o membro de **ti** (uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ) receberá informações sobre a ferramenta que ocupa o ponto. O membro **cbSize** da estrutura de **ti** deve ser preenchido antes de enviar esta mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se a ferramenta ocupar o ponto especificado ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Esta mensagem deve ser enviada quando a ferramenta tiver o sinalizador de faixa de TTF \_ definido. Para obter mais informações sobre esse sinalizador, consulte [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa). \_O TTM HITTEST falhará se \_ a faixa de TTF não estiver definida, independentemente se o ponto de acesso estiver no retângulo de ferramentas ou não.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ HITTESTW** (Unicode) e **TTM \_ hittesta** (ANSI)<br/>                   |



 

 






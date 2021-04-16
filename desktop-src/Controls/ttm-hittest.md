---
title: Mensagem de TTM_HITTEST (commctrl. h)
description: Testa um ponto para determinar se ele está dentro do retângulo delimitador da ferramenta especificada e, se for, recupera informações sobre a ferramenta.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- Controles de TTM_HITTEST de mensagens do Windows
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
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455168"
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

## <a name="return-value"></a>Retornar valor

Retornará **true** se a ferramenta ocupar o ponto especificado ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Esta mensagem deve ser enviada quando a ferramenta tiver o sinalizador de faixa de TTF \_ definido. Para obter mais informações sobre esse sinalizador, consulte [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa). \_O TTM HITTEST falhará se \_ a faixa de TTF não estiver definida, independentemente se o ponto de acesso estiver no retângulo de ferramentas ou não.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ HITTESTW** (Unicode) e **TTM \_ hittesta** (ANSI)<br/>                   |



 

 






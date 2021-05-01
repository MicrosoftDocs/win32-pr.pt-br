---
title: Mensagem de TTM_ENUMTOOLS (commctrl. h)
description: Recupera as informações que um controle ToolTip mantém sobre a ferramenta atual \ 8212; ou seja, a ferramenta para a qual ToolTip está atualmente exibindo texto.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- Controles de TTM_ENUMTOOLS de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67f23a145838aa3562c81e78fb82c3ea66320df
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327131"
---
# <a name="ttm_enumtools-message"></a>\_Mensagem TTM ENUMTOOLS

Recupera as informações que um controle ToolTip mantém sobre a ferramenta atual, que é a ferramenta para a qual a dica de ferramentas está exibindo texto no momento.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da ferramenta para a qual recuperar informações.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que recebe informações sobre a ferramenta. Defina o membro **cbSize** dessa estrutura como sizeof (TOOLINFO) antes de enviar esta mensagem. Aloque um buffer. Defina o membro **lpszText** para apontar para o buffer para receber o texto da ferramenta. Não é possível determinar o tamanho do buffer necessário. No entanto, o texto da ferramenta, como retornado no membro **lpszText** da estrutura **TOOLINFO** , tem um comprimento máximo de 80 **TCHARs**, incluindo o **nulo** de terminação. Se o texto exceder esse comprimento, ele será truncado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **false** se uma ferramenta foi enumerada ou não.

## <a name="remarks"></a>Comentários

**Aviso de segurança:** O uso dessa mensagem pode comprometer a segurança do seu programa. Essa mensagem não fornece uma maneira para o destinatário da mensagem saber o tamanho do buffer ou para especificar o tamanho do buffer. Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ ENUMTOOLSW** (Unicode) e **TTM \_ ENUMTOOLSA** (ANSI)<br/>               |



 

 






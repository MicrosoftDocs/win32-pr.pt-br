---
title: Mensagem de TTM_GETTEXT (commctrl. h)
description: Recupera as informações que um controle ToolTip mantém sobre uma ferramenta.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- Controles de TTM_GETTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753784"
---
# <a name="ttm_gettext-message"></a>\_Mensagem GETTEXT TTM

Recupera as informações que um controle ToolTip mantém sobre uma ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>O número de **TCHARs**, incluindo o **nulo** de terminação, a ser copiado para o buffer apontado por **lpszText**. </dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Defina o membro **cbSize** dessa estrutura como `sizeof(TOOLINFO)` antes de enviar essa mensagem. Defina os membros de **HWND** e **UID** para identificar a ferramenta para a qual recuperar informações. Aloque um buffer de tamanho especificado por *wParam*. Defina o membro **lpszText** para apontar para o buffer para receber o texto da ferramenta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ GETTEXTW** (Unicode) e **TTM \_ gettexta** (ANSI)<br/>                   |



 

 






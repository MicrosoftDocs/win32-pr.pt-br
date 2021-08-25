---
title: TTM_GETTEXT mensagem (Commctrl.h)
description: Recupera as informações que um controle de dica de ferramenta mantém sobre uma ferramenta.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- TTM_GETTEXT controles de Windows mensagem
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
ms.openlocfilehash: 9efe79105c705eba3dd25c124cf17ff0e4773618608bc7ef86ebbf3d0d9f715e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967886"
---
# <a name="ttm_gettext-message"></a>Mensagem \_ GETTEXT TTM

Recupera as informações que um controle de dica de ferramenta mantém sobre uma ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>O número de **TCHARs**, incluindo o **NULL** de terminação, a ser copiado para o buffer apontado por **lpszText**. </dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) De definir **o membro cbSize** dessa estrutura como `sizeof(TOOLINFO)` antes de enviar essa mensagem. De definir os **membros hwnd** e **uId** para identificar a ferramenta para a qual recuperar informações. Aloce um buffer de tamanho especificado por *wParam*. De definir **o membro lpszText** para apontar para o buffer para receber o texto da ferramenta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ GETTEXTW** (Unicode) e **TTM \_ GETTEXTA** (ANSI)<br/>                   |



 

 






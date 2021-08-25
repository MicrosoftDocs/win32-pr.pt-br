---
description: Enviado para a função CPlApplet de um aplicativo de painel de controle para recuperar o número de caixas de diálogo com suporte no aplicativo.
title: Mensagem de CPL_GETCOUNT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58f95a62d17ccafd308666a5632a1f7a42ebfda6ca0a54dfb6dfa9d9eda9b684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715476"
---
# <a name="cpl_getcount-message"></a>\_Mensagem de SQLcount do CPL

Enviado para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo de painel de controle para recuperar o número de caixas de diálogo com suporte no aplicativo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) retorna o número de caixas de diálogo que o aplicativo do painel de controle suporta.

## <a name="remarks"></a>Comentários

Essa mensagem é enviada imediatamente após a mensagem de [**\_ init de CPL**](cpl-init.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 

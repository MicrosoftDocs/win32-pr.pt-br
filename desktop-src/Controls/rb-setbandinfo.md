---
title: RB_SETBANDINFO mensagem (Commctrl.h)
description: Define características de uma banda existente em um controle de barra rebar.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- RB_SETBANDINFO controles de Windows mensagem
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee89d91bc65556179d14c7e86a69a9e6399223f38bb1bcc44f746d7cd8f8a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798466"
---
# <a name="rb_setbandinfo-message"></a>Mensagem RB \_ SETBANDINFO

Define características de uma banda existente em um controle de barra rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero da banda para receber as novas configurações.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que define a banda a ser modificada e as novas configurações. Antes de enviar essa mensagem, você deve definir o membro **cbSize** dessa estrutura como a estrutura **sizeof**(REBARBANDINFO). Além disso, você deve definir o membro **cch** da estrutura **REBARBANDINFO** para o tamanho do buffer **lpText** quando RBBIM \_ TEXT for especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **RB \_ SETBANDINFOW** (Unicode) e **RB \_ SETBANDINFOA** (ANSI)<br/>             |



 

 






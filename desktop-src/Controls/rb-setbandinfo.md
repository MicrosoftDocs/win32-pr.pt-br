---
title: Mensagem de RB_SETBANDINFO (commctrl. h)
description: Define características de uma banda existente em um controle rebar.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- Controles de RB_SETBANDINFO de mensagens do Windows
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
ms.openlocfilehash: 92e81377a40f8b6054f5d8cfae16837621b77b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455529"
---
# <a name="rb_setbandinfo-message"></a>\_Mensagem SETBANDINFO RB

Define características de uma banda existente em um controle rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da banda para receber as novas configurações.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que define a banda a ser modificada e as novas configurações. Antes de enviar essa mensagem, você deve definir o membro **cbSize** dessa estrutura como a estrutura **sizeof**(REBARBANDINFO). Além disso, você deve definir o membro **cch** da estrutura **REBARBANDINFO** para o tamanho do buffer **lpText** quando o \_ texto RBBIM for especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **RB \_ SETBANDINFOW** (Unicode) e **RB \_ SETBANDINFOA** (ANSI)<br/>             |



 

 






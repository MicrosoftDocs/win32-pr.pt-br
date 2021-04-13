---
title: Mensagem de TTM_SETTOOLINFO (commctrl. h)
description: Define as informações que um controle ToolTip mantém para uma ferramenta.
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- Controles de TTM_SETTOOLINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455891"
---
# <a name="ttm_settoolinfo-message"></a>\_Mensagem TTM SETTOOLINFO

Define as informações que um controle ToolTip mantém para uma ferramenta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que especifica as informações a serem definidas. O membro **cbSize** desta estrutura deve ser definido antes de enviar esta mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Algumas propriedades internas de uma ferramenta são estabelecidas quando a ferramenta é criada e não são recomputadas quando uma mensagem **TTM \_ SETTOOLINFO** é enviada. Se você simplesmente atribuir valores a uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) e passá-lo para o controle ToolTip com uma mensagem **TTM \_ SETTOOLINFO** , essas propriedades poderão ser perdidas. Em vez disso, seu aplicativo deve primeiro solicitar a estrutura **TOOLINFO** atual da ferramenta enviando o controle ToolTip a uma mensagem [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md) . Em seguida, modifique os membros dessa estrutura conforme necessário e passe-os de volta para o controle ToolTip com **TTM \_ SETTOOLINFO**.

Ao chamar **TTM \_ SETTOOLINFO**, a cadeia de caracteres apontada pelo membro **lpszText** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) não deve exceder 80 **TCHARs** de comprimento, incluindo o **nulo** de terminação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTM \_ SETTOOLINFOW** (Unicode) e **TTM \_ SETTOOLINFOA** (ANSI)<br/>           |



 

 






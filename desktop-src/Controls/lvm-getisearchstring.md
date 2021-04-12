---
title: Mensagem de LVM_GETISEARCHSTRING (commctrl. h)
description: Recupera a cadeia de caracteres de pesquisa incremental de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetISearchString do ListView.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- Controles de LVM_GETISEARCHSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455749"
---
# <a name="lvm_getisearchstring-message"></a>\_Mensagem GETISEARCHSTRING LVM

Recupera a cadeia de caracteres de pesquisa incremental de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetISearchString do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um buffer que recebe a cadeia de caracteres de pesquisa incremental. Para recuperar apenas o comprimento da cadeia de caracteres, defina *lParam* como **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de caracteres na cadeia de caracteres de pesquisa incremental, não incluindo o caractere nulo de terminação ou zero se o controle de exibição de lista não estiver no modo de pesquisa incremental.

## <a name="remarks"></a>Comentários

**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do seu programa. Essa mensagem não fornece uma maneira de saber o tamanho do buffer. Se você usar essa mensagem, primeiro chame a mensagem transmitindo **NULL** no *lParam*; isso retorna o número de caracteres, excluindo **NULL** que são necessários. Em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres. Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.

A seqüência de caracteres de *pesquisa incremental* é a sequência de caracteres que o usuário digita enquanto a exibição de lista tem o foco de entrada. Cada vez que o usuário digita um caractere, o sistema anexa o caractere à cadeia de caracteres de pesquisa e, em seguida, procura um item correspondente. Se o sistema encontrar uma correspondência, ele selecionará o item e, se necessário, o rolará para o modo de exibição.

Um período de tempo limite é associado a cada caractere que o usuário digita. Se o período de tempo limite expirar antes de o usuário digitar outro caractere, a cadeia de caracteres de pesquisa incremental será redefinida.

Verifique se o buffer é grande o suficiente para manter a cadeia de caracteres e o caractere nulo de terminação. Se for muito pequeno, será resultado uma falha de página inválida imediata.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ GETISEARCHSTRINGW** (Unicode) e **LVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 






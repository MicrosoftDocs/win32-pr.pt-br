---
title: Mensagem de LVM_GETISEARCHSTRING (commctrl. h)
description: Recupera a cadeia de caracteres de pesquisa incremental de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetISearchString do ListView.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- controles de Windows de mensagem de LVM_GETISEARCHSTRING
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
ms.openlocfilehash: d612a6c1ba303bc08b6d5067ccb4dd3802354456159e3aea4120bd122348e74f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540816"
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

## <a name="return-value"></a>Valor retornado

Retorna o número de caracteres na cadeia de caracteres de pesquisa incremental, não incluindo o caractere nulo de terminação ou zero se o controle de exibição de lista não estiver no modo de pesquisa incremental.

## <a name="remarks"></a>Comentários

**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do seu programa. Essa mensagem não fornece uma maneira de saber o tamanho do buffer. Se você usar essa mensagem, primeiro chame a mensagem transmitindo **NULL** no *lParam*; isso retorna o número de caracteres, excluindo **NULL** que são necessários. Em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres. você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.

A seqüência de caracteres de *pesquisa incremental* é a sequência de caracteres que o usuário digita enquanto a exibição de lista tem o foco de entrada. Cada vez que o usuário digita um caractere, o sistema anexa o caractere à cadeia de caracteres de pesquisa e, em seguida, procura um item correspondente. Se o sistema encontrar uma correspondência, ele selecionará o item e, se necessário, o rolará para o modo de exibição.

Um período de tempo limite é associado a cada caractere que o usuário digita. Se o período de tempo limite expirar antes de o usuário digitar outro caractere, a cadeia de caracteres de pesquisa incremental será redefinida.

Verifique se o buffer é grande o suficiente para manter a cadeia de caracteres e o caractere nulo de terminação. Se for muito pequeno, será resultado uma falha de página inválida imediata.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ GETISEARCHSTRINGW** (Unicode) e **LVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 






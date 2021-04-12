---
title: Mensagem de EM_EXLIMITTEXT (RichEdit. h)
description: Define um limite superior para a quantidade de texto que o usuário pode digitar ou colar em um controle de edição rico.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- Controles de EM_EXLIMITTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455440"
---
# <a name="em_exlimittext-message"></a>\_Mensagem em EXLIMITTEXT

Define um limite superior para a quantidade de texto que o usuário pode digitar ou colar em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica a quantidade máxima de texto que pode ser inserida. Se esse parâmetro for zero, o máximo padrão será usado, que é de 64K caracteres. Um objeto COM conta como um único caractere.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

O limite de texto definido pela mensagem em **\_ EXLIMITTEXT** não limita a quantidade de texto que você pode transmitir em um controle de edição rico usando a mensagem de [**\_ fluxo**](em-streamin.md) em em com *lParam* definido como \_ SMS. No entanto, ele limita a quantidade de texto que você pode transmitir em um controle de edição rico usando a mensagem de **\_ fluxo** em em com *lParam* definido como it \_ RTF.

Antes **de \_ EXLIMITTEXT** ser chamado, o limite padrão para a quantidade de texto que um usuário pode inserir é de 32.767 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**fluxo de em \_**](em-streamin.md)
</dt> </dl>

 

 






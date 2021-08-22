---
title: EM_GETWORDWRAPMODE mensagem (Richedit.h)
description: Obtém as opções de quebra de palavras e quebra de palavras atuais para o controle de edição rich.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- EM_GETWORDWRAPMODE controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef3127e5ce3652e9103dfa0e030d66ec7b1b085bc4b60d0cf0bb3f03a30d3fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437946"
---
# <a name="em_getwordwrapmode-message"></a>Mensagem EM \_ GETWORDWRAPMODE

Obtém as opções de quebra de palavras e quebra de palavras atuais para o controle de edição rich.

> [!Note]  
> Essa mensagem só tem suporte em versões de idioma asiático do Microsoft Rich Edit 1.0. Não há suporte para ele em nenhuma versão posterior do Rich Edit.

 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A mensagem retorna as opções de quebra de palavras e quebra de palavras atuais.

## <a name="remarks"></a>Comentários

Essa mensagem não deve ser enviada pelo procedimento de quebra de palavras definido pelo aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 






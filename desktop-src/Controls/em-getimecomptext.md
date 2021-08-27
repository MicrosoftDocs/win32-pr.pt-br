---
title: Mensagem de EM_GETIMECOMPTEXT (RichEdit. h)
description: Recupera o texto de composição do IME (editor de método de entrada).
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- controles de Windows de mensagem de EM_GETIMECOMPTEXT
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd915f037275d428df37ca02a206b936a63bfd2f6ac8fbb605d1573b9535789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049066"
---
# <a name="em_getimecomptext-message"></a>\_Mensagem em GETIMECOMPTEXT

Recupera o texto de composição do IME (editor de método de entrada).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A estrutura [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) .

</dd> <dt>

*lParam* 
</dt> <dd>

O buffer que recebe o texto de composição. O tamanho desse buffer está contido no membro **CB** da estrutura *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, o valor de retorno será o número de caracteres Unicode copiados para o buffer. Caso contrário, será zero.

## <a name="remarks"></a>Comentários

Essa mensagem usa apenas cadeias de caracteres Unicode.

**Aviso de segurança:** Certifique-se de ter um buffer suficiente para o tamanho da entrada. A falha em fazer isso pode causar problemas para seu aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho do SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 






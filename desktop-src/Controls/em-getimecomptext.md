---
title: Mensagem de EM_GETIMECOMPTEXT (RichEdit. h)
description: Recupera o texto de composição do IME (editor de método de entrada).
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- Controles de EM_GETIMECOMPTEXT de mensagens do Windows
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
ms.openlocfilehash: 834c55d6b5e40de7dcacfeb3e2d0c2e0878a0f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918806"
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

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, o valor de retorno será o número de caracteres Unicode copiados para o buffer. Caso contrário, será zero.

## <a name="remarks"></a>Comentários

Essa mensagem usa apenas cadeias de caracteres Unicode.

**Aviso de segurança:** Certifique-se de ter um buffer suficiente para o tamanho da entrada. A falha em fazer isso pode causar problemas para seu aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP com SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 






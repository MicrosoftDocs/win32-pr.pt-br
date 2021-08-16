---
title: EM_SETSCROLLPOS mensagem (Richedit.h)
description: Rola o conteúdo de um controle de edição rich para o ponto especificado.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- EM_SETSCROLLPOS controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d86609c1b3f4b04ade24e5ea2f3343c367bbad0a52b8e07be7c18b2282536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412331"
---
# <a name="em_setscrollpos-message"></a>Mensagem EM \_ SETSCROLLPOS

Rola o conteúdo de um controle de edição rich para o ponto especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura POINT**](/previous-versions//dd162805(v=vs.85)) que especifica um ponto no espaço de texto virtual do documento, expresso em pixels. O documento será rolado até que esse ponto seja localizado no canto superior esquerdo da janela de controle de edição. Se você quiser alterar a exibição de forma que o canto superior esquerdo da exibição seja duas linhas para baixo e um caractere na borda esquerda. Você passará um ponto de (7, 22).

O controle de edição rich verifica as coordenadas x e y e as ajusta, se necessário, para que uma linha completa seja exibida na parte superior. Ele também garante que o texto nunca seja completamente rolado para fora do retângulo de exibição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem sempre retorna 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Redistribuível<br/>          | Rich Edit 3.0<br/>                                                              |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> </dl>

 


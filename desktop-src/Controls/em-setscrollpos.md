---
title: Mensagem de EM_SETSCROLLPOS (RichEdit. h)
description: Rola o conteúdo de um controle de edição rico para o ponto especificado.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- Controles de EM_SETSCROLLPOS de mensagens do Windows
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
ms.openlocfilehash: ec41ac5255059b8d40f3a4c2e9b666815b9094fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455760"
---
# <a name="em_setscrollpos-message"></a>\_Mensagem em SETSCROLLPOS

Rola o conteúdo de um controle de edição rico para o ponto especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que especifica um ponto no espaço de texto virtual do documento, expresso em pixels. O documento será rolado até que esse ponto esteja localizado no canto superior esquerdo da janela de controle de edição. Se você quiser alterar a exibição de modo que o canto superior esquerdo da exibição tenha duas linhas abaixo e um caractere na borda esquerda. Você passaria um ponto de (7, 22).

O controle Rich Edit Verifica as coordenadas x e y e as ajusta, se necessário, para que uma linha completa seja exibida na parte superior. Ele também garante que o texto nunca seja completamente rolado para fora do retângulo de exibição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem sempre retorna 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| Redistribuível<br/>          | Edição avançada 3,0<br/>                                                              |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> </dl>

 


---
title: Mensagem de EM_SETPUNCTUATION (RichEdit. h)
description: Define os caracteres de Pontuação para um controle de edição rico.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- controles de Windows de mensagem de EM_SETPUNCTUATION
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5e0856c1ee1882695dc5e6d7dfdd6b72ea0f6c4f16ee7396bbfde2b76b49b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062896"
---
# <a name="em_setpunctuation-message"></a>\_Mensagem em SETpontuation

Define os caracteres de Pontuação para um controle de edição rico.

> [!Note]  
> Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0. Não há suporte para ele em nenhuma versão posterior.

 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o tipo de pontuação, que pode ser um dos valores a seguir.



| Valor                                                                                                                                                      | Significado                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**líder do PC \_**</dt> </dl>       | Caracteres de Pontuação à esquerda.<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC a \_ seguir**</dt> </dl> | Caracteres de Pontuação a seguir.<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**delimitador de PC \_**</dt> </dl> | Delimitador.<br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <dt>**PC \_ ESTOURO**</dt> </dl> | Sem suporte.<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**Pontuação**](/windows/desktop/api/Richedit/ns-richedit-punctuation) que contém os caracteres de pontuação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.

Se a operação falhar, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ GETpontuation**](em-getpunctuation.md)
</dt> <dt>

[**Pontuação**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 






---
title: Mensagem de EM_GETPUNCTUATION (RichEdit. h)
description: Obtém os caracteres de Pontuação atuais para o controle de edição rico.
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- Controles de EM_GETPUNCTUATION de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086095"
---
# <a name="em_getpunctuation-message"></a>\_Mensagem em GETpontuation

Obtém os caracteres de Pontuação atuais para o controle de edição rico.

> [!Note]  
> Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0. Não há suporte para ele em versões posteriores do rich edit.

 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de Pontuação pode ser um dos valores a seguir.



| Valor                                                                                                                                                      | Significado                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**líder do PC \_**</dt> </dl>       | Caracteres de Pontuação à esquerda<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC a \_ seguir**</dt> </dl> | Seguintes caracteres de Pontuação<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**delimitador de PC \_**</dt> </dl> | Delimitador<br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <dt>**estouro de PC \_**</dt> </dl>    | Sem suporte<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**Pontuação**](/windows/desktop/api/Richedit/ns-richedit-punctuation) que recebe os caracteres de pontuação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.

Se a operação falhar, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ SETpontuation**](em-setpunctuation.md)
</dt> <dt>

[**Pontuação**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 






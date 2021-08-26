---
title: Mensagem de EM_SETPARAFORMAT (RichEdit. h)
description: Define a formatação de parágrafo para a seleção atual em um controle de edição rico.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- controles de Windows de mensagem de EM_SETPARAFORMAT
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db0ba4e4bf505c5fb1b746b84cae71dcc621635a0a33b4a533ce8551486fe6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062906"
---
# <a name="em_setparaformat-message"></a>\_Mensagem em SETPARAFORMAT

Define a formatação de parágrafo para a seleção atual em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**PARAformativa**](/windows/desktop/api/Richedit/ns-richedit-paraformat) especificando os novos atributos de formatação de parágrafo. Somente os atributos especificados pelo membro **dwMask** são alterados.

Microsoft rich edit 2,0 e posterior: esse parâmetro pode ser um ponteiro para uma estrutura [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , que é uma extensão da estrutura [**paraformativa**](/windows/desktop/api/Richedit/ns-richedit-paraformat) . Antes de enviar a mensagem em **\_ SETPARAFORMAT** , defina o membro **cbSize** da estrutura para indicar a versão da estrutura.

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

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 






---
title: Mensagem de EM_GETPARAFORMAT (RichEdit. h)
description: Recupera a formatação de parágrafo da seleção atual em um controle de edição rico.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- Controles de EM_GETPARAFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49060861a955e85d153fc9041c9b364db109f83a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918986"
---
# <a name="em_getparaformat-message"></a>\_Mensagem em GETPARAFORMAT

Recupera a formatação de parágrafo da seleção atual em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**PARAformativa**](/windows/desktop/api/Richedit/ns-richedit-paraformat) que recebe os atributos de formatação de parágrafo da seleção atual.

Se mais de um parágrafo for selecionado, a estrutura receberá os atributos do primeiro parágrafo e o membro **dwMask** especificará quais atributos são consistentes em toda a seleção.

Microsoft rich edit 2,0 e posterior: esse parâmetro pode ser um ponteiro para uma estrutura [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , que é uma extensão da estrutura [**paraformativa**](/windows/desktop/api/Richedit/ns-richedit-paraformat) . Antes de enviar a mensagem em **\_ GETPARAFORMAT** , defina o membro **cbSize** da estrutura para indicar a versão da estrutura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna o valor do membro **dwMask** da estrutura [**paraformate**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .

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

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 






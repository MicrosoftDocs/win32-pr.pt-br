---
title: Mensagem de EM_SETPARAFORMAT (RichEdit. h)
description: Define a formatação de parágrafo para a seleção atual em um controle de edição rico.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- Controles de EM_SETPARAFORMAT de mensagens do Windows
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
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455020"
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

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 






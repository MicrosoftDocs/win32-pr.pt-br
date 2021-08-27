---
title: EM_GETPARAFORMAT mensagem (Richedit.h)
description: Recupera a formatação de parágrafo da seleção atual em um controle de edição rico.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- EM_GETPARAFORMAT controles Windows mensagem
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
ms.openlocfilehash: eda99d1fefc0e2a13cc989726c86588103b7f94d7042b98393709cf4a2cd5f29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048846"
---
# <a name="em_getparaformat-message"></a>Mensagem \_ EM GETPARAFORMAT

Recupera a formatação de parágrafo da seleção atual em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) que recebe os atributos de formatação de parágrafo da seleção atual.

Se mais de um parágrafo for selecionado, a estrutura receberá os atributos do primeiro parágrafo e o membro **dwMask** especificará quais atributos são consistentes em toda a seleção.

Microsoft Rich Edit 2.0 e posterior: esse parâmetro pode ser um ponteiro para uma estrutura [**PARAFORMAT2,**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) que é uma extensão da [**estrutura PARAFORMAT.**](/windows/desktop/api/Richedit/ns-richedit-paraformat) Antes de enviar **a mensagem EM \_ GETPARAFORMAT,** de definir o membro **cbSize** da estrutura para indicar a versão da estrutura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem retorna o valor do **membro dwMask** da [**estrutura PARAFORMAT.**](/windows/desktop/api/Richedit/ns-richedit-paraformat)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**Paraformat2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 






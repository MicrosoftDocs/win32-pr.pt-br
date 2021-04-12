---
title: Mensagem de EM_SETIMECOLOR (RichEdit. h)
description: Define a cor de composição do IME (editor de método de entrada) para um controle de edição rico.
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- Controles de EM_SETIMECOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c020bb3af2b1197afc005bd0b6efec82b609b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455348"
---
# <a name="em_setimecolor-message"></a>\_Mensagem em SETIMECOLOR

Define a cor de composição do IME (editor de método de entrada) para um controle de edição rico.

> [!Note]  
> Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0. Não há suporte para ele em nenhuma versão posterior.

 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) que contém a cor de composição a ser definida.

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

[**em \_ GETIMECOLOR**](em-getimecolor.md)
</dt> <dt>

[**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 






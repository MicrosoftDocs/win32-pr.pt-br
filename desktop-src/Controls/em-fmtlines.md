---
title: Mensagem de EM_FMTLINES (WinUser. h)
description: Define um sinalizador que determina se um controle de edição de várias linhas inclui caracteres de quebra de linha flexível. Uma quebra de linha suave consiste em dois retornos de carro e um feed de linha e é inserido no final de uma linha quebrada por causa de wordwrapping.
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- Controles de EM_FMTLINES de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c12a22ee8c30ffa74705f670a16caa3651e9b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455280"
---
# <a name="em_fmtlines-message"></a>\_Mensagem em FMTLINES

Define um sinalizador que determina se um controle de edição de várias linhas inclui caracteres de quebra de linha flexível. Uma quebra de linha suave consiste em dois retornos de carro e um feed de linha e é inserido no final de uma linha quebrada por causa de wordwrapping.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se os caracteres de quebra de linha flexível devem ser inseridos. Um valor **true** insere os caracteres; um valor **false** remove-os.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é idêntico ao parâmetro *wParam* .

## <a name="remarks"></a>Comentários

Essa mensagem afeta apenas o buffer retornado pela mensagem [**em \_ GetHandle**](em-gethandle.md) e o texto retornado pela mensagem de [**\_ gettext do WM**](/windows/desktop/winmsg/wm-gettext) . Ele não tem nenhum efeito na exibição do texto dentro do controle de edição.

A mensagem em **\_ FMTLINES** não afeta uma linha que termina com uma quebra de linha rígida. Uma quebra de linha rígida consiste em um retorno de carro e um feed de linha.

> [!Note]  
> O tamanho do texto é alterado quando essa mensagem é processada.

 

**Edição avançada:** Não há suporte para a mensagem em **\_ FMTLINES** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ GEThandle**](em-gethandle.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 


---
title: Mensagem de EM_CHARFROMPOS (WinUser. h)
description: Obtém informações sobre o caractere mais próximo de um ponto especificado na área do cliente de um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- controles de Windows de mensagem de EM_CHARFROMPOS
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a133907b29857abdc1663d3283bc4b4164878f3fa0976769e6d42daef2c4cb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915956"
---
# <a name="em_charfrompos-message"></a>\_Mensagem em CHARFROMPOS

Obtém informações sobre o caractere mais próximo de um ponto especificado na área do cliente de um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

As coordenadas de um ponto na área do cliente do controle. As coordenadas estão em unidades de tela e são relativas ao canto superior esquerdo da área do cliente do controle.

**Controles de edição avançados:** Um ponteiro para uma estrutura [**pontual**](/previous-versions//dd162807(v=vs.85)) que contém as coordenadas horizontais e verticais.

**Controles de edição:** O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém a coordenada horizontal. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém a coordenada vertical.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**Controles de edição avançados:** O valor de retorno especifica o índice de caracteres com base em zero do caractere mais próximo ao ponto especificado. O valor de retorno indica o último caractere no controle de edição se o ponto especificado estiver além do último caractere no controle.

**Controles de edição:** O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o índice de base zero do caractere mais próximo ao ponto especificado. Esse índice é relativo ao início do controle, não ao início da linha. Se o ponto especificado estiver além do último caractere no controle de edição, o valor de retorno indicará o último caractere no controle. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o índice de base zero da linha que contém o caractere. Para controles de edição de linha única, esse valor é zero. O índice indica o delimitador de linha se o ponto especificado estiver além do último caractere visível em uma linha.

## <a name="remarks"></a>Comentários

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

Se um ponto for passado para **em \_ CHARFROMPOS** como o *lParam* e o ponto estiver fora dos limites do controle de edição, o *LRESULT* será (65535, 65535).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ POSFROMCHAR**](em-posfromchar.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**PONTO**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 


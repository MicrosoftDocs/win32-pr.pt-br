---
title: Mensagem de EM_GETWORDBREAKPROC (WinUser. h)
description: Obtém o endereço da função WordWrap atual. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- Controles de EM_GETWORDBREAKPROC de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb9499492668abac24774b66304ae8a87a2d739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455610"
---
# <a name="em_getwordbreakproc-message"></a>\_Mensagem em GETWORDBREAKPROC

Obtém o endereço da função WordWrap atual. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno especifica o endereço da função WordWrap definida pelo aplicativo. O valor de retorno será **nulo** se não existir nenhuma função WordWrap.

## <a name="remarks"></a>Comentários

Uma função WordWrap examina um buffer de texto que contém o texto a ser enviado para a exibição, procurando a primeira palavra que não caiba na linha de exibição atual. A função WordWrap coloca essa palavra no início da próxima linha na exibição. Uma função WordWrap define o ponto no qual o sistema deve quebrar uma linha de texto para controles de edição de várias linhas, geralmente com um caractere de espaço que separa duas palavras.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

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

[*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**em \_ FMTLINES**](em-fmtlines.md)
</dt> <dt>

[**em \_ SETWORDBREAKPROC**](em-setwordbreakproc.md)
</dt> </dl>

 


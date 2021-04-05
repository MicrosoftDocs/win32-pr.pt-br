---
title: Mensagem de EM_LINEINDEX (WinUser. h)
description: Obtém o índice de caracteres do primeiro caractere de uma linha especificada em um controle de edição de várias linhas.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Controles de EM_LINEINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_LINEINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611d4ff892f95287c45166ae55ff2389f454512c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918282"
---
# <a name="em_lineindex-message-winuserh"></a>Mensagem de EM_LINEINDEX (WinUser. h)

Obtém o índice de caracteres do primeiro caractere de uma linha especificada em um controle de edição de várias linhas. Um índice de caracteres é o índice de base zero do caractere do início do controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de linha com base em zero. Um valor de-1 especifica o número de linha atual (a linha que contém o cursor).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o índice de caracteres da linha especificada no parâmetro *wParam* ou é-1 se o número de linha especificado for maior que o número de linhas no controle de edição.

## <a name="remarks"></a>Comentários

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ LINEFROMCHAR**](em-linefromchar.md)
</dt> </dl>

 

 






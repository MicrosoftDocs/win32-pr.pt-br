---
title: Mensagem de EM_LINEFROMCHAR (WinUser. h)
description: Obtém o índice da linha que contém o índice de caracteres especificado em um controle de edição de várias linhas.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Controles de EM_LINEFROMCHAR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0dfe0c6c2ed0f9d77817fddde75fa18b64d485f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085410"
---
# <a name="em_linefromchar-message"></a>\_Mensagem em LINEFROMCHAR

Obtém o índice da linha que contém o índice de caracteres especificado em um controle de edição de várias linhas. Um índice de caracteres é o índice de base zero do caractere do início do controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de caracteres do caractere contido na linha cujo número deve ser recuperado. Se esse parâmetro for-1, **em \_ LINEFROMCHAR** recuperará o número de linha da linha atual (a linha que contém o cursor) ou, se houver uma seleção, o número de linha da linha que contém o início da seleção.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o número de linha com base em zero da linha que contém o índice de caracteres especificado por *wParam*.

## <a name="remarks"></a>Comentários

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Se o índice de caracteres for maior que 64.000, use a mensagem em [**\_ EXLINEFROMCHAR**](em-exlinefromchar.md) . Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

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

[**em \_ EXLINEFROMCHAR**](em-exlinefromchar.md)
</dt> <dt>

[**em \_ LINEINDEX**](em-lineindex.md)
</dt> </dl>

 

 






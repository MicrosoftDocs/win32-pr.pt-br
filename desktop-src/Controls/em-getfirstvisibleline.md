---
title: Mensagem de EM_GETFIRSTVISIBLELINE (WinUser. h)
description: Obtém o índice de base zero da linha visível superior em um controle de edição de várias linhas. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- Controles de EM_GETFIRSTVISIBLELINE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499549"
---
# <a name="em_getfirstvisibleline-message"></a>\_Mensagem em GETFIRSTVISIBLELINE

Obtém o índice de base zero da linha visível superior em um controle de edição de várias linhas. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

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

O valor de retorno é o índice de base zero da linha visível superior em um controle de edição de várias linhas.

**Controles de edição:** Para controles de edição de linha única, o valor de retorno é o índice de base zero do primeiro caractere visível.

**Controles de edição avançados:** Para controles de edição Rich de linha única, o valor de retorno é zero.

## <a name="remarks"></a>Comentários

O número de linhas e o comprimento das linhas em um controle de edição dependem da largura do controle e da configuração de WordWrap atual.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



 

 






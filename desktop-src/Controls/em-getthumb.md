---
title: Mensagem de EM_GETTHUMB (WinUser. h)
description: Obtém a posição da caixa de rolagem (Thumb) na barra de rolagem vertical de um controle de edição de várias linhas. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 04bd0102-1652-405b-8c42-50e138abaf75
keywords:
- Controles de EM_GETTHUMB de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETTHUMB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6689c530794e11897f1f88a7d5864058d53aa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086033"
---
# <a name="em_getthumb-message"></a>\_Mensagem em GETthumb

Obtém a posição da caixa de rolagem (Thumb) na barra de rolagem vertical de um controle de edição de várias linhas. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

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

O valor de retorno é a posição da caixa de rolagem.

## <a name="remarks"></a>Comentários

**Edição avançada:** Com suporte no Microsoft rich edit 2,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



 

 






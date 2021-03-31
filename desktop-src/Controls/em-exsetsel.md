---
title: Mensagem de EM_EXSETSEL (RichEdit. h)
description: Seleciona um intervalo de caracteres ou objetos de Component Object Model (COM) em um controle de edição rico da Microsoft.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- Controles de EM_EXSETSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824532"
---
# <a name="em_exsetsel-message"></a>\_Mensagem em EXSETSEL

Seleciona um intervalo de caracteres ou objetos de Component Object Model (COM) em um controle de edição rico da Microsoft.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que especifica o intervalo de seleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é a seleção que realmente está definida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 






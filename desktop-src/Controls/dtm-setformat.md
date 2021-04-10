---
title: Mensagem de DTM_SETFORMAT (commctrl. h)
description: Define a exibição de um controle DTP (data e hora) com base em uma determinada cadeia de caracteres de formato. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetFormat de DateTime.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- Controles de DTM_SETFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17669ed2e1ed23e3b090b77701bbe05d23a5ccb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009569"
---
# <a name="dtm_setformat-message"></a>\_Mensagem DTM SETformat

Define a exibição de um controle DTP (data e hora) com base em uma determinada cadeia de caracteres de formato. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetFormat de DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [cadeia de caracteres de formato](date-and-time-picker-controls.md) terminada em zero que define a exibição desejada. Definir esse parâmetro como **NULL** redefinirá o controle para a cadeia de caracteres de formato padrão para o estilo atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

É aceitável incluir caracteres extras na cadeia de caracteres de formato para produzir uma exibição mais rica. No entanto, todos os caracteres não formatados devem ser colocados entre aspas simples. Por exemplo, a cadeia de caracteres de formato "' hoje é: ' hh ': ' M' ' s ddddMMMdd ', ' YYY ' produziria uma saída como" hoje é: 04:22:31 terça-feira, 23 de março, 1996 ".

> [!Note]  
> Um controle DTP controla as alterações de localidade quando está usando a cadeia de caracteres de formato padrão. Se você definir uma cadeia de caracteres de formato personalizado, ela não será atualizada em resposta às alterações de localidade.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DTM \_ SETFORMATW** (Unicode) e **DTM \_ setformaa** (ANSI)<br/>               |



 

 






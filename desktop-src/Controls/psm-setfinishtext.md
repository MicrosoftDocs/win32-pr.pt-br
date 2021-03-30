---
title: Mensagem de PSM_SETFINISHTEXT (Prsht. h)
description: Define o texto do botão concluir em um assistente, mostra e habilita o botão e oculta os botões Avançar e voltar. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ SetFinishText.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- Controles de PSM_SETFINISHTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644299"
---
# <a name="psm_setfinishtext-message"></a>Mensagem de PSM \_ SETFINISHTEXT

Define o texto do botão **concluir** em um assistente, mostra e habilita o botão e oculta os botões **Avançar** e **voltar** . Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para o novo texto do botão **concluir** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Por padrão, o botão **concluir** não tem um acelerador de teclado. Você pode criar um acelerador de teclado com essa mensagem incluindo um e comercial (&) na cadeia de texto que você atribui ao *lParam*. Por exemplo, "&concluir" define F como a tecla aceleradora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **PSM \_ SETFINISHTEXTW** (Unicode) e **PSM \_ SETFINISHTEXTA** (ANSI)<br/>    |



 

 






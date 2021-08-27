---
title: PSM_SETFINISHTEXT mensagem (Prsht.h)
description: Define o texto do botão Concluir em um assistente, mostra e habilita o botão e oculta os botões Próximo e Voltar. Você pode enviar essa mensagem explicitamente ou usando a \_ macro PropSheet SetFinishText.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- PSM_SETFINISHTEXT controles de Windows mensagem
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
ms.openlocfilehash: 5a08cafbeafeccb2235cb9b653f997aa8c60bd5fd21a3ccbc92e572fa5d3d0db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088556"
---
# <a name="psm_setfinishtext-message"></a>Mensagem \_ SETFINISHTEXT do PSM

Define o texto do **botão** Concluir em um assistente, mostra e habilita o botão e oculta os **botões Próximo** **e** Voltar. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ PropSheet SetFinishText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para o novo texto do **botão** Concluir.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Por padrão, o **botão** Concluir não tem um acelerador de teclado. Você pode criar um acelerador de teclado com essa mensagem incluindo um e ampersand (&) na cadeia de caracteres de texto que você atribui a *lParam*. Por exemplo, "&Concluir" define F como a tecla de acelerador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **PSM \_ SETFINISHTEXTW** (Unicode) e **PSM \_ SETFINISHTEXTA** (ANSI)<br/>    |



 

 






---
title: Mensagem de EM_GETSELTEXT (RichEdit. h)
description: Recupera o texto atualmente selecionado em um controle de edição rico.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- Controles de EM_GETSELTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde2c0677fa04ff6d7991bca56bad0c08a6f5ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824365"
---
# <a name="em_getseltext-message"></a>\_Mensagem em GETSELTEXT

Recupera o texto atualmente selecionado em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um buffer que recebe o texto selecionado. O aplicativo de chamada deve garantir que o buffer seja grande o suficiente para manter o texto selecionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna o número de caracteres copiados, não incluindo o caractere nulo de terminação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 






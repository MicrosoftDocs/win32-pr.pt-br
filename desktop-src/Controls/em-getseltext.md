---
title: EM_GETSELTEXT mensagem (Richedit.h)
description: Recupera o texto selecionado no momento em um controle de edição rico.
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- EM_GETSELTEXT controles de Windows mensagem
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
ms.openlocfilehash: 540567f1b52c936ad085acac8e0374fdb0a912bae06480632263f9676f2948e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019494"
---
# <a name="em_getseltext-message"></a>Mensagem EM \_ GETSELTEXT

Recupera o texto selecionado no momento em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um buffer que recebe o texto selecionado. O aplicativo de chamada deve garantir que o buffer seja grande o suficiente para manter o texto selecionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem retorna o número de caracteres copiados, não incluindo o caractere nulo de terminação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 






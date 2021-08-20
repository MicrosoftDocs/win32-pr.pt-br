---
title: Mensagem de EM_GETTEXTRANGE (RichEdit. h)
description: Recupera um intervalo de caracteres especificado de um controle de edição rico.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- controles de Windows de mensagem de EM_GETTEXTRANGE
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12282b970c38164e5b28a31ed778a3320f88bbdf16b6d182586e492e5e699eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006571"
---
# <a name="em_gettextrange-message"></a>\_Mensagem em GETtextrange

Recupera um intervalo de caracteres especificado de um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) que especifica o intervalo de caracteres a serem recuperados e um buffer no qual os caracteres são copiados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A mensagem retorna o número de caracteres copiados, não incluindo o caractere nulo de terminação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 






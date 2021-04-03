---
title: Mensagem de EM_GETTEXTRANGE (RichEdit. h)
description: Recupera um intervalo de caracteres especificado de um controle de edição rico.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- Controles de EM_GETTEXTRANGE de mensagens do Windows
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
ms.openlocfilehash: d68c4089bbe2cc09daa39d69e9094a4abaead787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918882"
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

## <a name="return-value"></a>Retornar valor

A mensagem retorna o número de caracteres copiados, não incluindo o caractere nulo de terminação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 






---
title: EM_GETSCROLLPOS mensagem (Richedit.h)
description: Obtém a posição de rolagem atual do controle de edição.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- EM_GETSCROLLPOS controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42bde137096ae3c13582017f91b82c1eb9100097bb76f0d1babb91fa47b52196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800026"
---
# <a name="em_getscrollpos-message"></a>Mensagem \_ EM GETSCROLLPOS

Obtém a posição de rolagem atual do controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura POINT.**](/previous-versions//dd162805(v=vs.85)) Depois de **chamar EM \_ GETSCROLLPOS**, esses parâmetros contêm um ponto no espaço de texto virtual do documento, expresso em pixels. Esse ponto será o ponto localizado atualmente no canto superior esquerdo da janela de controle de edição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem sempre retorna 1.

## <a name="remarks"></a>Comentários

Os valores retornados na [**estrutura POINT**](/previous-versions//dd162805(v=vs.85)) são valores de 16 bits (mesmo nos campos de 32 bits de largura).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Redistribuível<br/>          | Rich Edit 3.0<br/>                                                              |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ SETSCROLLPOS**](em-setscrollpos.md)
</dt> </dl>

 


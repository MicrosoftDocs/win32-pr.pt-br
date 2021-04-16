---
title: Mensagem de EM_GETSCROLLPOS (RichEdit. h)
description: Obtém a posição de rolagem atual do controle de edição.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- Controles de EM_GETSCROLLPOS de mensagens do Windows
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
ms.openlocfilehash: 70458abca94e483f8e202f13ecaed3df04a68366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455069"
---
# <a name="em_getscrollpos-message"></a>\_Mensagem em GETSCROLLPOS

Obtém a posição de rolagem atual do controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) . Depois de chamar em **\_ GETSCROLLPOS**, esses parâmetros contêm um ponto no espaço de texto virtual do documento, expresso em pixels. Esse ponto será o ponto localizado atualmente no canto superior esquerdo da janela de controle de edição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem sempre retorna 1.

## <a name="remarks"></a>Comentários

Os valores retornados na estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) são valores de 16 bits (mesmo nos campos de largura de 32 bits).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| Redistribuível<br/>          | Edição avançada 3,0<br/>                                                              |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SETSCROLLPOS**](em-setscrollpos.md)
</dt> </dl>

 


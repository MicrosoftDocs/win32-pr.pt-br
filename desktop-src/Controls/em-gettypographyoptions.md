---
title: Mensagem de EM_GETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Retorna o estado atual das opções de tipografia de um controle de edição rico.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- controles de Windows de mensagem de EM_GETTYPOGRAPHYOPTIONS
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d575550e2c239ee5b689deb5874a9803c581151b54100ab227a24d4f29941973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831159"
---
# <a name="em_gettypographyoptions-message"></a>\_Mensagem em GETtipografiaoptions

Retorna o estado atual das opções de tipografia de um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna as opções de tipografia atuais. Para obter uma lista de opções, consulte em [**\_ settypographyoptions**](em-settypographyoptions.md).

## <a name="remarks"></a>Comentários

Você pode ativar a quebra de linha avançada enviando a mensagem em [**\_ settipografiaoptions**](em-settypographyoptions.md) . A quebra de linha avançada e normal também pode ser ativada automaticamente pelo controle de edição avançada se for necessário para determinados idiomas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Redistribuível<br/>          | Edição avançada 3,0<br/>                                                              |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ SETtipografiaoptions**](em-settypographyoptions.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Sobre os controles de edição avançados](about-rich-edit-controls.md)
</dt> </dl>

 

 






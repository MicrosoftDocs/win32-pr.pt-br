---
title: Mensagem de EM_GETAUTOURLDETECT (RichEdit. h)
description: Indica se a detecção automática de URL está ativada no controle rich edit.
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- Controles de EM_GETAUTOURLDETECT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009453"
---
# <a name="em_getautourldetect-message"></a>\_Mensagem em GETAUTOURLDETECT

Indica se a detecção automática de URL está ativada no controle rich edit.

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

## <a name="return-value"></a>Retornar valor

Se a detecção de URL automática estiver ativa, o valor de retorno será 1.

Se a detecção de URL automática estiver inativa, o valor de retorno será 0.

## <a name="remarks"></a>Comentários

Quando a detecção automática de URL está ativada, a edição rica da Microsoft está verificando constantemente o texto digitado em busca de uma URL válida. O Rich Edit reconhece URLs que começam com estes prefixos:

-   http:
-   file:
-   mailto:
-   FTP
-   https
-   Gopher
-   NNTP
-   prospero:
-   estabelecer
-   Notícias
-   WAIS
-   Outlook

A edição avançada também reconhece nomes de caminho padrão que começam com \\ \\ . Quando a edição avançada localiza uma URL, ela altera a cor do texto da URL, sublinha o texto e notifica o cliente usando o [ \_ link en](en-link.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[\_link para](en-link.md)
</dt> </dl>

 

 






---
title: Mensagens comunicadas por meio de interfaces do usuário
description: Este tópico lista as mensagens que um serviço de diretório pode enviar de uma interface do usuário.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Mensagens comunicadas por meio de interfaces do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab0d01717129db284f05b2361b2a067d611a33e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004912"
---
# <a name="messages-communicated-through-user-interfaces"></a>Mensagens comunicadas por meio de interfaces do usuário

Este tópico lista as mensagens que um serviço de diretório pode enviar de uma interface do usuário.

## <a name="common-query-page-messages"></a>Mensagens comuns da página de consulta

As seguintes mensagens são enviadas para uma página de extensão do formulário de consulta do serviço de diretório na função de retorno de chamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) :

-   [**CQPM \_ CLEARFORM**](cqpm-clearform.md)
-   [**CQPM \_ habilitar**](cqpm-enable.md)
-   [**\_Parameters CQPM**](cqpm-getparameters.md)
-   [**CQPM \_ HANDLERSPECIFIC**](cqpm-handlerspecific.md)
-   [**ajuda do CQPM \_**](cqpm-help.md)
-   [**CQPM \_ inicializar**](cqpm-initialize.md)
-   [**CQPM \_ persistir**](cqpm-persist.md)
-   [**\_versão CQPM**](cqpm-release.md)
-   [**CQPM \_ SETpadrãoparameters**](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a>Mensagens diversas

A tabela a seguir lista as mensagens que um serviço de diretório pode enviar.



| Mensagem                  | Valor                     | Descrição                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DSPROP \_ ATTRCHANGED \_ msg | "DsPropAttrChanged"       | Uma mensagem enviada para sincronizar páginas de propriedades e as ferramentas de administração do serviço de diretório, declarada em DSClient. h.                                                                                                                       |
| DSQPM \_ GETclasslist      | CQPM \_ HANDLERSPECIFIC + 0   | Uma mensagem de página enviada para as páginas de formulário para recuperar uma lista de classes para consulta, usada pelo seletor de campo e Propriedade bem para criar sua lista de classes de exibição. wParam = flags e lParam = LPLPDSQUERYCLASSLIST, declarados em DSQuery. h. |
| DSQPM \_ HELPTOPICS        | (CQPM \_ HANDLERSPECIFIC + 1) | Uma mensagem de página enviada para as páginas de formulário para manipular a solicitação "tópicos da ajuda". wParam = 0, lParam = hWndParent, declarado em DSQuery. h.                                                                                                         |



 

 

 





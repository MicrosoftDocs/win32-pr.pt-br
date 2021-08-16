---
title: Mensagens comunicadas por meio de interfaces do usuário
description: Este tópico lista as mensagens que um serviço de diretório pode enviar de uma interface do usuário.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Mensagens comunicadas por meio de interfaces do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b20b2706ae9f03109064c459ce494fb38da3f4579ca8f5b03ade970fcb0391f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186568"
---
# <a name="messages-communicated-through-user-interfaces"></a>Mensagens comunicadas por meio de interfaces do usuário

Este tópico lista as mensagens que um serviço de diretório pode enviar de uma interface do usuário.

## <a name="common-query-page-messages"></a>Mensagens de página de consulta comuns

As seguintes mensagens são enviadas para uma página de extensão de formulário de consulta de serviço de diretório na função de retorno de chamada [**CQPageProc:**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)

-   [**CQPM \_ CLEARFORM**](cqpm-clearform.md)
-   [**CQPM \_ ENABLE**](cqpm-enable.md)
-   [**GETPARAMETERS DO CQPM \_**](cqpm-getparameters.md)
-   [**MANIPULADOR \_ CQPMSPECIFIC**](cqpm-handlerspecific.md)
-   [**AJUDA DO \_ CQPM**](cqpm-help.md)
-   [**INICIALIZAÇÃO DO \_ CQPM**](cqpm-initialize.md)
-   [**CQPM \_ PERSIST**](cqpm-persist.md)
-   [**VERSÃO DO \_ CQPM**](cqpm-release.md)
-   [**CQPM \_ SETDEFAULTPARAMETERS**](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a>Mensagens diversas

A tabela a seguir lista as mensagens que um serviço de diretório pode enviar.



| Mensagem                  | Valor                     | Descrição                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DSPROP \_ ATTRCHANGED \_ MSG | "DsPropAttrChanged"       | Uma mensagem enviada para sincronizar páginas de propriedades e as ferramentas de administração de serviço de diretório, declaradas em Dsclient.h.                                                                                                                       |
| GETCLASSLIST do DSQPM \_      | MANIPULADOR \_ CQPMSPECIFIC+0   | Uma mensagem de página enviada às páginas de formulário para recuperar uma lista de classes para consulta, usada pelo seletor de campo e pela propriedade well para criar sua lista de classes de exibição. wParam = flags e lParam = LPLPDSQUERYCLASSLIST, declarado em Dsquery.h. |
| DSQPM \_ HELPTOPICS        | (CQPM \_ HANDLERSPECIFIC+1) | Uma mensagem de página enviada para as páginas de formulário para lidar com a solicitação "Tópicos da Ajuda". wParam = 0, lParam = hWndParent, declarado em Dsquery.h.                                                                                                         |



 

 

 





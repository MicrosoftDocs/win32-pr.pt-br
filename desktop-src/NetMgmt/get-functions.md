---
title: Obter funções
description: As funções Get de gerenciamento de rede recuperam informações sobre um domínio. Você também pode chamar essas funções para recuperar informações sobre contas de usuário locais, globais, de estação de trabalho e de servidor.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498732"
---
# <a name="get-functions"></a>Obter funções

As funções Get de gerenciamento de rede recuperam informações sobre um domínio. Você também pode chamar essas funções para recuperar informações sobre contas de usuário locais, globais, de estação de trabalho e de servidor.

As funções Get de gerenciamento de rede são listadas a seguir.



| Função                                                               | Descrição                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetGetAnyDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Retorna o nome de qualquer controlador de domínio para um domínio que é diretamente confiável para um servidor especificado.                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Retorna o nome do controlador de domínio primário (PDC) para o domínio especificado.                                                        |
| [**NetGetDisplayInformationIndex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Retorna o índice da primeira entrada de informações de exibição cujo nome começa com uma cadeia de caracteres especificada ou segue em ordem alfabética a cadeia de caracteres. |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Retorna informações de conta de usuário, computador ou grupo global.                                                                             |



 

As informações retornadas pela função [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) estão disponíveis nos seguintes níveis:

-   [**\_grupo de exibição NET \_**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [**\_computador de exibição NET \_**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [**NET \_ Display \_ usuário**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 





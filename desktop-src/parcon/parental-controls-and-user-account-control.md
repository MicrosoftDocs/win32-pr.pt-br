---
description: Controles dos pais e controle de conta de usuário
ms.assetid: dc7c322a-f534-4dda-8c62-aa628a7b91bc
title: Controles dos pais e controle de conta de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7798661a7cadc4d497791925c83cdfa684b252a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771327"
---
# <a name="parental-controls-and-user-account-control"></a>Controles dos pais e controle de conta de usuário

O UAC (controle de conta de usuário) resultará na presença de contas de usuário padrão e de administrador protegido. Um administrador protegido será executado com os mesmos direitos que um usuário padrão em uso normal. Para operações privilegiadas:

-   Um usuário padrão será mostrado na caixa de diálogo credenciais da interface do usuário, que requer a entrada de um nome de usuário e senha para um administrador protegido ou administrador interno.
-   Um administrador protegido será mostrado na caixa de diálogo interface do usuário de consentimento, que requer a seleção de permitir para continuar.

É importante observar que o UAC é implementado por processo, de modo que um processo seja executado com privilégios elevados ou não. Em geral, ele não é adequado de um ponto de vista de segurança para executar aplicativos grandes como sempre elevado. Para controles dos pais, o código que deve modificar as configurações deve ser isolado por uma das duas opções de implementação:

1.  Crie um pequeno executável para o gerenciamento de configurações que está marcado em seu manifesto, exigindo direitos administrativos. A invocação do executável fará com que a interface do usuário de consentimento ou credenciais seja exibida antes de permitir que o processo seja executado.
2.  Forneça interfaces COM em uma DLL de produto que permita invocação por documentação do UAC. Isso também fará com que a interface do usuário de credenciais ou consentimento apropriado seja mostrada.

 

 




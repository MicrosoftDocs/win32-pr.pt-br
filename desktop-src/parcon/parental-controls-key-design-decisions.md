---
description: Os pais controlam as principais decisões de design
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Os pais controlam as principais decisões de design
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39cb4be775a3380cb9fe7aa677362df31a2dc453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011736"
---
# <a name="parental-controls-key-design-decisions"></a>Os pais controlam as principais decisões de design

As principais decisões de design no desenvolvimento de controles dos pais do Windows Vista são:

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a>Dependência essencial no recurso UAC (controle de conta de usuário) do Windows Vista

Uma decisão importante para os controles dos pais do Windows Vista é contar com o novo recurso UAC (controle de conta de usuário) para implementar as identidades de conta de direitos reduzidas especialmente necessárias para restrições offline em usuários controlados. Para obter mais informações sobre o UAC, consulte [a história do desenvolvedor do Windows Vista e do Windows Server 2008: requisitos de desenvolvimento de aplicativos do Windows Vista para UAC (controle de conta de usuário)](/previous-versions/aa905330(v=msdn.10)). Em resumo, cada conta com direitos de administrador efetivamente tem privilégios para executar a função pai ou de guardião de exibir dados de log e definir políticas. Os controles dos pais só podem ser definidos em usuários com direitos padrão (chamados anteriormente de contas de usuário com privilégios mínimos ou LUAs), pois apenas eles não podem alterar logs e configurações com ACLs (listas de controle de acesso) configuradas somente para os administradores gravarem. Em outras palavras:

-   Uma identidade pai ou guardião é implicitamente igual a uma conta que tem direitos de um administrador.
-   Os usuários controlados de forma responsável devem ser usuários padrão.

## <a name="nearly-all-settings-are-available-by-apis"></a>Quase todas as configurações estão disponíveis por APIs

Com exceção de itens como definições do sistema de classificação, as configurações disponíveis para manipulação pela interface do usuário de controles pais também podem ser modificadas por APIs expostas. É necessário que os programas implementem a elevação a direitos administrativos a fim de alterar as configurações, conforme observado acima para o UAC.

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a>Os controles dos pais do Windows Vista são uma tecnologia somente para consumidores

Os controles dos pais do Windows Vista não se destinam a serem usados com contas de domínio. Como uma tecnologia de consumidor, os controles dos pais não são implantados em SKUs comerciais do Windows Vista. Se um computador tiver ingressado em um domínio, os links da interface do usuário de segurança da família serão suprimidos.

Um mecanismo será fornecido para expor a funcionalidade para o caso ingressado no domínio, mas somente contas de usuário que não sejam de domínio poderão ser configuradas com controles dos pais.

 

 

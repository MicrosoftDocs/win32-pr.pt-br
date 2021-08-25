---
description: Decisões de design de chave dos controles dos pais
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Decisões de design de chave dos controles dos pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fef8f1e1d1b629c9fbb4354fb266376453938a35bde80e7b60f57be8f77da70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939286"
---
# <a name="parental-controls-key-design-decisions"></a>Decisões de design de chave dos controles dos pais

As principais decisões de design no desenvolvimento de controles Windows Pais do Vista são:

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a>Dependência essencial do Windows UAC (Controle de Conta de Usuário) do Vista

Uma decisão importante para Windows Vista Parent Controls é contar com o novo recurso UAC (Controle de Conta de Usuário) para implementar as identidades de conta de direitos reduzidas especialmente necessárias para restrições offline em usuários controlados. Para obter mais informações sobre o UAC, consulte The Windows Vista and [Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC).](/previous-versions/aa905330(v=msdn.10)) Em resumo, cada conta com direitos de administrador efetivamente tem privilégios para executar a função pai ou guardião de exibir dados de log e definir políticas. Os controles dos pais só podem ser definidos em usuários com direitos padrão (anteriormente chamados de Contas de Usuário com privilégios mínimos ou LUAs), pois apenas eles não podem alterar logs e configurações com ACLs (Listas de Controle de Acesso) configuradas apenas para os administradores gravarem. Em outras palavras:

-   Uma identidade pai ou guardião é implicitamente igual a uma conta que tem direitos de administrador.
-   Os usuários controlados pelos pais devem ser usuários padrão.

## <a name="nearly-all-settings-are-available-by-apis"></a>Quase todas as Configurações estão disponíveis por APIs

Com exceção de itens como definições do sistema de classificações, as configurações disponíveis para manipulação pelos controles dos pais Interface do Usuário também podem ser modificadas por APIs expostas. É necessário que os programas implementem a elevação a direitos administrativos para alterar as configurações, conforme mencionado acima para o UAC.

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a>Windows Os controles dos pais do Vista são uma tecnologia somente para o consumidor

Windows Os Controles parentais do Vista não devem ser usados com contas de domínio. Como uma tecnologia de consumidor, os Controles dos Pais não são implantados em SKUs de negócios do Windows Vista. Se um computador estiver ingressado em um domínio, os links da interface do usuário do Family Safety serão suprimidos.

Um mecanismo será fornecido para expor a funcionalidade para o caso ingressado no domínio, mas somente contas de usuário que não são de domínio podem ser configuradas com controles dos pais.

 

 

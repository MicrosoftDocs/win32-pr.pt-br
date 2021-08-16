---
description: Para recuperar dados do Registro, um aplicativo normalmente enumera as sub-chaves de uma chave até encontrar uma determinada e, em seguida, recupera dados do valor ou valores associados a ela.
ms.assetid: ce4be388-5506-4d01-a73c-33372ef4ccd7
title: Recuperando dados do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bedbe0631015188a8a9fe280ba17d929c83663e995f440f4528c0913fc69cb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763475"
---
# <a name="retrieving-data-from-the-registry"></a>Recuperando dados do Registro

Para recuperar dados do Registro, um aplicativo normalmente enumera as sub-chaves de uma chave até encontrar uma determinada e, em seguida, recupera dados do valor ou valores associados a ela. Um aplicativo pode chamar a [**função RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa) para enumerar as sub-chaves de uma determinada chave.

Para recuperar dados detalhados sobre uma sub-chave específica, um aplicativo pode chamar a [**função RegQueryInfoKey.**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya) A [**função RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity) recupera uma cópia do descritor de segurança que protege uma chave.

Um aplicativo pode usar a [**função RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) para enumerar os valores de uma determinada chave e a função [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) para recuperar um valor específico para uma chave. Um aplicativo normalmente chama **RegEnumValue** para determinar os nomes de valor e **RegQueryValueEx** para recuperar os dados dos nomes.

A [**função RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa) recupera o tipo e os dados de uma lista de nomes de valor associados a uma chave aberta do Registro. Essa função é útil para provedores de chave dinâmica porque garante a consistência dos dados recuperando vários valores em uma operação atômica.

Como outros aplicativos podem alterar os dados em um valor do Registro entre o momento em que seu aplicativo pode ler um valor e usá-lo, talvez seja necessário garantir que seu aplicativo tenha os dados mais recentes. Você pode usar a função [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) para notificar o thread de chamada quando houver alterações nos atributos ou conteúdo de uma chave do Registro ou se a chave for excluída. A função sinaliza um objeto de evento para notificar o chamador. Se o thread que chama **RegNotifyChangeKeyValue** sair, o evento será sinalizado e o monitoramento da chave do Registro será interrompido.

Você pode controlar ou especificar quais alterações devem ser relatadas por meio do uso de um filtro ou sinalizador de notificação. Normalmente, as alterações são relatadas sinalizando um evento que você especifica para a função. Observe que a [**função RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) não funciona com alças remotas.

Para monitorar as operações do Registro mais detalhadamente, consulte [**Registro**](/windows/desktop/ETW/registry).

 

 

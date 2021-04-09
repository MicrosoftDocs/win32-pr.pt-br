---
description: Para recuperar dados do registro, um aplicativo normalmente enumera as subchaves de uma chave até encontrar uma específica e, em seguida, recupera os dados do valor ou valores associados a ela.
ms.assetid: ce4be388-5506-4d01-a73c-33372ef4ccd7
title: Recuperando dados do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d8dd6f6e4d667cf2760c7cba441200755fb6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011666"
---
# <a name="retrieving-data-from-the-registry"></a>Recuperando dados do registro

Para recuperar dados do registro, um aplicativo normalmente enumera as subchaves de uma chave até encontrar uma específica e, em seguida, recupera os dados do valor ou valores associados a ela. Um aplicativo pode chamar a função [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa) para enumerar as subchaves de uma determinada chave.

Para recuperar dados detalhados sobre uma determinada subchave, um aplicativo pode chamar a função [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya) . A função [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity) recupera uma cópia do descritor de segurança protegendo uma chave.

Um aplicativo pode usar a função [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) para enumerar os valores de uma determinada chave e a função [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) para recuperar um valor específico para uma chave. Um aplicativo normalmente chama **RegEnumValue** para determinar os nomes de valor e, em seguida, **RegQueryValueEx** para recuperar os dados para os nomes.

A função [**RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa) recupera o tipo e os dados para uma lista de nomes de valores associados a uma chave de registro aberta. Essa função é útil para provedores de chaves dinâmicas porque garante a consistência dos dados recuperando vários valores em uma operação atômica.

Como outros aplicativos podem alterar os dados em um valor de registro entre o momento em que o aplicativo pode ler um valor e usá-lo, talvez seja necessário garantir que seu aplicativo tenha os dados mais recentes. Você pode usar a função [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) para notificar o thread de chamada quando houver alterações nos atributos ou no conteúdo de uma chave do registro ou se a chave for excluída. A função sinaliza um objeto de evento para notificar o chamador. Se o thread que chama **RegNotifyChangeKeyValue** for encerrado, o evento será sinalizado e o monitoramento da chave do registro será interrompido.

Você pode controlar ou especificar quais alterações devem ser relatadas por meio do uso de um filtro ou sinalizador de notificação. Normalmente, as alterações são relatadas sinalizando um evento que você especifica para a função. Observe que a função [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) não funciona com identificadores remotos.

Para monitorar as operações de registro mais detalhadamente, consulte [**registro**](/windows/desktop/ETW/registry).

 

 

---
description: Quando o Winlogon é inicializado, ele registra a SAS (sequência de atenção segura) CTRL+ALT+DEL com o sistema e, em seguida, cria três áreas de trabalho dentro da estação de janela WinSta0.
ms.assetid: 874aa12b-e213-4857-9600-698c28dfda37
title: Inicializando o Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fff33740b77b23577cd7749b8cc745cd06a55e18675e35b817e405a71679b482
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482388"
---
# <a name="initializing-winlogon"></a>Inicializando o Winlogon

Quando [o Winlogon](winlogon.md) é inicializado, ele registra a SAS [*(sequência*](../secgloss/s-gly.md) de atenção segura) CTRL+ALT+DEL com o sistema e, em seguida, cria três áreas de trabalho dentro da estação de janela WinSta0.

Registrar CTRL+ALT+DEL torna essa inicialização o primeiro processo, garantindo assim que nenhum outro aplicativo tenha conectado essa sequência de chaves.

WinSta0 é o nome do objeto da estação de janela que representa a tela física, o teclado e o mouse. O Winlogon cria as áreas de trabalho a seguir no objeto WinSta0.



| Desktop              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Área de trabalho do Winlogon     | Essa é a área de trabalho usada pelo Winlogon e [*PELOL para*](../secgloss/g-gly.md) identificação interativa e autenticação e outras caixas de diálogo seguras. O Winlogon alterna automaticamente para essa área de trabalho quando recebe uma notificação de evento SAS.                                                                                                                                                                                                                                                                                                                                                                          |
| Área de trabalho do aplicativo  | Sempre que um usuário faz logon com êxito, uma área de trabalho do aplicativo é criada para essa sessão [*de logon.*](../secgloss/l-gly.md) A área de trabalho do aplicativo também é conhecida como a área de trabalho padrão ou de usuário. É nessa área de trabalho que ocorre toda a atividade do usuário. A área de trabalho do aplicativo está protegida; somente o sistema e a sessão de logon interativo têm acesso a ele. Observe que apenas uma instância específica do usuário conectado tem acesso à área de trabalho. Se o usuário interativo ativar um processo usando o controlador de serviço, esse aplicativo de serviço não terá acesso à área de trabalho do aplicativo. |
| Área de trabalho de economia de tela | Essa é a área de trabalho atual quando uma economia de tela está em execução. Se um usuário estiver conectado, o sistema e a sessão de logon interativo terão acesso à área de trabalho. Caso contrário, somente o sistema terá acesso à área de trabalho.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Como o proprietário dessas áreas de trabalho, o Winlogon pode alternar a área de trabalho atual ou visível para qualquer uma das três áreas de trabalho e permitir o acesso DELP a essa funcionalidade. Em geral, os desenvolvedores de SEMPRE não alterarão a área de trabalho atual porque o Winlogon define a área de trabalho adequadamente antes de se comunicar com o LTD. A descrição de cada função DEM indica qual área de trabalho é atual para essa chamada.



| Para obter informações sobre                                    | Consulte                                                                                                      |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Os diferentes estados nos quais o Winlogon pode ser executado           | [Estados do Winlogon](winlogon-states.md)                                                                   |
| Operações de tempo-out                                      | [Operações de tempo-out do serviço caixa de diálogo com suporte](supported-dialog-box-service-time-out-operations.md) |
| Enviar mensagens para o VISOR enquanto uma caixa de diálogo é exibida | [Enviando mensagens para o LTD](sending-messages-to-the-gina.md)                                         |
| Funções de suporte                                        | [Funções de suporte do Winlogon](authentication-functions.md)                    |



 

 

 

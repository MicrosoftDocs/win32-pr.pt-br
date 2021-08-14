---
description: O Winlogon, a GINA e os provedores de rede são as partes do modelo de logon interativo.
ms.assetid: d049d83f-b962-4c47-a79a-da556831e319
title: Winlogon e GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cc39b905d6a49eb84ccab164f99481561133e6cdd9ea40cfd0b1067315569a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915065"
---
# <a name="winlogon-and-gina"></a>Winlogon e GINA

O [*Winlogon*](../secgloss/w-gly.md), a [*Gina*](../secgloss/g-gly.md)e os provedores de rede são as partes do modelo de logon interativo. O procedimento de logon interativo normalmente é controlado por Winlogon, MSGina.dll e provedores de rede. Para alterar o procedimento de logon interativo, MSGina.dll pode ser substituído por uma DLL GINA personalizada.

para trabalhar com o Winlogon, a GINA e os provedores de rede, você deve ter conhecimento da arquitetura de segurança Windows, especialmente em relação a [*tokens*](../secgloss/a-gly.md), [*pacotes de autenticação*](../secgloss/a-gly.md)e assuntos relacionados.

> [!Note]  
> as DLLs ginas são ignoradas no Windows Vista.

 

Para obter informações sobre funções e estruturas específicas, consulte [referência de autenticação](authentication-reference.md). Esta seção de referência inclui descrições das funções que uma DLL GINA deve implementar, as funções de suporte do Winlogon que a DLL GINA pode chamar e as estruturas de dados usadas para passar informações entre o Winlogon e a GINA.

O código de GINA de exemplo pode ser encontrado nos exemplos de segurança do SDK (Software Development Kit) da plataforma. Os exemplos contêm código C para implementar um stub GINA e um gancho GINA. Para obter mais informações sobre o desenvolvimento de DLL de GINA personalizada, envie uma mensagem de email para: ginareqs@microsoft.com .

para obter informações sobre o modelo de autenticação com suporte pelo Windows e para obter detalhes sobre os serviços da [*autoridade de segurança Local*](../secgloss/l-gly.md) (LSA) e as interfaces do [*pacote de autenticação*](../secgloss/a-gly.md) , consulte [autenticação LSA](lsa-authentication.md).

Para obter informações sobre os aspectos da autoridade de segurança local relacionada à administração da política de segurança, que inclui relações de confiança com outros computadores e domínios, atribuição de privilégios, controle de geração de auditoria, acessibilidade do sistema e outros tópicos semelhantes, consulte [política de LSA](../secmgmt/lsa-policy.md).

Para obter informações sobre Winlogon e GINA, consulte os tópicos a seguir.



| Tópico                                                                              | Descrição                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Winlogon](winlogon.md)                                                           | O Winlogon fornece um conjunto de funções de suporte para a DLL GINA.<br/>                                                                                                                                                                 |
| [GINA](gina.md)                                                                   | Uma DLL GINA fornece procedimentos de autenticação e identificação de usuário personalizáveis.<br/>                                                                                                                                            |
| [Funções de GINA de serviços de terminal](terminal-services-gina-functions.md)           | Quando os serviços de terminal são habilitados, a GINA deve chamar funções de suporte do Winlogon para concluir várias tarefas.<br/>                                                                                                                   |
| [Interação com provedores de rede](interaction-with-network-providers.md)       | Você pode configurar um sistema para dar suporte a zero ou mais provedores de rede.<br/>                                                                                                                                                          |
| [Responsabilidades e recursos](responsibilities-and-features.md)                 | Cada parte do processo de logon interativo tem um conjunto de responsabilidades.<br/>                                                                                                                                                      |
| [Interação entre Winlogon e GINA](interaction-between-winlogon-and-gina.md) | O estado do Winlogon determina qual função GINA é chamada para processar qualquer evento de [*sequência de atenção segura*](../secgloss/s-gly.md) (SAS).<br/> |
| [Pacotes de notificação do Winlogon](winlogon-notification-packages.md)               | Você pode implementar um pacote de notificação para monitorar e responder a eventos do Winlogon.<br/>                                                                                                                                            |



 

 

 

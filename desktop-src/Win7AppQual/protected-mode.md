---
description: Modo protegido
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Modo protegido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2f16b9f923215af6c2211339859d8eab4803e6793be248a83760e298ed084c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994776"
---
# <a name="protected-mode"></a>Modo protegido

a maioria Windows recursos de segurança do internet explorer 8 estão disponíveis no Internet explorer 8 para o sistema operacional Windows XP com Service Pack 2 (SP2) e versões posteriores. o modo protegido está disponível somente para o Windows Vista ou versões posteriores porque ele se baseia nos seguintes recursos de segurança que são novos no Windows Vista:

-   O [UAC (controle de conta de usuário)](https://msdn.microsoft.com/library/aa511445.aspx) facilita a execução sem privilégios de administrador. Quando os usuários executam programas com privilégios de usuário limitados, eles são mais seguros de um ataque do que quando são executados com privilégios de administrador. o sistema operacional Windows pode restringir o código mal-intencionado de realizar ações perigosas.
-   Um mecanismo de integridade restringe o acesso de gravação a [objetos protegíveis](../secauthz/securable-objects.md) por processos de baixa integridade, da mesma maneira que a associação de grupo de contas de usuário restringe os direitos de usuários para acessar componentes confidenciais do sistema.
-   O [UIPI (isolamento de privilégios de interface do usuário)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) impede que processos enviem mensagens de janela selecionadas e outras APIs de usuário para processos que estão sendo executados com maior integridade.

a infra-estrutura de segurança do mecanismo de integridade Windows permite que o modo protegido forneça Windows Internet Explorer com os privilégios de que os usuários precisam para navegar na web, enquanto os privilégios de retenção que os usuários precisam para instalar programas silenciosamente ou modificar dados confidenciais do sistema.

Os usuários podem desabilitar esse recurso por meio de uma caixa de seleção e os administradores podem desabilitá-lo usando Política de Grupo.

> [!IMPORTANT]
> Você deve desabilitar o recurso somente como uma medida temporária durante a solução de problemas para comparar o comportamento do aplicativo quando o recurso estiver habilitado ou não. Recomendamos que você mantenha esse recurso permanentemente habilitado.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 

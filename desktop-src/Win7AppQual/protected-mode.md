---
description: Modo protegido
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Modo protegido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc1b8b1e6931ed83ec59ccfe4c3c63d8e5b5eed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116444"
---
# <a name="protected-mode"></a>Modo protegido

A maioria dos recursos de segurança do Windows Internet Explorer 8 está disponível no Internet Explorer 8 para o sistema operacional Windows XP com Service Pack 2 (SP2) e versões posteriores. O modo protegido está disponível apenas para o Windows Vista ou versões posteriores porque ele se baseia nos seguintes recursos de segurança que são novos no Windows Vista:

-   O [UAC (controle de conta de usuário)](https://msdn.microsoft.com/library/aa511445.aspx) facilita a execução sem privilégios de administrador. Quando os usuários executam programas com privilégios de usuário limitados, eles são mais seguros de um ataque do que quando são executados com privilégios de administrador. O sistema operacional Windows pode restringir o código mal-intencionado de realizar ações perigosas.
-   Um mecanismo de integridade restringe o acesso de gravação a [objetos protegíveis](../secauthz/securable-objects.md) por processos de baixa integridade, da mesma maneira que a associação de grupo de contas de usuário restringe os direitos de usuários para acessar componentes confidenciais do sistema.
-   O [UIPI (isolamento de privilégios de interface do usuário)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) impede que processos enviem mensagens de janela selecionadas e outras APIs de usuário para processos que estão sendo executados com maior integridade.

A infraestrutura de segurança do mecanismo de integridade do Windows permite que o modo protegido forneça ao Windows Internet Explorer os privilégios de que os usuários precisam para navegar na Web, enquanto os privilégios de retenção dos usuários precisam instalar programas silenciosamente ou modificar dados confidenciais do sistema.

Os usuários podem desabilitar esse recurso por meio de uma caixa de seleção e os administradores podem desabilitá-lo usando Política de Grupo.

> [!IMPORTANT]
> Você deve desabilitar o recurso somente como uma medida temporária durante a solução de problemas para comparar o comportamento do aplicativo quando o recurso estiver habilitado ou não. Recomendamos que você mantenha esse recurso permanentemente habilitado.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 

---
description: Usar corretamente a política de restrição de software pode tornar sua empresa mais ágil porque fornece uma estrutura proativa para evitar problemas, em vez de uma estrutura reativa que depende da alternativa cara de restaurar um sistema após um problema. A política de restrição de software foi introduzida com o lançamento do Microsoft Windows XP para ajudar a proteger sistemas contra código desconhecido e possivelmente perigoso. A política de restrição fornece um mecanismo em que apenas o código confiável recebe privilégios irrestritos a um usuário. O código desconhecido, que pode conter vírus ou código que está em conflito com programas instalados no momento, tem permissão para ser executado somente em um ambiente restrito (geralmente chamado de área restrita) em que não é permitido acessar quaisquer privilégios de usuário sensíveis à segurança.
ms.assetid: 233483a0-ff16-4e21-a312-cc57a92124c3
title: Usando a política de restrição de software em COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e823d794cccf590ddf9ffd8fcb6f7982eb1543368e400ab3632601ec3a2b96e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304932"
---
# <a name="using-the-software-restriction-policy-in-com"></a>Usando a política de restrição de software em COM+

Usar corretamente a política de restrição de software pode tornar sua empresa mais ágil porque fornece uma estrutura proativa para evitar problemas, em vez de uma estrutura reativa que depende da alternativa cara de restaurar um sistema após um problema. A política de restrição de software foi introduzida com o lançamento do Microsoft Windows XP para ajudar a proteger sistemas contra código desconhecido e possivelmente perigoso. A política de restrição fornece um mecanismo em que apenas o código confiável recebe acesso irrestrito aos privilégios de um usuário. O código desconhecido, que pode conter vírus ou código que está em conflito com programas instalados no momento, tem permissão para ser executado somente em um ambiente restrito (geralmente chamado de área *restrita)* em que não é permitido acessar quaisquer privilégios de usuário sensíveis à segurança.

A política de restrição de software depende da atribuição de níveis de confiança ao código que pode ser executado em um sistema. Atualmente, existem dois níveis de confiança: Irrestrito e Não permitido. O código que tem um nível de confiança Irrestrito recebe acesso irrestrito aos privilégios do usuário, portanto, esse nível de confiança deve ser aplicado somente ao código totalmente confiável. O código com um nível de confiança Não permitido não é permitido de acessar quaisquer privilégios de usuário sensíveis à segurança e pode ser executado somente em uma área restrita que ajuda a impedir que o código irrestrito carrega o código não permitido em seu espaço de endereço.

A configuração da política de restrição de software para um sistema é feita por meio da ferramenta administrativa Política de Segurança Local, enquanto a configuração da política de restrição de aplicativos COM+ individuais é feita programaticamente ou por meio da ferramenta administrativa dos Serviços de Componentes. Se o nível de confiança da política de restrição não for especificado para um aplicativo COM+, as configurações de todo o sistema serão usadas para determinar o nível de confiança do aplicativo. As configurações da política de restrição COM+ devem ser cuidadosamente coordenadas com as configurações de todo o sistema porque um aplicativo COM+ que tem um nível de confiança Irrestrito pode carregar somente componentes com um nível de confiança Irrestrito; um aplicativo COM+ não permitido pode carregar componentes com qualquer nível de confiança, mas não pode acessar todos os privilégios do usuário.

Além dos níveis de confiança da política de restrição de software de aplicativos COM+ individuais, duas outras propriedades determinam como a política de restrição é usada para todos os aplicativos COM+. Se [SRPRunningObjectChecks](/windows/desktop/com/srprunningobjectchecks) estiver habilitado, as tentativas de conexão com objetos em execução serão verificadas em busca de níveis de confiança apropriados. O objeto em execução não pode ter um nível de confiança menos rigoroso do que o objeto cliente. Por exemplo, o objeto em execução não poderá ter um nível de confiança Não permitido se o objeto cliente tiver um nível de confiança Irrestrito.

A segunda propriedade determina como a política de restrição de software lida com conexões de ativar como ativador. Se [SRPActivateAsActivatorChecks](/windows/desktop/com/srpactivateasactivatorchecks) estiver habilitado, o nível de confiança configurado para o objeto de servidor será comparado com o nível de confiança do objeto cliente e o nível de confiança mais rigoroso será usado para executar o objeto de servidor. Se SRPActivateAsActivatorChecks não estiver habilitado, o objeto de servidor será executado com o nível de confiança do objeto cliente, independentemente do nível de confiança com o qual ele foi configurado. Por padrão, SRPRunningObjectChecks e SRPActivateAsActivatorChecks estão habilitados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de cliente](client-authentication.md)
</dt> <dt>

[Representação e delegação do cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Configurando a política de restrição de software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Segurança do aplicativo de biblioteca](library-application-security.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> <dt>

[Segurança de componente programático](programmatic-component-security.md)
</dt> <dt>

[Administração de segurança baseada em função](role-based-security-administration.md)
</dt> </dl>

 

 

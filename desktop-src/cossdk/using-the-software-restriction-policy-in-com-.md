---
description: O uso correto da diretiva de restrição de software pode tornar seus negócios mais ágeis, pois fornece uma estrutura proativa para evitar problemas, em vez de uma estrutura reativa que se baseia na alternativa dispendiosa de restaurar um sistema após a ocorrência de um problema. A diretiva de restrição de software foi introduzida com o lançamento do Microsoft Windows XP para ajudar a proteger os sistemas contra códigos desconhecidos e possivelmente perigosos. A política de restrição fornece um mecanismo em que apenas o código confiável recebe acesso irrestrito a privilégios de usuários. Um código desconhecido, que pode conter vírus ou código que está em conflito com os programas atualmente instalados, tem permissão para ser executado apenas em um ambiente restrito (geralmente chamado de área restrita), em que não é permitido acessar nenhum privilégio de usuário sensível à segurança.
ms.assetid: 233483a0-ff16-4e21-a312-cc57a92124c3
title: Usando a política de restrição de software no COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3620aba8cce2859d76ba07c2fa9655dd9036bdbb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457046"
---
# <a name="using-the-software-restriction-policy-in-com"></a>Usando a política de restrição de software no COM+

O uso correto da diretiva de restrição de software pode tornar seus negócios mais ágeis, pois fornece uma estrutura proativa para evitar problemas, em vez de uma estrutura reativa que se baseia na alternativa dispendiosa de restaurar um sistema após a ocorrência de um problema. A diretiva de restrição de software foi introduzida com o lançamento do Microsoft Windows XP para ajudar a proteger os sistemas contra códigos desconhecidos e possivelmente perigosos. A política de restrição fornece um mecanismo em que apenas o código confiável recebe acesso irrestrito aos privilégios de um usuário. Um código desconhecido, que pode conter vírus ou código que está em conflito com os programas atualmente instalados, tem permissão para ser executado apenas em um ambiente restrito (geralmente chamado de *área restrita*), em que não é permitido acessar nenhum privilégio de usuário sensível à segurança.

A diretiva de restrição de software depende da atribuição de níveis de confiança ao código que pode ser executado em um sistema. Atualmente, existem dois níveis de confiança: irrestrito e não permitido. O código que tem um nível de confiança irrestrito recebe acesso irrestrito aos privilégios do usuário, portanto, esse nível de confiança deve ser aplicado somente ao código totalmente confiável. O código com um nível de confiança não permitido não é permitido de acessar nenhum privilégio de usuário sensível à segurança e pode ser executado somente em uma área restrita que ajuda a impedir que código irrestrito carregue o código não permitido em seu espaço de endereço.

A configuração da diretiva de restrição de software para um sistema é feita por meio da ferramenta administrativa diretiva de segurança local, enquanto a configuração da diretiva de restrição de aplicativos COM+ individuais é feita de forma programática ou por meio da ferramenta administrativa serviços de componentes. Se o nível de confiança da política de restrição não for especificado para um aplicativo COM+, as configurações de todo o setor serão usadas para determinar o nível de confiança do aplicativo. As configurações da política de restrição COM+ devem ser cuidadosamente coordenadas com as configurações de todo o nível, pois um aplicativo COM+ que tem um níveis de confiança irrestrito pode carregar apenas componentes com um nível de confiança irrestrito; um aplicativo COM+ não permitido pode carregar componentes com qualquer nível de confiança, mas não pode acessar todos os privilégios do usuário.

Além dos níveis de confiança da diretiva de restrição de software de aplicativos COM+ individuais, duas outras propriedades determinam como a política de restrição é usada para todos os aplicativos COM+. Se [SRPRunningObjectChecks](/windows/desktop/com/srprunningobjectchecks) estiver habilitado, as tentativas de conexão com objetos em execução serão verificadas em relação aos níveis de confiança apropriados. O objeto em execução não pode ter um nível de confiança menos estrito do que o objeto do cliente. Por exemplo, o objeto em execução não poderá ter um nível de confiança não permitido se o objeto de cliente tiver um nível de confiança irrestrito.

A segunda propriedade determina como a diretiva de restrição de software lida com conexões Activate as-Activator. Se [SRPActivateAsActivatorChecks](/windows/desktop/com/srpactivateasactivatorchecks) estiver habilitado, o nível de confiança configurado para o objeto de servidor será comparado com o nível de confiança do objeto de cliente e o nível de confiança mais estrito será usado para executar o objeto de servidor. Se SRPActivateAsActivatorChecks não estiver habilitado, o objeto de servidor será executado com o nível de confiança do objeto de cliente, independentemente do nível de confiança com o qual ele foi configurado. Por padrão, SRPRunningObjectChecks e SRPActivateAsActivatorChecks estão habilitados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de cliente](client-authentication.md)
</dt> <dt>

[Representação e delegação de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Configurando a política de restrição de software](configuring-the-software-restriction-policy.md)
</dt> <dt>

[Segurança de aplicativos de biblioteca](library-application-security.md)
</dt> <dt>

[Segurança de aplicativos de várias camadas](multi-tier-application-security.md)
</dt> <dt>

[Segurança de componente programática](programmatic-component-security.md)
</dt> <dt>

[Administração de segurança baseada em funções](role-based-security-administration.md)
</dt> </dl>

 

 

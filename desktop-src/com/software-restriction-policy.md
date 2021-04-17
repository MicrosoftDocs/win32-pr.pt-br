---
title: Política de restrição de software
description: As configurações da política de restrição de software (SRP) foram introduzidas com o lançamento do Windows XP para ajudar a proteger os sistemas contra códigos desconhecidos e possivelmente perigosos.
ms.assetid: 44b4e448-f5b4-4483-b53b-506938b36857
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97bf42cd949127e9012580ec16379cf36a95353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105797672"
---
# <a name="software-restriction-policy"></a>Política de restrição de software

As configurações da política de restrição de software (SRP) foram introduzidas com o lançamento do Windows XP para ajudar a proteger os sistemas contra códigos desconhecidos e possivelmente perigosos. O SRP fornece um mecanismo em que apenas o código confiável recebe acesso irrestrito aos privilégios de um usuário. Um código desconhecido, que pode conter vírus ou código que está em conflito com os programas atualmente instalados, tem permissão para ser executado apenas em um ambiente restrito (geralmente chamado de *área restrita*), em que não é permitido acessar nenhum privilégio de usuário sensível à segurança. O uso correto do SRP pode tornar seus negócios mais ágeis, pois fornece uma estrutura proativa para evitar problemas, em vez de uma estrutura reativa que se baseia na alternativa dispendiosa de restaurar um sistema após a ocorrência de um problema.

O SRP depende da atribuição de níveis de confiança ao código que pode ser executado em um sistema. Atualmente, existem dois níveis de confiança: irrestrito e não permitido. O código que tem um nível de confiança irrestrito recebe acesso irrestrito aos privilégios do usuário, portanto, esse nível de confiança deve ser aplicado somente ao código totalmente confiável. O código com um nível de confiança não permitido não é permitido de acessar nenhum privilégio de usuário sensível à segurança e pode ser executado somente em uma área restrita para que o código irrestrito não possa carregar o código não permitido em seu espaço de endereço.

A configuração de SRP de aplicativos COM individuais é feita por meio do valor [SRPTrustLevel](srptrustlevel.md) na chave [AppID](appid-key.md) do aplicativo no registro. Se o nível de confiança SRP não for especificado para um aplicativo COM, o valor padrão de não permitido será usado. Um aplicativo COM que tem um nível de confiança irrestrito tem acesso irrestrito aos privilégios do usuário, mas pode carregar apenas componentes com um nível de confiança irrestrito, enquanto um aplicativo COM não permitido pode carregar componentes com qualquer nível de confiança, mas não pode acessar nenhum privilégio de usuário sensível à segurança.

Além dos níveis de confiança do SRP de aplicativos COM individuais, duas outras propriedades de SRP determinam como o SRP é usado para todos os aplicativos COM. Se [SRPRunningObjectChecks](srprunningobjectchecks.md) estiver habilitado, as tentativas de conexão com objetos em execução serão verificadas quanto aos níveis de confiança do SRP apropriados. O objeto em execução não pode ter um nível de confiança SRP menos estrito do que o objeto cliente. Por exemplo, o objeto em execução não poderá ter um nível de confiança não permitido se o objeto de cliente tiver um nível de confiança irrestrito.

A segunda propriedade determina como o SRP lida com conexões de ativação como ativador. Se [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md) estiver habilitado, o nível de confiança do SRP configurado para o objeto de servidor será comparado com o nível de confiança SRP do objeto de cliente e o nível de confiança mais estrito será usado para executar o objeto de servidor. Se **SRPActivateAsActivatorChecks** não estiver habilitado, o objeto de servidor será executado com o nível de confiança SRP do objeto de cliente, independentemente do nível de confiança do SRP com o qual foi configurado. Por padrão, **SRPRunningObjectChecks** e **SRPActivateAsActivatorChecks** estão habilitados.

 

 





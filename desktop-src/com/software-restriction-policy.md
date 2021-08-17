---
title: Política de restrição de software
description: As configurações de SRP (política de restrição de software) foram introduzidas com o lançamento do Windows XP para ajudar a proteger sistemas contra código desconhecido e possivelmente perigoso.
ms.assetid: 44b4e448-f5b4-4483-b53b-506938b36857
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23176b23be5fcf4dc45f040f53e5d8f9dfbcdf05a8aee87feabd125d05c5372d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129798"
---
# <a name="software-restriction-policy"></a>Política de restrição de software

As configurações de SRP (política de restrição de software) foram introduzidas com o lançamento do Windows XP para ajudar a proteger sistemas contra código desconhecido e possivelmente perigoso. O SRP fornece um mecanismo em que apenas o código confiável recebe acesso irrestrito aos privilégios de um usuário. O código desconhecido, que pode conter vírus ou código que está em conflito com programas instalados no momento, tem permissão para ser executado somente em um ambiente restrito (geralmente chamado de área *restrita)* em que não é permitido acessar quaisquer privilégios de usuário sensíveis à segurança. O uso correto do SRP pode tornar sua empresa mais ágil porque fornece uma estrutura proativa para evitar problemas, em vez de uma estrutura reativa que depende da alternativa cara de restaurar um sistema após um problema.

O SRP depende da atribuição de níveis de confiança ao código que pode ser executado em um sistema. Atualmente, existem dois níveis de confiança: Irrestrito e Não permitido. O código que tem um nível de confiança Irrestrito recebe acesso irrestrito aos privilégios do usuário, portanto, esse nível de confiança deve ser aplicado somente ao código totalmente confiável. O código com um nível de confiança não permitido não é permitido de acessar quaisquer privilégios de usuário sensíveis à segurança e pode ser executado somente em uma área restrita para que o código irrestrito não possa carregar o código não permitido em seu espaço de endereço.

A configuração SRP de aplicativos COM individuais é feita por meio do valor [SRPTrustLevel](srptrustlevel.md) na chave [AppID](appid-key.md) do aplicativo no Registro. Se o nível de confiança SRP não for especificado para um aplicativo COM, o valor padrão de Não permitido será usado. Um aplicativo COM que tem um nível de confiança Irrestrito tem acesso irrestrito aos privilégios do usuário, mas pode carregar somente componentes com um nível de confiança Irrestrito, enquanto um aplicativo COM não permitido pode carregar componentes com qualquer nível de confiança, mas não pode acessar privilégios de usuário sensíveis à segurança.

Além dos níveis de confiança SRP de aplicativos COM individuais, duas outras propriedades SRP determinam como o SRP é usado para todos os aplicativos COM. Se [SRPRunningObjectChecks](srprunningobjectchecks.md) estiver habilitado, as tentativas de conexão com objetos em execução serão verificadas em busca de níveis de confiança SRP apropriados. O objeto em execução não pode ter um nível de confiança SRP menos rigoroso do que o objeto cliente. Por exemplo, o objeto em execução não poderá ter um nível de confiança Não permitido se o objeto cliente tiver um nível de confiança Irrestrito.

A segunda propriedade determina como o SRP lida com conexões de ativar como ativador. Se [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md) estiver habilitado, o nível de confiança SRP configurado para o objeto de servidor será comparado com o nível de confiança SRP do objeto cliente e o nível de confiança mais rigoroso será usado para executar o objeto de servidor. Se **SRPActivateAsActivatorChecks** não estiver habilitado, o objeto de servidor será executado com o nível de confiança SRP do objeto cliente, independentemente do nível de confiança SRP com o qual ele foi configurado. Por padrão, **SRPRunningObjectChecks** e **SRPActivateAsActivatorChecks** estão habilitados.

 

 





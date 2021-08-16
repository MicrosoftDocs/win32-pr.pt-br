---
title: Sobre partições do Diretório do Aplicativo
description: Os desenvolvedores que usam ADSI ou LDAP para armazenar e acessar dados relativamente estáticos e globalmente no Active Directory Domain Services também podem preferir, por questão de simplicidade e uniformidade, continuar usando o acesso ADSI ou LDAP para seus requisitos de dados dinâmicos. Os dados dinâmicos mudam com mais frequência do que o recomendado para armazenar em Active Directory Domain Services. Os dados dinâmicos normalmente mudam com mais frequência do que a latência de replicação envolvida na propagação da alteração para todas as réplicas dos dados.
ms.assetid: bf856c3a-9061-474a-a536-c87ca50d5f83
ms.tgt_platform: multiple
keywords:
- Sobre partições do Diretório do Aplicativo
- Partições do Diretório do Aplicativo, Sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9063a05bdb6f04681f012f1e6317b3343833c79c8f6a5af39a1a7865eccbab63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841026"
---
# <a name="about-application-directory-partitions"></a>Sobre partições do Diretório do Aplicativo

Os desenvolvedores que usam ADSI ou LDAP para armazenar e acessar dados relativamente estáticos e globalmente no Active Directory Domain Services também podem preferir, por questão de simplicidade e uniformidade, continuar usando o acesso ADSI ou LDAP para seus requisitos de dados dinâmicos. Os dados dinâmicos mudam com mais frequência do que o recomendado para armazenar em Active Directory Domain Services. Os dados dinâmicos normalmente mudam com mais frequência do que a latência de replicação envolvida na propagação da alteração para todas as réplicas dos dados.

No Windows 2000, o suporte para dados dinâmicos é limitado. Armazenar dados dinâmicos em uma partição de domínio pode ser complicado. Os dados são replicados para todos os controladores de domínio no domínio que geralmente são desnecessários e podem resultar em dados inconsistentes devido à latência de replicação. Isso pode afetar negativamente o desempenho da rede. Além disso, as partições de domínio não são eficazes para aplicativos que devem replicar dados entre limites de domínio. Outra opção no Windows 2000 é armazenar dados dinâmicos em atributos marcados como não replicados. No entanto, essa disposição é limitada porque tem um único ponto de falha, ou seja, o controlador de domínio único que resiria a única cópia dos atributos não replicados do objeto.

As partições de diretório do aplicativo fornecem a capacidade de controlar o escopo da replicação e permitir o posicionamento de réplicas de maneira mais adequada para dados dinâmicos. Como resultado, a partição de diretório do aplicativo fornece a capacidade de hospedar dados dinâmicos no Servidor do Active Directory, permitindo assim o acesso ADSI/LDAP a ele, sem afetar significativamente o desempenho da rede.

O Windows 2000 DNS é um exemplo de um serviço que pode aproveitar as partições do diretório do aplicativo. No Windows 2000, se o serviço DNS estiver configurado opcionalmente para usar Active Directory Domain Services, os dados da zona DNS serão armazenados no Servidor do Active Directory em uma partição de domínio. Ou seja, os dados são replicados para todos os controladores de domínio no domínio, independentemente de um servidor DNS estar configurado para ser executado no controlador de domínio. Essa é uma instância em que a replicação completa em todo o domínio é desnecessária. Ao armazenar os dados da zona DNS em uma partição de diretório do aplicativo, o serviço pode redefinir o escopo da replicação apenas para esse subconjunto de controladores de domínio no domínio que realmente executar o servidor DNS.

Considere os seguintes cenários para hospedar uma réplica de uma partição de diretório de aplicativo:

-   Uma réplica de uma partição de diretório de aplicativo pode ser criada em qualquer sistema operacional Windows Server 2003 e controlador de domínio posterior em uma floresta Active Directory Domain Services dados.
-   O conjunto de controladores de domínio que hospedam réplicas de uma partição de diretório do aplicativo pode ser especificado. Ao contrário de uma partição de domínio, uma partição de diretório de aplicativo não é necessária para replicar para todos os controladores de domínio em um domínio e pode replicar para controladores de domínio em diferentes domínios da floresta.
-   Um controlador de domínio com uma réplica de partição de diretório de aplicativo pode coexistir e funcionar em um ambiente de modo misto com outros computadores que executam o Windows 2000 ou Windows NT 4.0.

Os tipos de dados que podem ser armazenados em uma partição de diretório do aplicativo incluem:

-   Uma partição de diretório do aplicativo pode conter instâncias de qualquer tipo de objeto, exceto entidades de segurança, como usuários, computadores ou grupos.
-   Os objetos em uma partição de diretório de aplicativo podem manter referências de valor DN a outros objetos na mesma partição de diretório do aplicativo, a objetos nas partições de configuração e esquema e a qualquer cabeça de contexto de nomentura (que é o objeto superior de uma partição de diretório, como o objeto **domainDNS** na parte superior de uma partição de diretório do aplicativo).
-   Para obter mais informações e um exemplo do tipo de dados dinâmicos que podem ser armazenados em uma partição de diretório do aplicativo, consulte [Objetos dinâmicos.](dynamic-objects.md) Há suporte para objetos dinâmicos a partir do Windows Server 2003. Objetos dinâmicos têm uma propriedade que determina o tempo de vida, após o qual o objeto é excluído pelo servidor do Active Directory.

Algumas limitações das partições de diretório do aplicativo incluem:

-   Objetos em uma partição de diretório de aplicativo não podem manter *referências de valor DN* a objetos em outras partições de diretório do aplicativo ou partições de domínio. (Referências de valor DN são referências persistentes a um valor de nome diferenciado, como "CN=someuser,DC=corp,DC=Fabrikam,DC=com"). Da mesma forma, os objetos nas partições Domínio, Configuração e Esquema não podem manter referências de valor DN a objetos em uma partição de diretório do aplicativo. Uma referência de valor DN pode ser mantida no head de contexto de nomentura. () )
-   Objetos em uma partição de diretório de aplicativo não são replicados para o Catálogo Global. Assim como com qualquer controlador de domínio, um servidor de catálogo global também pode ser configurado para conter uma réplica completa de uma partição de diretório do aplicativo, mas os dados de partição do diretório do aplicativo são completamente separados dos dados do catálogo global.
-   Quando uma réplica de partição de diretório do aplicativo é criada, a função Domain-Naming FSMO deve estar em um dos controladores de domínio do Windows Server 2003 e posteriores do sistema operacional. Depois que a réplica de partição do diretório do aplicativo for criada, a função FSMO de Nomenplicação de Domínio poderá ser atribuída de volta a um controlador de domínio Windows 2000.
-   Os objetos de partição do diretório do aplicativo não podem ser movidos para outras partições do Active Directory fora da partição na qual foram criados.

Outros recursos de partição do diretório do aplicativo incluem:

-   O modelo de segurança e controle de acesso para a partição de diretório do aplicativo é o mesmo para outras partições no Active Directory Domain Services.
-   Os intervalos de tempo que controlam a latência de iniciar uma notificação de alteração originada para parceiros de replicação em um site podem ser configurados separadamente para cada base de partição do diretório do aplicativo.
-   As partições de diretório do aplicativo podem ser nomeadas como domínios regulares, anexadas em qualquer lugar no namespace do Active Directory em que um domínio pode e descobertas usando DNS, mesmo por sistemas Windows 2000.
-   Uma partição de diretório do aplicativo pode ser criada, seu escopo de replicação definido e suas configurações configuráveis ajustadas programaticamente usando APIs LDAP e ADSI padrão. Para obter mais informações sobre como manipular partições de diretório de aplicativo de forma programática, consulte [Application Directory Partitions](application-directory-partitions.md).

 

 





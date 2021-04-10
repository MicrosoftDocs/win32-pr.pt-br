---
title: Sobre partições de diretório de aplicativo
description: Os desenvolvedores que usam ADSI ou LDAP para armazenar e acessar dados relativamente estáticos e globais em Active Directory Domain Services também podem preferir, por questões de simplicidade e uniformidade, para continuar usando o acesso de ADSI ou LDAP para seus requisitos de dados dinâmicos. Os dados dinâmicos são alterados com mais frequência do que o que foi recomendado para armazenar em Active Directory Domain Services. Normalmente, os dados dinâmicos são alterados com mais frequência do que a latência de replicação envolvida na propagação da alteração para todas as réplicas dos dados.
ms.assetid: bf856c3a-9061-474a-a536-c87ca50d5f83
ms.tgt_platform: multiple
keywords:
- Sobre partições de diretório de aplicativo
- Partições de diretório de aplicativos, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc1970f27d18d760ab3a45fae389809a40a2a89
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004824"
---
# <a name="about-application-directory-partitions"></a>Sobre partições de diretório de aplicativo

Os desenvolvedores que usam ADSI ou LDAP para armazenar e acessar dados relativamente estáticos e globais em Active Directory Domain Services também podem preferir, por questões de simplicidade e uniformidade, para continuar usando o acesso de ADSI ou LDAP para seus requisitos de dados dinâmicos. Os dados dinâmicos são alterados com mais frequência do que o que foi recomendado para armazenar em Active Directory Domain Services. Normalmente, os dados dinâmicos são alterados com mais frequência do que a latência de replicação envolvida na propagação da alteração para todas as réplicas dos dados.

No Windows 2000, o suporte para dados dinâmicos é limitado. O armazenamento de dados dinâmicos em uma partição de domínio pode ser complicado. Os dados são replicados para todos os controladores de domínio no domínio, que geralmente são desnecessários e podem resultar em dados inconsistentes devido à latência de replicação. Isso pode afetar negativamente o desempenho da rede. Além disso, as partições de domínio não são eficazes para aplicativos que devem replicar dados entre limites de domínio. Outra opção no Windows 2000 é armazenar dados dinâmicos em atributos marcados como não replicados. No entanto, essa organização é limitada, pois tem um ponto único de falha, ou seja, o único controlador de domínio hospeda a única cópia dos atributos não replicados do objeto.

As partições de diretório de aplicativo fornecem a capacidade de controlar o escopo da replicação e permitir o posicionamento de réplicas de uma maneira mais adequada para dados dinâmicos. Como resultado, a partição de diretório de aplicativos fornece a capacidade de hospedar dados dinâmicos no servidor de Active Directory, permitindo, portanto, acesso de ADSI/LDAP a ele, sem afetar significativamente o desempenho da rede.

O serviço DNS do Windows 2000 é um exemplo de um serviço que pode tirar proveito das partições de diretório de aplicativo. No Windows 2000, se o serviço DNS for configurado opcionalmente para usar Active Directory Domain Services, os dados da zona DNS serão armazenados no servidor de Active Directory em uma partição de domínio. Ou seja, os dados são replicados para todos os controladores de domínio no domínio, independentemente de um servidor DNS estar configurado para ser executado no controlador de domínio. Essa é uma instância em que a replicação completa em todo o domínio é desnecessária. Ao armazenar os dados de zona DNS em uma partição de diretório de aplicativo, o serviço pode redefinir o escopo da replicação somente para esse subconjunto de controladores de domínio no domínio que realmente executa o servidor DNS.

Considere os seguintes cenários para hospedar uma réplica de uma partição de diretório de aplicativos:

-   Uma réplica de uma partição de diretório de aplicativo pode ser criada em qualquer sistema operacional Windows Server 2003 e controlador de domínio posterior em uma floresta Active Directory Domain Services.
-   O conjunto de controladores de domínio que hospedam réplicas de uma partição de diretório de aplicativos pode ser especificado. Ao contrário de uma partição de domínio, uma partição de diretório de aplicativo não precisa ser replicada para todos os controladores de domínio em um domínio e pode replicar para controladores de domínio em domínios diferentes da floresta.
-   Um controlador de domínio com uma réplica de partição de diretório de aplicativo pode coexistir e funcionar em um ambiente de modo misto com outros computadores que executam o Windows 2000 ou o Windows NT 4,0.

Os tipos de dados que podem ser armazenados em uma partição de diretório de aplicativo incluem:

-   Uma partição de diretório de aplicativo pode conter instâncias de qualquer tipo de objeto, exceto entidades de segurança, como usuários, computadores ou grupos.
-   Os objetos em uma partição de diretório de aplicativo podem manter referências de valor DN para outros objetos na mesma partição de diretório de aplicativo, para objetos nas partições de configuração e esquema e para qualquer cabeçalho de contexto de nomenclatura (que é o objeto superior de uma partição de diretório, como o objeto **domainDns** na parte superior de uma partição de diretório de aplicativo).
-   Para obter mais informações e um exemplo do tipo de dados dinâmicos que podem ser armazenados em uma partição de diretório de aplicativo, consulte [objetos dinâmicos](dynamic-objects.md). Há suporte para objetos dinâmicos a partir do Windows Server 2003. Os objetos dinâmicos têm uma propriedade que determina a vida útil, após a qual o objeto é excluído pelo servidor de Active Directory.

Algumas limitações das partições de diretório de aplicativo incluem:

-   Objetos em uma partição de diretório de aplicativo não podem manter *referências de valor DN* para objetos em outras partições de diretório de aplicativo ou partições de domínio. (Referências de valor DN são referências persistentes a um valor de nome distinto, como "CN = someuser, DC = Corp, DC = Fabrikam, DC = com"). Da mesma forma, objetos em domínio, configuração e partições de esquema não podem manter referências de valor DN para objetos em uma partição de diretório de aplicativo. Uma referência de valor DN pode ser mantida para o cabeçalho de contexto de nomenclatura. () )
-   Os objetos em uma partição de diretório de aplicativo não são replicados para o catálogo global. Assim como ocorre com qualquer controlador de domínio, um servidor de catálogo global também pode ser configurado para conter uma réplica completa de uma partição de diretório de aplicativo, mas os dados de partição de diretório de aplicativo são completamente separados dos dados do catálogo global.
-   Quando uma réplica de partição de diretório de aplicativo é criada, a função FSMO de Domain-Naming deve estar em um dos controladores de domínio do sistema operacional Windows Server 2003 e posterior. Depois que a réplica de partição de diretório de aplicativo é criada, a função FSMO de nomeação de domínio pode ser atribuída de volta a um controlador de domínio do Windows 2000.
-   Os objetos de partição de diretório de aplicativo não podem ser movidos para outras partições de Active Directory fora da partição na qual foram criados.

Outros recursos de partição de diretório de aplicativo incluem:

-   O modelo de controle de acesso e segurança para a partição de diretório de aplicativo é o mesmo que para outras partições no Active Directory Domain Services.
-   Os intervalos de tempo que controlam a latência de iniciar uma notificação de alteração originada para parceiros de replicação em um site podem ser configurados separadamente para cada partição de diretório de aplicativo.
-   As partições de diretório de aplicativo podem ser nomeadas como domínios regulares, anexados em qualquer lugar no namespace de Active Directory em que um domínio pode e descoberto usando o DNS mesmo por sistemas Windows 2000 de nível inferior.
-   Uma partição de diretório de aplicativo pode ser criada, seu escopo de replicação definido e suas configurações configuráveis são ajustadas programaticamente usando as APIs LDAP e ADSI padrão. Para obter mais informações sobre a manipulação programática de partições de diretório de aplicativos, consulte [partições de diretório de aplicativos](application-directory-partitions.md).

 

 





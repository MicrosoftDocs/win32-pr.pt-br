---
title: A patch do Software de Jogo no Windows XP, Windows Vista e Windows 7
description: Este artigo examina alguns métodos de a patch que funcionarão bem no Windows Vista e Windows 7, bem como Windows XP.
ms.assetid: 27be805a-bffd-a9f8-2207-2a9a4822ba48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91dae9b3bc91c96006f3b2117093962ee485db948fd983191f2db3c7f88fb33a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042496"
---
# <a name="patching-game-software-in-windows-xp-windows-vista-and-windows-7"></a>A patch do Software de Jogo no Windows XP, Windows Vista e Windows 7

Windows O Vista Windows 7 tem vários recursos para tornar o sistema operacional mais seguro. Segurança adicionada significa que a aplicação de patches ao software não é tão simples quanto era no passado. Este artigo examina alguns métodos de a patch que funcionarão bem no Windows Vista e Windows 7, bem como Windows XP.

Há duas categorias principais de jogos que exigem patches:

-   Jogos que exigem apenas patches ocasionais, como a maioria dos jogos offline.
-   Jogos que exigem patches frequentes, como a maioria dos jogos online.

Este artigo também oferece uma breve introdução ao UAC (Controle de Conta de Usuário) para servir como base sobre os direitos que os desenvolvedores podem esperar que os usuários tenham no Windows Vista e Windows 7.

-   [Controle de conta de usuário](#user-account-control)
-   [Jogos que exigem apenas patches ocasionais](#games-that-require-only-occasional-patches)
    -   [Método 1: usar Windows instalador para patches ocasionais](#method-1-use-windows-installer-for-occasional-patches)
    -   [Método 2: Exigir direitos de administrador para aplicar patches](#method-2-require-administrator-rights-to-apply-patches)
-   [Jogos que exigem patches frequentes](#games-that-require-frequent-patches)
    -   [Método 3: Instalar por usuário](#method-3-install-per-user)
    -   [Método 4: Instalar em um local de Per-Computer Comum](#method-4-install-to-a-common-per-computer-location)
    -   [Outras possibilidades](#other-possibilities)
-   [Resumo](#summary)

## <a name="user-account-control"></a>Controle de Conta de Usuário

Windows O Vista e Windows 7 têm dois tipos principais de contas de usuário: Usuário Padrão e Administrador. Uma conta de usuário padrão tem várias restrições de acesso; por exemplo, ele não pode gravar dados no sistema de arquivos em %SystemDrive% Arquivos de Programas ou no Registro no \\ COMPUTADOR LOCAL do \_ HKEY. \_ Isso terá implicações para aplicar patches a um jogo se ele estiver instalado em um local somente leitura. Ao contrário Windows XP, a conta de Usuário Padrão é muito mais comum no Windows Vista e Windows 7. Contas de usuário padrão também são necessárias para recursos importantes do sistema operacional, como controles dos pais. Os controles dos pais exigem que a conta filho seja Usuário Padrão e elevar essa conta para Administrador para até mesmo um jogo impede que os controles dos pais trabalham com todos os outros jogos. Portanto, é importante que os jogos sejam projetados para o Usuário Padrão.

Windows O Vista e Windows 7 têm um modelo mais novo para direitos de usuário, para ajudar a impedir que os usuários executem programas que tentam executar operações que o usuário não pretende nem autoriza. Para esse fim, o Controle de Conta de Usuário (anteriormente chamado de Conta de Usuário com privilégios mínimos ou LUA) permite que os usuários operem o computador com direitos de baixo nível na maioria das vezes, ao mesmo tempo em que podem executar facilmente aplicativos que exigem direitos de nível superior, quando necessário. Isso significa que contas de usuário padrão e contas de administrador são ambas executar aplicativos com direitos de Usuário Padrão, mas somente as contas de Administrador têm a capacidade de conceder direitos elevados aos aplicativos. O sistema operacional solicita aos usuários com contas de Administrador consentimento explícito antes de executar um aplicativo com direitos elevados e, se um programa que exige direitos de Administrador for executado em uma conta de Usuário Padrão, o sistema solicitará a aprovação do Administrador.

## <a name="games-that-require-only-occasional-patches"></a>Jogos que exigem apenas patches ocasionais

Alguns jogos exigem apenas alguns patches em todo o ciclo de vida. Dois métodos que você pode empregar para essa frequência de a patch são distribuir patches como pacotes do instalador do Windows, que geralmente não exigem direitos de Administrador ou usar algum outro tipo de distribuição que modifica diretamente os arquivos de jogo.

> [!Note]  
> Independentemente de um jogo exigir a aplicação de patch frequente, os aplicativos normalmente exigem que os direitos de administrador sejam instalados ou removidos.

 

### <a name="method-1-use-windows-installer-for-occasional-patches"></a>Método 1: usar Windows instalador para patches ocasionais

Nesse método, um instalador Windows é usado para instalar um pacote (arquivo .msi) e um patch do instalador do Windows (arquivo .msp) é distribuído para instalar patches. O pacote deve ter uma tabela MsiPatchCertificate e o patch deve ser assinado digitalmente por um certificado na tabela. Mais informações sobre a assinatura digital podem ser encontradas em [Autenticação Authenticode para desenvolvedores de jogos.](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

Mais detalhes e requisitos para usar esse método de a patch podem ser encontrados na documentação do Windows Installer:

-   [A patch e as atualizações](/windows/desktop/Msi/patching-and-upgrades)
-   [A patch do UAC (Controle de Conta de Usuário)](/windows/desktop/Msi/user-account-control--uac--patching)

A desvantagem desse método é que, se o jogo não tiver sido instalado da mídia removível no Windows XP, a adoção de patch exigirá direitos de Administrador. No entanto, isso provavelmente não é muito restritivo, porque a maioria dos administradores de usuários no Windows XP e a restrição ao software instalado de mídia removível não está presente no Windows Vista.

A principal vantagem desse método é que os patches podem ser aplicados por uma conta de usuário padrão sem a necessidade de um prompt e autenticação para direitos elevados. Isso fornece uma melhor experiência do usuário, pois para jogar um jogo, um usuário com uma conta de Usuário Padrão não precisa pedir a alguém com uma conta de Administrador para instalar o patch ou fornecer à conta de usuário padrão direitos permanentes de Administrador.

É possível que esse método funcione para jogos que exigem patches frequentes, mas a sobrecarga de usar pacotes do instalador do Windows, em termos de integração de build e suporte a um grande número de arquivos, pode tornar esse método menos desejável do que outros.

### <a name="method-2-require-administrator-rights-to-apply-patches"></a>Método 2: Exigir direitos de administrador para aplicar patches

Nesse método, o arquivo executável que aplica o patch requer direitos de Administrador para execução. Com os direitos de Administrador, o executável de a patch pode modificar diretamente os arquivos de jogo localizados em %SystemDrive% \\ Program Files.

A vantagem desse método é sua simplicidade. No entanto, esse método não será adequado se o jogo precisar de patches frequentes, porque se um usuário com uma conta de Usuário Padrão quiser jogar um jogo que exija patches frequentes, como um jogo online de vários jogadores, esse usuário terá duas opções:

-   Faça com que um Administrador faça logoff e faça patch no jogo, o que pode ser inconveniente para ambas as partes.
-   Ter sua conta permanentemente elevada com direitos de Administrador.

> [!Note]  
> A última solução não apenas desescia a segurança do sistema como um todo, mas impede que recursos importantes, como controles dos pais, funcionaam.

 

Ao implementar esse método, o arquivo executável que aplica o patch deve ser diferente do executável do jogo. O manifesto do executável de aplicação de patch deve especificar requireAdministrator para requestedExecutionLevel denotá-lo como um aplicativo que requer direitos de Administrador. Mais informações sobre como fazer isso podem ser encontradas em Práticas recomendadas para desenvolvedores e diretrizes para aplicativos em um ambiente com privilégios [mínimos,](/previous-versions/dotnet/articles/aa480150(v=msdn.10))em "Esquema de Manifesto do Aplicativo".

Quando esse método é usado, mesmo com as configurações no manifesto, o arquivo executável ainda pode ser lançado sem direitos de Administrador em dois casos:

-   Se o sistema operacional for Windows XP e a conta do usuário for um Usuário Restrito.
-   Se o sistema operacional for Windows Vista ou Windows 7, a conta do usuário será um Usuário Padrão e o UAC será desabilitado.

Ambos são cenários de consumidor raros. No entanto, o patcher deve ter o manifesto que exige direitos de Administrador e deve chamar [**IsUserAnAdmin**](/windows/desktop/api/shlobj_core/nf-shlobj_core-isuseranadmin); Se essa função retornar FALSE, a mensagem de erro "Direitos de administrador são necessários" será exibida.

Em geral, o método 1 é preferível para jogos que precisam de apenas alguns patches em relação aos seus tempos de vida.

## <a name="games-that-require-frequent-patches"></a>Jogos que exigem patches frequentes

Muitos jogos baseados na Internet estão sendo aprimorados continuamente e geralmente exigem patches regulares. Para esses jogos, os patches podem ser aplicados por usuário ou por computador, conforme discutido nos tópicos a seguir. Outras soluções possíveis incluem a alteração da ACL que protege %SystemDrive% dos Arquivos de \\ Programas ou a criação de um serviço personalizado.

### <a name="method-3-install-per-user"></a>Método 3: Instalar Per-User

Uma abordagem recomendada e fácil é instalar todo o jogo em uma subpasta por usuário da pasta de dados do aplicativo local, que você pode encontrar chamando [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) com CSIDL \_ LOCAL \_ APPDATA. Um caminho de exemplo é C: \\ Documentos e Configurações nome de usuário Local Configurações Application Data \\ \\ \\ \\ ExampleGame. Esse local permite que um aplicativo em execução com direitos de Usuário Padrão modifique diretamente os arquivos do jogo.

No entanto, há uma desvantagem para essa abordagem quando um computador tem vários usuários: cada usuário tem uma cópia do jogo instalada e os patches devem ser baixados e aplicados por cada usuário. Isso perde não apenas o tempo e o espaço em disco dos usuários, mas também aumenta o uso da largura de banda de rede para o servidor que fornece patches. Além disso, como qualquer aplicativo com direitos de usuário padrão pode modificar o jogo, os executáveis do jogo são menos protegidos; É responsabilidade do fabricante do jogo decidir se isso é aceitável ou não.

### <a name="method-4-install-to-a-common-per-computer-location"></a>Método 4: Instalar em um local de Per-Computer Comum

Outro método é instalar os dados de jogos não executáveis em um subdiretório do caminho especificado por [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) CSIDL COMMON APPDATA; um caminho de exemplo é C: Documentos e Configurações Exemplo de Dados de Aplicativo de Todos os \_ \_ \\ \\ \\ \\ Usuários. Esse é um local compartilhado para todos os usuários e pode ser modificado por aplicativos que são executados com direitos de Usuário Padrão. Esse método minimiza a necessidade de reaplicar patches grandes quando o jogo é desempenhado de mais de uma conta. Arquivos executáveis para o jogo devem ser mantidos em %SystemDrive% Arquivos de Programas para minimizar o risco para \\ outras contas no sistema. Os arquivos executáveis devem verificar a integridade do novo conteúdo no diretório compartilhado, pois esse local pode ser modificado por um programa ou pessoa com direitos de Usuário Padrão; considere usar [**MapFileAndCheckSum**](/windows/desktop/api/imagehlp/nf-imagehlp-mapfileandchecksuma) para calcular uma verificação dos arquivos.

Esse método tem a vantagem de trabalhar igualmente bem no Windows XP e Windows Vista e não requer direitos de Administrador.

### <a name="other-possibilities"></a>Outras possibilidades

Fora dos métodos já discutidos, outra possibilidade é alterar a ACL de %SystemDrive% Program Files Game Folder ao instalar o jogo para que uma ferramenta de a patch possa gravar diretamente nos arquivos do jogo mesmo quando executado com direitos de Usuário \\ \\ \\ Padrão. Embora isso não seja difícil, ele ignora a proteção de segurança que o sistema oferece aos arquivos do jogo e fornece uma oportunidade para programas mal-intencionados alterarem o conteúdo do diretório. Isso não é aconselhável e é altamente recomendável que uma alternativa seja usada.

Uma possibilidade final é escrever um serviço personalizado. Em geral, escrever um serviço personalizado para corrigir jogos não é uma boa ideia, pois isso é complicado e propenso a erros. É recomendável que a adoção de patch seja feita por meio de outros métodos discutidos neste artigo. No entanto, um serviço personalizado pode ser necessário quando combinado com soluções anti-fraude ou antivassuidade. Esse serviço deve dar suporte a um grande número de jogos e ser projetado para que ele só possa baixar os arquivos de patch e gravar somente no diretório de instalação do jogo de destino. É importante que o serviço seja pequeno, tenha uma área de superfície mínima vulnerável a ataques e use o menor número possível de recursos do sistema quando o jogo não estiver em execução.

## <a name="summary"></a>Resumo

Por fim, é decisão sua decidir qual método implementar. Você precisa avaliar os fatores que são importantes para você. Segurança, frequência de aplicação de patch, facilidade de uso pelo cliente, carga de trabalho necessária para implementar, complexidade da solução e conformidade de recursos da plataforma são os fatores que cada desenvolvedor deve considerar antes de decidir sobre um método específico.

Você pode encontrar mais informações sobre a proteção de conta de usuário [Windows Vista Application Development Requirements for User Account Control (UAC).](/previous-versions/aa905330(v=msdn.10))

 

 
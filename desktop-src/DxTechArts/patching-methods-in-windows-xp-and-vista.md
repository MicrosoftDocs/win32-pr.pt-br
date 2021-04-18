---
title: Aplicação de patch no software de jogos no Windows XP, no Windows Vista e no Windows 7
description: Este artigo examina alguns métodos de aplicação de patch que funcionarão bem no Windows Vista e no Windows 7, bem como no Windows XP.
ms.assetid: 27be805a-bffd-a9f8-2207-2a9a4822ba48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ae0b1455cae61b8372f81e6928977743084c9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105757828"
---
# <a name="patching-game-software-in-windows-xp-windows-vista-and-windows-7"></a>Aplicação de patch no software de jogos no Windows XP, no Windows Vista e no Windows 7

O Windows Vista e o Windows 7 têm uma série de recursos para tornar o sistema operacional mais seguro. Segurança adicionada significa que a aplicação de patches ao software não é tão simples quanto no passado. Este artigo examina alguns métodos de aplicação de patch que funcionarão bem no Windows Vista e no Windows 7, bem como no Windows XP.

Há duas categorias principais de jogos que exigem patches:

-   Jogos que exigem apenas patches ocasionais, como a maioria dos jogos offline.
-   Jogos que exigem patches frequentes, como a maioria dos jogos online.

Este artigo também oferece uma breve introdução ao UAC (controle de conta de usuário) para servir como plano de fundo sobre os direitos que os desenvolvedores podem esperar que os usuários tenham no Windows Vista e no Windows 7.

-   [Controle de conta de usuário](#user-account-control)
-   [Jogos que exigem apenas patches ocasionais](#games-that-require-only-occasional-patches)
    -   [Método 1: usar Windows Installer para patches ocasionais](#method-1-use-windows-installer-for-occasional-patches)
    -   [Método 2: exigir direitos de administrador para aplicar patches](#method-2-require-administrator-rights-to-apply-patches)
-   [Jogos que exigem patches frequentes](#games-that-require-frequent-patches)
    -   [Método 3: instalar por usuário](#method-3-install-per-user)
    -   [Método 4: instalar em um local de Per-Computer comum](#method-4-install-to-a-common-per-computer-location)
    -   [Outras possibilidades](#other-possibilities)
-   [Resumo](#summary)

## <a name="user-account-control"></a>Controle de Conta de Usuário

O Windows Vista e o Windows 7 têm dois tipos principais de contas de usuário: usuário padrão e administrador. Uma conta de usuário padrão tem várias restrições de acesso; por exemplo, ele não pode gravar dados no sistema de arquivos em% SystemDrive% \\ arquivos de programas ou no registro no \_ computador local hKey \_ . Isso tem implicações para aplicar patches a um jogo se ele estiver instalado em um local somente leitura. Ao contrário do Windows XP, a conta de usuário padrão é muito mais comum no Windows Vista e no Windows 7. As contas de usuário padrão também são necessárias para recursos importantes do sistema operacional, como controles dos pais. Os controles dos pais exigem que a conta filho seja usuário padrão, e elevar essa conta para o administrador de até mesmo um jogo impede que os controles dos pais trabalhem com todos os outros jogos. Portanto, é importante que os jogos sejam projetados para o usuário padrão.

O Windows Vista e o Windows 7 têm um modelo mais recente para direitos de usuário, para ajudar a impedir que os usuários executem programas que tentam executar operações que o usuário não pretende ou autorizar. Para esse fim, o controle de conta de usuário (anteriormente chamado de conta de usuário com privilégios mínimos ou LUA) permite que os usuários operem o computador com direitos de nível inferior na maior parte do tempo, e possam facilmente executar aplicativos que exigem direitos de nível superior, quando necessário. Isso significa que contas de usuário padrão e contas de administrador executam aplicativos com direitos de usuário padrão, mas somente contas de administrador têm a capacidade de conceder direitos elevados aos aplicativos. O sistema operacional solicita aos usuários com contas de administrador o consentimento explícito antes de executar um aplicativo com direitos elevados e, se um programa que requer direitos de administrador for executado em uma conta de usuário padrão, o sistema solicitará a aprovação do administrador.

## <a name="games-that-require-only-occasional-patches"></a>Jogos que exigem apenas patches ocasionais

Alguns jogos exigem apenas alguns patches em todo o ciclo de vida. Dois métodos que você pode empregar para essa frequência de aplicação de patches são distribuir patches como pacotes de Windows Installer, que geralmente não exigem direitos de administrador ou para usar algum outro tipo de distribuição que modifica os arquivos de jogos diretamente.

> [!Note]  
> Independentemente de um jogo exigir aplicação de patch freqüente, os aplicativos normalmente exigem que os direitos de administrador sejam instalados ou removidos.

 

### <a name="method-1-use-windows-installer-for-occasional-patches"></a>Método 1: usar Windows Installer para patches ocasionais

Nesse método, um Windows Installer é usado para instalar um pacote (arquivo. msi) e um patch Windows Installer (arquivo. msp) é distribuído para instalar patches. O pacote deve ter uma tabela MsiPatchCertificate e o patch deve ser assinado digitalmente por um certificado na tabela. Mais informações sobre a assinatura digital podem ser encontradas em [assinatura Authenticode para desenvolvedores de jogos](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

Mais detalhes e requisitos para usar esse método de aplicação de patch podem ser encontrados na documentação do Windows Installer:

-   [Aplicação de patch e atualizações](/windows/desktop/Msi/patching-and-upgrades)
-   [Aplicação de patch de UAC (controle de conta de usuário)](/windows/desktop/Msi/user-account-control--uac--patching)

A desvantagem desse método é que, se o jogo não tiver sido instalado a partir de mídia removível no Windows XP, a aplicação de patches exigirá direitos de administrador. No entanto, isso não é provavelmente muito restritivo, pois a maioria dos administradores de usuários no Windows XP e a restrição de software instalado a partir de mídia removível não estão presentes no Windows Vista.

A principal vantagem desse método é que os patches podem ser aplicados por uma conta de usuário padrão sem a necessidade de uma solicitação e autenticação para direitos elevados. Isso proporciona uma melhor experiência do usuário, pois, para jogar um jogo, um usuário com uma conta de usuário padrão não precisa pedir a alguém com uma conta de administrador para instalar o patch ou para fornecer a conta de usuário padrão com direitos de administrador permanentes.

É possível que esse método funcione para jogos que exigem patches frequentes, mas a sobrecarga de usar pacotes de Windows Installer, em termos de integração de compilação e suporte a um grande número de arquivos, pode tornar esse método menos desejável do que outros.

### <a name="method-2-require-administrator-rights-to-apply-patches"></a>Método 2: exigir direitos de administrador para aplicar patches

Nesse método, o arquivo executável que aplica o patch requer a execução de direitos de administrador. Com direitos de administrador, o executável de aplicação de patch pode modificar diretamente os arquivos de jogos localizados em arquivos de programas% SystemDrive% \\ .

A vantagem desse método é sua simplicidade. No entanto, esse método não é adequado se o jogo precisar de patches frequentes, porque se um usuário com uma conta de usuário padrão quiser jogar um jogo que exige patches frequentes, como um jogo online de vários jogadores em grande escala, esse usuário terá duas opções:

-   Obtenha um administrador para fazer logon e corrigir o jogo, que pode ser inconveniente para ambas as partes.
-   Faça com que sua conta seja promovida permanentemente com direitos de administrador.

> [!Note]  
> A última solução não apenas enfraquece a segurança do sistema como um todo, mas impede que recursos importantes, como controles dos pais, funcionem.

 

Ao implementar esse método, o arquivo executável que aplica o patch deve ser diferente do executável do jogo. O manifesto do executável de aplicação de patch deve especificar requireAdministrator para requestedExecutionLevel para denotar como um aplicativo que exige direitos de administrador. Mais informações sobre como fazer isso podem ser encontradas em [práticas recomendadas do desenvolvedor e diretrizes para aplicativos em um ambiente com privilégios mínimos](/previous-versions/dotnet/articles/aa480150(v=msdn.10)), em "esquema do manifesto do aplicativo".

Quando esse método é usado, mesmo com as configurações no manifesto, o arquivo executável ainda pode ser iniciado sem direitos de administrador em dois casos:

-   Se o sistema operacional for o Windows XP e a conta do usuário for um usuário restrito.
-   Se o sistema operacional for o Windows Vista ou o Windows 7, a conta do usuário será um usuário padrão e o UAC será desabilitado.

Ambos são cenários raros de consumo. No entanto, o patcher deve fazer com que o manifesto exija direitos de administrador e deve chamar [**IsUserAnAdmin**](/windows/desktop/api/shlobj_core/nf-shlobj_core-isuseranadmin); Se essa função retornar FALSE, a mensagem de erro "direitos de administrador são necessários" será exibida.

Em geral, o método 1 é preferível para jogos que precisam de apenas alguns patches durante seus tempos de vida.

## <a name="games-that-require-frequent-patches"></a>Jogos que exigem patches frequentes

Muitos jogos baseados na Internet estão sendo aprimorados continuamente e geralmente exigem patches regulares. Para esses jogos, os patches podem ser aplicados por usuário ou por computador, conforme discutido nos tópicos a seguir. Outras soluções possíveis incluem alterar a ACL que protege arquivos de programas% SystemDrive% \\ ou criar um serviço personalizado.

### <a name="method-3-install-per-user"></a>Método 3: instalar Per-User

Uma abordagem recomendada e fácil é instalar o jogo inteiro em uma subpasta por usuário da pasta de dados do aplicativo local, que você pode encontrar chamando [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) com \_ AppData local CSIDL \_ . Um exemplo de caminho é C: \\ Documents and Settings \\ User name \\ Local Settings \\ Application Data \\ ExampleGame. Esse local permite que um aplicativo em execução com direitos de usuário padrão modifique arquivos de jogos diretamente.

No entanto, há uma desvantagem dessa abordagem quando um computador tem vários usuários: cada usuário tem uma cópia do jogo instalada e os patches devem ser baixados e aplicados por cada usuário. Isso desperdiça não apenas o espaço em disco e o tempo dos usuários, mas também aumenta o uso da largura de banda de rede para o servidor que fornece patches. Além disso, como qualquer aplicativo com direitos de usuário padrão pode modificar o jogo, os executáveis de jogos são menos protegidos; cabe ao fabricante do jogo decidir se isso é aceitável ou não.

### <a name="method-4-install-to-a-common-per-computer-location"></a>Método 4: instalar em um local de Per-Computer comum

Outro método é instalar os dados do jogo não executável em um subdiretório do caminho especificado por [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) CSIDL \_ Common \_ AppData; um caminho de exemplo é C: \\ Documents and Settings \\ All Users \\ Application Data \\ ExampleGame. Esse é um local compartilhado para todos os usuários e pode ser modificado por aplicativos que são executados com direitos de usuário padrão. Esse método minimiza a necessidade de reaplicar patches grandes quando o jogo é reproduzido de mais de uma conta. Os arquivos executáveis para o jogo devem ser mantidos em arquivos de programas% SystemDrive% \\ para minimizar o risco a outras contas no sistema. Os arquivos executáveis devem verificar a integridade do novo conteúdo no diretório compartilhado, já que esse local pode ser modificado por um programa ou pessoa com direitos de usuário padrão; Considere o uso de [**MapFileAndCheckSum**](/windows/desktop/api/imagehlp/nf-imagehlp-mapfileandchecksuma) para computar uma soma de verificação dos arquivos.

Esse método tem a vantagem de trabalhar igualmente bem no Windows XP e no Windows Vista, além de não exigir direitos de administrador.

### <a name="other-possibilities"></a>Outras possibilidades

Fora dos métodos já abordados, outra possibilidade é alterar a ACL da pasta de jogos de arquivos de programas% SystemDrive% \\ \\ \\ ao instalar o jogo para que uma ferramenta de aplicação de patch possa gravar diretamente nos arquivos do jogo mesmo quando ele for executado com direitos de usuário padrão. Embora isso não seja difícil, ele ignora a proteção de segurança que o sistema oferece aos arquivos do jogo e fornece uma oportunidade para que programas mal-intencionados alterem o conteúdo do diretório. Isso não é aconselhável e é altamente recomendável que uma alternativa seja usada em vez disso.

Uma possibilidade final é escrever um serviço personalizado. Em geral, escrever um serviço personalizado para jogos de patch não é uma boa ideia, pois isso é complicado e propenso a erros. É recomendável que a aplicação de patch seja feita pelo uso de outros métodos discutidos neste artigo. No entanto, um serviço personalizado pode ser necessário quando combinado com soluções antifalsificação ou antipirataria. Esse serviço deve dar suporte a um grande número de jogos e ser projetado para que ele só possa baixar os arquivos de patch e gravar somente no diretório de instalação do jogo de destino. É importante que o serviço seja pequeno, tenha uma área de superfície mínima que seja vulnerável a ataques e use o mínimo de recursos do sistema possível quando o jogo não estiver em execução.

## <a name="summary"></a>Resumo

Por fim, cabe a você decidir qual método implementar. Você precisa avaliar os fatores que são importantes para você. Segurança, frequência de aplicação de patches, facilidade de uso pelo cliente, carga de trabalho necessária para implementar, complexidade de solução e conformidade de recursos de plataforma são os fatores que cada desenvolvedor deve considerar antes de decidir sobre um determinado método.

Você pode encontrar mais informações sobre a proteção de conta de usuário nos [requisitos de desenvolvimento de aplicativos do Windows Vista para UAC (controle de conta de usuário)](/previous-versions/aa905330(v=msdn.10)).

 

 
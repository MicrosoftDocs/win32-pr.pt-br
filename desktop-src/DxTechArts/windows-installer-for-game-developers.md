---
title: Windows Instalador para desenvolvedores de jogos
description: este artigo fornece uma visão geral das Windows Installer, especificamente direcionadas aos desenvolvedores de jogos. para obter a documentação detalhada sobre os recursos e as APIs mencionadas neste artigo, consulte o SDK do Windows Platform.
ms.assetid: 07401792-b34b-71c9-18f8-a11c916c7d81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc587725ce2a2a675c9db835fabb503bc44ffa62c07ee1ce80578aef9432cf9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290386"
---
# <a name="windows-installer-for-game-developers"></a>Windows Instalador para desenvolvedores de jogos

mostra como Windows Installer pode ser usado para instalar jogos em computadores de usuário final. Windows O instalador oferece suporte completo para uma interface de usuário personalizada, bem como para aplicação de patches.

Microsoft Windows Installer é a API preferida para instalar o software em computadores baseados em Windows. embora muitos dos recursos do Windows Installer sejam projetados para dar suporte à implantação de aplicativos de negócios em um ambiente corporativo, o Windows Installer também é totalmente adequado para a instalação de jogos em computadores de usuários finais. as principais vantagens de usar o Windows Installer para instalação de jogos são:

-   Desinstalação confiável
-   Capacidade de instalar conteúdo sob demanda
-   Suporte para interface do usuário totalmente personalizada
-   Aplicação de patch eficiente

este artigo fornece uma visão geral das Windows Installer, especificamente direcionadas aos desenvolvedores de jogos. para obter a documentação detalhada sobre os recursos e as APIs mencionadas neste artigo, consulte o SDK do Windows Platform.

-   [Visão geral](#overview)
-   [conceitos principais do Windows Installer](#key-windows-installer-concepts)
    -   [Componentes](#components)
    -   [Recursos](#features)
-   [Estados de instalação](#install-states)
-   [Instalar sob demanda](#install-on-demand)
-   [Interface do usuário personalizada](#custom-user-interface)
-   [Aplicação de patch](#patching)
-   [Outros recursos](#other-resources)

## <a name="overview"></a>Visão geral

todas as configurações baseadas em Windows Installer usam um arquivo de banco de dados de instalação chamado arquivo MSI para descrever como o aplicativo deve ser instalado. O arquivo MSI contém informações sobre quais arquivos, chaves do registro, atalhos de área de trabalho, associações de arquivo e outros elementos de aplicativo devem ser instalados. Os arquivos reais a serem instalados podem ser compactados no próprio arquivo MSI, agrupados e compactados em "arquivos de gabinete" separados ou armazenados em outro lugar na mídia de instalação como arquivos individuais descompactados. O arquivo MSI também pode referenciar ações personalizadas implementadas externamente, a fim de permitir ações para as quais o arquivo MSI não permite nativamente.

Um arquivo MSI pode, opcionalmente, conter uma interface do usuário para orientar o usuário durante o processo de instalação. Essa interface do usuário é adequada para a maioria dos aplicativos. no entanto, ele tem a aparência de um aplicativo Windows regular, e muitos desenvolvedores de jogos preferem que seu aplicativo de instalação mantenha a aparência do próprio jogo, a fim de fornecer uma experiência de usuário final mais consistente. para dar suporte a esse cenário de interface do usuário totalmente personalizado, um aplicativo de instalação pode desativar a interface de usuário interna do Windows Installer e manipular toda a própria interface do usuário. a API de Windows Installer expõe um mecanismo de retorno de chamada para permitir que uma interface do usuário de instalação personalizada seja notificada do progresso da instalação, bem como eventos importantes, como solicitações de alteração de disco.

Windows O instalador não é uma solução de ponta a ponta para a criação de configurações. É apenas uma API que pode ser usada por um programa de instalação para fazer a instalação real de arquivos, chaves do registro, atalhos da área de trabalho e outros elementos do aplicativo. as versões recentes de todas as principais ferramentas de configuração comercial (por exemplo, InstallShield, inteligente e Microsoft Visual Studio) dão suporte a Windows Installer. essas ferramentas fornecem interfaces de usuário convenientes para criar a configuração para um jogo, mas elas dependem da API de Windows Installer para fazer grande parte da instalação real. Essas ferramentas também podem ser usadas apenas para criar um banco de dados MSI que contém o pacote de instalação, que pode ser instalado a partir de uma interface do usuário de instalação personalizada. como alternativa a ferramentas de terceiros, a API de Windows Installer fornece todas as funções necessárias para criar e manipular um banco de dados msi programaticamente, e o SDK da plataforma de Windows inclui uma ferramenta de edição de banco de dados msi básica, chamada Orca.

## <a name="key-windows-installer-concepts"></a>conceitos principais do Windows Installer

aqui estão os componentes e recursos Windows Installer.

### <a name="components"></a>Componentes

Um aplicativo é composto de um ou mais componentes, identificados por uma ID de componente GUID. Um componente é uma unidade atômica; Ele está totalmente instalado ou não está instalado. Um componente pode consistir em um único arquivo, vários arquivos, chaves do registro, atalhos da área de trabalho ou alguma combinação deles. Os recursos (arquivos, etc.) dentro de um componente devem ser exclusivos desse componente; dois componentes não podem conter o mesmo recurso. Um componente nunca é instalado explicitamente; Ele é instalado apenas como parte de um recurso (consulte a seguir).

### <a name="features"></a>Recursos

Um recurso é um grupo de componentes, identificado por uma ID de recurso de GUID. Ao contrário dos componentes, vários recursos podem conter o mesmo componente. Um componente compartilhado entre vários recursos será instalado se algum desses recursos estiver instalado e removido somente quando todos os recursos que fazem referência ao componente tiverem sido desinstalados. A instalação de um recurso pode ser feita automaticamente como parte da instalação de um produto ou pode ser feita manualmente usando a API [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) .

embora alguns jogos tenham vários "recursos" que podem ser instalados de forma independente, o conceito de Windows Installer de um recurso ainda é útil. como um recurso de Windows Installer não é nada mais do que uma coleção de componentes que podem ser instalados juntos, os jogos podem usar recursos para agrupar todo o conteúdo necessário para um estágio específico do jogo. Por exemplo, um jogo orientado por nível pode definir um recurso por nível, consistindo em todo o conteúdo necessário para esse nível. Isso permitiria que o jogo instalasse o conteúdo um nível por vez no próprio jogo, em vez de instalar todo o conteúdo de todos os níveis durante a instalação inicial.

## <a name="install-states"></a>Estados de instalação

Cada componente ou recurso tem um estado de instalação associado, que determina se o componente ou recurso está disponível e, em caso afirmativo, onde os arquivos do componente ou recurso estão instalados. Os Estados de instalação possíveis para um recurso são:

<dl> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>Ausente
</dt> <dd>

O recurso não está instalado e, portanto, está inacessível.

</dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>Local
</dt> <dd>

O recurso está disponível e é instalado para ser executado do disco rígido local.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Original
</dt> <dd>

O recurso está disponível e é instalado para ser executado a partir da mídia de origem original (geralmente um CD ou DVD).

</dd> <dt>

<span id="Advertised"></span><span id="advertised"></span><span id="ADVERTISED"></span>Anunciados
</dt> <dd>

O recurso não está instalado, mas pode ser instalado sob demanda usando a API [**MsiConfigureFeature**](/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea) . Quando o recurso está realmente instalado, ele pode ser instalado no estado local ou de origem.

</dd> </dl>

Um componente pode ter qualquer um dos Estados acima, exceto para "anunciado". Se um componente fizer parte de um recurso anunciado, o componente será exibido como "ausente" até que o recurso seja instalado.

## <a name="install-on-demand"></a>Instalar sob demanda

Windows O instalador permite que um aplicativo marque recursos como anunciados, o que significa que o recurso ainda não está instalado, mas está disponível para instalação no tempo de execução, se necessário. A instalação de recursos em tempo de execução é conhecida como "instalar sob demanda". Os jogos podem usar a instalação sob demanda para reduzir drasticamente o tempo necessário para a configuração inicial do jogo, adiando a instalação do conteúdo do jogo até que seja necessário em tempo de execução. O atraso necessário para instalar o conteúdo em tempo de execução geralmente pode ser parcial ou completamente ocultado fazendo a instalação sob demanda em um thread em segundo plano, enquanto o usuário está ocupado com o jogo.

## <a name="custom-user-interface"></a>Interface do usuário personalizada

embora Windows Installer forneça uma interface do usuário padrão que orienta o usuário por meio da instalação do aplicativo, essa interface é parecida com a de um aplicativo de Windows padrão. Muitos desenvolvedores de jogos preferem que sua interface do usuário de instalação tenha a mesma aparência que o próprio jogo, para fornecer ao usuário um gosto do ambiance do jogo. para dar suporte a isso, Windows Installer permite que a interface do usuário interna seja completamente desabilitada, permitindo que o desenvolvedor forneça uma interface do usuário totalmente personalizada.

primeiro, o programa de instalação personalizada desabilita a interface do usuário interna Windows Installer usando a API [**MsiSetInternalUI**](/windows/desktop/api/msi/nf-msi-msisetinternalui) para definir o nível de interface de usuário como INSTALLUILEVEL \_ NONE. Em seguida, ele chama a API [**MsiSetExternalUI**](/windows/desktop/api/msi/nf-msi-msisetexternaluia) para especificar uma função de retorno de chamada que será chamada durante o processo de instalação para notificar o programa de instalação de eventos-chave durante a instalação.

O processo de instalação real é iniciado chamando a API [**MsiInstallProduct**](/windows/desktop/api/msi/nf-msi-msiinstallproducta) . Essa API aceita uma cadeia de caracteres de parâmetro que permite que o chamador especifique valores para propriedades nomeadas. Essas propriedades podem ser usadas no próprio banco de dados de instalação para personalizar como o aplicativo será instalado. Essas propriedades podem ser usadas para especificar:

-   O diretório no qual o aplicativo deve ser instalado
-   Quais recursos devem ser instalados localmente e que devem ser instalados para serem executados a partir do CD/DVD (por exemplo, para habilitar a escolha entre uma instalação mínima e uma instalação completa)
-   Se o aplicativo deve ser instalado para todos os usuários do computador ou apenas para o usuário atual

Durante a instalação, o programa de instalação usa as mensagens de notificação enviadas para sua função de retorno de chamada para determinar quando atualizar sua interface do usuário do indicador de progresso, quando solicitar que o usuário insira o próximo CD ou quando notificar o utilizador sobre um erro no processo de instalação.

## <a name="patching"></a>Aplicação de patch

Windows O instalador permite que os aplicativos instalados sejam corrigidos aplicando um arquivo de patch. Um arquivo de patch contém os novos arquivos a serem adicionados pelo patch, os arquivos que são modificados pelo patch e uma lista de alterações a serem feitas no banco de dados de instalação. Para conservar o espaço, em vez de armazenar o conteúdo completo de um arquivo alterado pelo patch, o arquivo de patch realmente contém apenas as diferenças entre a versão original do arquivo e a nova versão do arquivo.

Para criar um patch, você precisa da imagem de instalação para cada uma das versões do aplicativo do qual deseja que o patch seja atualizado, bem como a imagem de instalação para a nova versão atualizada do aplicativo. Uma imagem de instalação consiste no banco de dados MSI e em todos os arquivos reais para o aplicativo. A melhor maneira de criar uma imagem de instalação para uma nova versão do aplicativo é copiar a imagem de instalação da versão anterior do aplicativo e, em seguida, fazer as alterações necessárias para atualizar essa cópia para a versão corrigida.

Depois de ter todas as imagens de instalação necessárias, você pode criar os patches usando o Msimsp.exe, que é uma ferramenta de criação de patch disponível como parte do SDK da plataforma. A ferramenta solicitará os locais de cada uma das imagens de instalação e, em seguida, determinará como representar com eficiência as diferenças entre as versões sucessivas. A saída da ferramenta é o arquivo de patch final (identificado pela extensão MSP). Para instalar o patch programaticamente, chame a API [**MsiApplyPatch.**](/windows/desktop/api/msi/nf-msi-msiapplypatcha) O usuário também pode instalar o patch manualmente clicando duas vezes no arquivo MSP no Explorer.

## <a name="other-resources"></a>Outros recursos

-   Para obter informações detalhadas sobre a API do Windows, consulte [Windows Installer](/windows/desktop/Msi/windows-installer-portal).
-   Para obter informações sobre as práticas recomendadas para instalação de jogos, consulte [Instalação e manutenção de jogos.](/windows/desktop/DxTechArts/installation-and-maintenance-of-games)

 

 
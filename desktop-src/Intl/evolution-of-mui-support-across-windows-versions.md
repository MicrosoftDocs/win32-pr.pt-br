---
description: Evolução do suporte à MUI entre Windows versões
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Evolução do suporte à MUI entre Windows versões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e08ff181cf34daa95710d5bf57a294703a88ef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467893"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a>Evolução do suporte à MUI entre Windows versões

-   [Antes Windows Vista](#before-windows-vista)
-   [Windows Vista e Além](#windows-vista-and-beyond)
    -   [Um sistema operacional de linguagem neutra/MUI](#a-language-neutralmui-operating-system)
    -   [Os cenários de implantação são totalmente baseados em MUI](#deployment-scenarios-are-fully-mui-based)
    -   [Implantação de imagem única](#single-image-deployment)
    -   [Modelo de manutenção aprimorado](#improved-servicing-model)
    -   [Infraestrutura de MUI](#mui-infrastructure)
    -   [Gerenciamento de idiomas](#language-management)
    -   [Tratamento de recursos](#resource-handling)

## <a name="before-windows-vista"></a>Antes Windows Vista

Antes da versão do Windows Vista, o Windows era fornecido com imagens de idioma único, o que significa que cada versão localizada do Windows continha um único idioma para sua interface do usuário. A MUI era um complemento para a versão em inglês do sistema operacional e os pacotes Interface de Usuário Multilíngue só podiam ser adicionados a determinadas versões em inglês do Windows. Quando instalada na versão em inglês do Windows, a MUI permitia que o idioma da interface do usuário do sistema operacional fosse alterado de acordo com as preferências de usuários individuais para um dos idiomas com suporte.

O MUI Pack modelo não expõe o suporte de MUI para aplicativos. Embora os desenvolvedores pudessem criar aplicativos multilínguos, eles tinham que criar seus próprios mecanismos para fazer isso.

## <a name="windows-vista-and-beyond"></a>Windows Vista e Além

Com Windows Vista, a Microsoft fez um investimento significativo na MUI. Windows O Vista é criado do zero em uma plataforma de MUI. Embora isso represente um grande avanço na estratégia de localização do Windows, pois é um fator importante para a Microsoft fornecer Windows em mais idiomas do que nunca, primeiro e, em primeiro lugar, um grande avanço para Windows usuários e clientes.

### <a name="a-language-neutralmui-operating-system"></a>Um sistema operacional de linguagem neutra/MUI

A grande maioria dos Windows binários do Vista são compatíveis com a MUI e seus dados localizáveis são armazenados separadamente do código. Isso oferece flexibilidade, pois diferentes dados de linguagem podem ser adicionados a qualquer momento.

### <a name="deployment-scenarios-are-fully-mui-based"></a>Os cenários de implantação são totalmente baseados em MUI

O design de instalação e empacotamento do Windows Vista é baseado em MUI e todos os dados localizáveis são empacotados em pacotes específicos de linguagem, e cada pacote de idiomas pode ser implantado em cenários diferentes. Por exemplo, embora os DVDs de varejo do Windows Vista contenham versões de idioma único, os usuários da  edição Ultimate podem baixar pacotes de idiomas de MUI adicionais e podem alternar o idioma da interface do usuário do painel de controle Opções Regionais e de Idioma. Enterprise licenças de edição têm todos os idiomas e podem implantar qualquer um deles.

### <a name="single-image-deployment"></a>Implantação de imagem única

Enterprise clientes e OEMs agora podem reduzir o número de imagens que precisam manter para implantar Windows e aplicativos em computadores em diferentes localidades por meio da implantação de imagem única.

Com a MUI no Windows Vista, uma imagem que contém vários idiomas pode ser implantada em qualquer usuário de linguagem, e os usuários podem determinar seus próprios idiomas preferenciais (dentro da política) durante a instalação ou a "experiência inicial inicial" com o computador. Em particular, os OEMs podem colocar muitas linguagens de interface do usuário em seus novos computadores para permitir que os usuários selecionem um dos Centro de Boas-Vindas. Portanto, em uma imagem com vários pacotes de idiomas, a Instalação exibirá uma lista de idiomas disponíveis e permitirá que os usuários escolham um deles. Todas as configurações internacionais são definidas para corresponder ao idioma ou localidade selecionado.

### <a name="improved-servicing-model"></a>Modelo de manutenção aprimorado

O mesmo pacote de correção de segurança ou QFE agora pode ser instalado sobre qualquer sistema de linguagem. Isso é essencial, pois permite uma solução mais rápida de correções de segurança em particular e permite que todos os usuários internacionais se beneficiem da mesma disponibilidade de tempo de todas as correções de segurança.

### <a name="mui-infrastructure"></a>Infraestrutura de MUI

A partir do Windows Vista, as APIs de MUI estão disponíveis para permitir que os desenvolvedores aproveitem os mecanismos de MUI para seus próprios aplicativos, sem precisar criar lógica personalizada para manipulação de recursos e gerenciamento de idioma.

### <a name="language-management"></a>Gerenciamento de idiomas

As APIs de MUI base que fornecem recursos de gerenciamento de linguagem de interface do usuário estão disponíveis como parte da infraestrutura de MUI. Para ajudar a gerenciar as diferentes configurações de idioma da interface do usuário no nível do sistema, do usuário e do aplicativo, a MUI as combina internamente em uma única lista priorizada. Em seguida, a MUI implementa um mecanismo de fallback com base nessa lista priorizada, permitindo soluções de localização parciais, fornecendo aos usuários uma experiência de linguagem de interface do usuário apropriada, se não preferencial.

Por exemplo, um sistema que executa a versão em espanhol do Windows Vista com um pacote de interface de linguagem (LIP) em espanhol instalado na parte superior do sistema operacional base pode dar suporte ao seguinte comportamento: o sistema tentará exibir seus recursos em Linguiano primeiro e, se esses recursos não estão disponíveis no Espanhol, forneça ao usuário recursos em vez disso.

### <a name="resource-handling"></a>Tratamento de recursos

Com a infraestrutura de MUI aprimorada que está disponível a partir do Windows Vista, as tecnologias de recursos mais comuns são habilitadas para MUI. A tabela a seguir fornece detalhes adicionais sobre o suporte ao tratamento de recursos disponível no Windows Vista.




| Categoria | Suporte | 
|----------|---------|
| Tipos de recurso compatíveis | <ul><li>Recurso win32/não gerenciamento: .DLL/.EXE/. OCX</li><li>Registros relacionados ao shell</li><li>Recursos relacionados ao gerenciamento: log de eventos, snap-in/arquivos MSC</li><li>WMI: MOF/MFL</li><li>Política de Grupo: ADMX/ADML</li><li>Gerenciado Resources.dll</li></ul> | 
| Ferramentas de desenvolvimento | <ul><li>Para Win32: RC.exe, MUIRCT.exe e Visual Studio 2005 e posterior</li></ul> | 
| Suporte ao tipo de recurso limitado | <ul><li>Arquivos de ajuda *.chm</li></ul> | 




 

 

 




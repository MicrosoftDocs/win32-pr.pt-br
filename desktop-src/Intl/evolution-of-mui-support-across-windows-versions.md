---
description: Evolução do suporte do MUI em versões do Windows
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Evolução do suporte do MUI em versões do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b896c3651cbea3eef8f2d2021194742f24818f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810485"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a>Evolução do suporte do MUI em versões do Windows

-   [Antes do Windows Vista](#before-windows-vista)
-   [Windows Vista e posterior](#windows-vista-and-beyond)
    -   [Um sistema operacional de linguagem neutra/MUI](#a-language-neutralmui-operating-system)
    -   [Cenários de implantação são totalmente baseados em MUI](#deployment-scenarios-are-fully-mui-based)
    -   [Implantação de imagem única](#single-image-deployment)
    -   [Modelo de manutenção aprimorado](#improved-servicing-model)
    -   [Infraestrutura do MUI](#mui-infrastructure)
    -   [Gerenciamento de idioma](#language-management)
    -   [Manipulação de recursos](#resource-handling)

## <a name="before-windows-vista"></a>Antes do Windows Vista

Antes da versão Windows Vista, o Windows foi fornecido com imagens de idioma único, o que significava que cada versão localizada do Windows continha uma linguagem única para a interface do usuário. O MUI foi um complemento à versão em inglês do sistema operacional, e os pacotes de interface do usuário multilíngüe só podiam ser adicionados a determinadas versões em inglês do Windows. Quando instalado na versão em inglês do Windows, o MUI permitia que o idioma da interface do usuário do sistema operacional fosse alterado de acordo com as preferências de usuários individuais para um dos idiomas com suporte.

O modelo de MUI Pack não expôs o suporte a MUI para aplicativos. Embora os desenvolvedores pudessem criar aplicativos multilíngües, eles tinham que criar seus próprios mecanismos para fazer isso.

## <a name="windows-vista-and-beyond"></a>Windows Vista e posterior

Com o Windows Vista, a Microsoft fez um investimento significativo em MUI. O Windows Vista foi criado desde o início em uma plataforma MUI. Embora isso represente um grande avanço na estratégia de localização do Windows, uma vez que é um habilitador principal para a Microsoft fornecer janelas em mais idiomas do que nunca, é primeiro e mais importante para usuários e clientes do Windows.

### <a name="a-language-neutralmui-operating-system"></a>Um sistema operacional de linguagem neutra/MUI

A grande maioria dos binários do Windows Vista são compatíveis com o MUI e seus dados localizáveis são armazenados separadamente do código. Isso oferece flexibilidade, pois diferentes dados de idioma podem ser adicionados a qualquer momento.

### <a name="deployment-scenarios-are-fully-mui-based"></a>Cenários de implantação são totalmente baseados em MUI

O design de empacotamento e instalação do Windows Vista são baseados em MUI e todos os dados localizáveis são empacotados em pacotes específicos de idioma, e cada pacote de idiomas pode ser implantado em diferentes cenários. Por exemplo, embora os DVDs de varejo para Windows Vista contenham versões de idioma único, os usuários da edição Ultimate podem baixar pacotes de idiomas adicionais do MUI e podem alternar o idioma da interface do usuário no painel de controle **Opções regionais e de idiomas** . Os licenciados da Enterprise Edition obtêm todos os idiomas e podem implantar qualquer um deles.

### <a name="single-image-deployment"></a>Implantação de imagem única

Os clientes empresariais e os OEMs agora podem reduzir o número de imagens que precisam manter para implantar o Windows e os aplicativos em computadores em diferentes localidades por meio de implantação de imagem única.

Com o MUI no Windows Vista, uma imagem que contém vários idiomas pode ser implantada em qualquer usuário de idioma, e os usuários podem determinar suas próprias linguagens preferenciais (na política) durante a instalação ou a "experiência de uso inicial" com o computador. Em particular, os OEMs podem colocar vários idiomas da interface do usuário em seus novos computadores para permitir que os usuários selecionem um no centro de boas-vindas. Assim, de uma imagem com vários pacotes de idiomas, a instalação exibirá uma lista de idiomas disponíveis e permitirá que os usuários escolham um deles. Todas as configurações internacionais são então definidas para corresponder ao idioma ou à localidade selecionada.

### <a name="improved-servicing-model"></a>Modelo de manutenção aprimorado

O mesmo QFE ou pacote de correção de segurança agora pode ser instalado na parte superior de qualquer sistema de linguagem. Isso é essencial, pois permite um retorno mais rápido de correções de segurança em particular e permite que todos os usuários internacionais se beneficiem da disponibilidade de todas as correções de segurança.

### <a name="mui-infrastructure"></a>Infraestrutura do MUI

A partir do Windows Vista, as APIs do MUI estão disponíveis para permitir que os desenvolvedores tirem proveito dos mecanismos de MUI para seus próprios aplicativos, sem precisar criar lógica personalizada para manipulação de recursos e gerenciamento de idioma.

### <a name="language-management"></a>Gerenciamento de idioma

As APIs básicas do MUI que fornecem recursos de gerenciamento de idioma da interface do usuário estão disponíveis como parte da infraestrutura do MUI. Para ajudar a gerenciar as diferentes configurações de idioma da interface do usuário no nível do sistema, de usuários e de aplicativos, o MUI os combina internamente em uma única lista priorizada. Em seguida, o MUI implementa um mecanismo de fallback com base nessa lista priorizada, permitindo soluções de localização parcial, fornecendo aos usuários uma experiência de linguagem de interface do usuário apropriada, se não preferível.

Por exemplo, um sistema que executa a versão em espanhol do Windows Vista com um LIP (Language Interface Pack) do catalão instalado na parte superior do sistema operacional de base pode dar suporte ao seguinte comportamento: o sistema tentará exibir seus recursos em catalão primeiro e, se esses recursos não estiverem disponíveis no catalão, forneça ao usuário recursos em espanhol.

### <a name="resource-handling"></a>Manipulação de recursos

Com a infraestrutura de MUI aprimorada que está disponível a partir do Windows Vista, as tecnologias de recursos mais comuns são habilitadas para MUI. A tabela a seguir fornece detalhes adicionais sobre o suporte à manipulação de recursos disponível no Windows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Suporte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tipos de recurso compatíveis</td>
<td><ul>
<li>Recurso Win32/não gerenciado:. DLL/. EXE/. OCX</li>
<li>Registros relacionados ao shell</li>
<li>Recursos relacionados ao gerenciamento: log de eventos, snap-in/arquivos MSC</li>
<li>WMI: MOF/MFL</li>
<li>Política de Grupo: ADMX/ADML</li>
<li>Resources.dll gerenciados</li>
</ul></td>
</tr>
<tr class="even">
<td>Ferramentas de desenvolvimento</td>
<td><ul>
<li>Para Win32: RC.exe, MUIRCT.exe e Visual Studio 2005 e posterior</li>
</ul></td>
</tr>
<tr class="odd">
<td>Suporte a tipo de recurso limitado</td>
<td><ul>
<li>arquivos de ajuda *. chm</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 




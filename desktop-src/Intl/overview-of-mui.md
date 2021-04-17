---
description: Este tópico fornece uma visão geral conceitual da tecnologia MUI (Multilingual User interface), o suporte de plataforma que ele fornece para habilitar experiências de usuário multilíngues e os benefícios que ele oferece ao ecossistema do Windows.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Visão geral do MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674cb5e0fee4e7b8d3990a99f13f981c4a8c5803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564145"
---
# <a name="overview-of-mui"></a>Visão geral do MUI

Este tópico fornece uma visão geral conceitual da tecnologia MUI (Multilingual User interface), o suporte de plataforma que ele fornece para habilitar experiências de usuário multilíngues e os benefícios que ele oferece ao ecossistema do Windows.

Nessa página:

-   [A necessidade de computação multilíngue](#the-need-for-multilingual-computing)
-   [A função do MUI na habilitação da computação multilíngue](#the-role-of-mui-in-enabling-multilingual-computing)
-   [Conceitos principais do MUI](#core-concepts-of-mui)
-   [Histórico do MUI no Windows](#history-of-mui-in-windows)
-   [Benefícios da tecnologia MUI](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a>A necessidade de computação multilíngue

Para se beneficiar das oportunidades de crescimento apresentadas por mercados internacionais, as plataformas e os aplicativos da Microsoft dão suporte a mais idiomas, culturas e mercados do que nunca.

A linguagem, a cultura e as especificações de mercado ainda são extremamente relevantes para usuários internacionais, apesar de aumentar as tendências de globalização. O gráfico de pizza a seguir mostra que os palestrantes que não estão em Inglês ainda compõem 91,5% da população do mundo.

![gráfico de pizza com três segmentos; o rótulo "alto-falantes que não são do Inglês 91,5%" é muito maior do que os outros dois combinados](images/overview-of-mui-fig1.gif)

Em todo o mundo, há 193 países e mais de 6.900 idiomas de vida conhecidos em uso hoje. O inglês, apesar de sua função como a linguagem de negócios do mundo, é falado apenas em 8,5% da população do mundo como primeira ou segunda linguagem. Para fornecer informações nativas a 94% da população do mundo, essas informações precisariam estar disponíveis no 347 (cerca de 5%) das linguagens do mundo que têm pelo menos um milhão de alto-falantes. Isso é especialmente verdadeiro, pois as tendências de globalização aumentaram as expectativas desses usuários em relação à tecnologia e à sua disponibilidade em seus mercados.

A necessidade de localizar software em mais idiomas aumentou ao longo dos anos e a Microsoft agora está fornecendo o Windows Vista e outros produtos em mais idiomas do que nunca. Essa evolução é especialmente clara com o Microsoft Windows, já que deixou de dar suporte a 30 idiomas com o Windows 98 a quase 100 com o Windows Vista, conforme ilustrado no gráfico de barras a seguir.

![gráfico de barras mostrando que o número de idiomas é muito maior no Windows Vista do que no Windows 98 ou no Windows XP](images/overview-of-mui-fig2.gif)

*Figura 2 — número de idiomas com suporte das versões do Microsoft Windows*

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a>A função do MUI na habilitação da computação multilíngue

Conforme discutido na seção anterior, a [globalização](glossary-for-understanding-mui.md) e a [localização](glossary-for-understanding-mui.md) de aplicativos se tornaram uma necessidade em um mundo mais integrado globalmente. Em particular, como cada vez mais empresas estão se tornando globais, seja internamente ou por meio de suas redes comerciais, a necessidade de aplicativos multilíngües é cada vez mais significativa. Portanto, os obstáculos que essas empresas enfrentam atualmente na implantação desses aplicativos globalmente.

Fornecer suporte para mais idiomas para sistemas operacionais Windows, bem como aplicativos de software criados para a plataforma Windows, requer novas estratégias que permitem que todos os principais cenários sejam implementados com sobrecarga mínima de engenharia.

A tecnologia MUI destina-se a desenvolvedores e ISVs que visam criar e dar suporte a aplicativos multilíngües para a plataforma Windows. O MUI também é de importante importância para OEMs e empresas, que pode aproveitá-lo para implantar o sistema operacional Windows e adicionar aplicativos a computadores em diferentes idiomas por meio de implantação de imagem única.

## <a name="core-concepts-of-mui"></a>Conceitos principais do MUI

A ideia fundamental por trás do MUI é [separar o armazenamento de recursos localizáveis do código-fonte do aplicativo](mui-fundamental-concepts-explained.md), para poder arquitetar qualquer aplicativo multilíngue como uma combinação de um binário de núcleo com neutralidade de idioma e um conjunto de arquivos de recursos localizados específicos do idioma.

Depois que o código-fonte do aplicativo é armazenado separadamente dos recursos localizados, fica fácil [carregar dinamicamente os recursos localizados apropriados](mui-fundamental-concepts-explained.md) para um determinado contexto de aplicativo com base em uma lógica que leva em conta as configurações de nível de aplicativo, de usuário e de sistema para o idioma da interface do usuário.

Esses atributos fundamentais do MUI ajudam a facilitar os cenários de negócios, como:

-   Um modelo de localização aprimorado para o conteúdo da interface do usuário e da ajuda, por meio da separação física do código-fonte do aplicativo e de recursos localizáveis.
-   Tratar os recursos localizáveis como conteúdo dinâmico e carregá-los de acordo com as configurações de idioma da interface do usuário e as preferências de fallback. Isso permite cenários como:
    -   Alternando de um idioma da interface do usuário para outro em tempo de execução.
    -   Criação de imagens de implantação única regionais ou mundiais que abrangem um conjunto de idiomas para OEMs e empresas.

## <a name="history-of-mui-in-windows"></a>Histórico do MUI no Windows

O nível de suporte disponível para uma experiência de usuário multilíngüe no nível do sistema operacional Windows e para o desenvolvimento de aplicativos multilíngues na plataforma Windows evoluiu ao longo do tempo e nas diferentes versões do Windows.

A funcionalidade com suporte [antes do Windows Vista](evolution-of-mui-support-across-windows-versions.md) era bastante básica, com imagens do Windows de idioma único e uma opção para complementar pacotes de interface do usuário multilíngüe em cenários específicos. Nenhum suporte ao desenvolvedor para aplicativos multilíngues estava disponível.

[Com o Windows Vista](evolution-of-mui-support-across-windows-versions.md), a Microsoft fez um investimento significativo em MUI, e o Windows Vista foi criado desde o início em uma plataforma mui. Embora isso represente um grande avanço na estratégia de localização do Windows, como é um habilitador de chave para a Microsoft fornecer janelas em mais idiomas do que nunca, ela é primeiro e mais importante para usuários, desenvolvedores e clientes do Windows. Ele fornece vários benefícios importantes, como:

-   Um sistema operacional com neutralidade de idioma com suporte interno para o MUI.
-   Empacotamento, implantação e instalação configuráveis para dar suporte a cenários multilíngües.
-   Implantação de imagem única com vários idiomas.
-   Um modelo de manutenção aprimorado em que o código executável pode ser atualizado independentemente dos recursos.
-   Suporte ao desenvolvedor para a criação de aplicativos multilíngues.

A tabela a seguir fornece uma visão geral detalhada do suporte da plataforma Windows para o MUI:

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
<td>Versões do Windows com suporte (somente suporte para SO)</td>
<td><ul>
<li>Windows 2000 Professional</li>
<li>Família do Windows 2000 Server</li>
<li>Windows XP Professional</li>
<li>Windows XP Tablet PC Edition</li>
<li>Família Windows Server 2003</li>
<li>Windows XP Embedded</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Versões do Windows com suporte (so & suporte a aplicativos)</td>
<td><ul>
<li>Windows Vista</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Versões do Windows sem suporte</td>
<td><ul>
<li>Windows 9x</li>
<li>Windows me</li>
<li>Windows XP Home Edition</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a>Benefícios da tecnologia MUI

O MUI afeta positivamente vários aspectos do ecossistema do Windows:

-   [Benefícios para os desenvolvedores](benefits-of-mui-explained.md): vários benefícios são oferecidos aos desenvolvedores de aplicativos pela disponibilidade do suporte à API do MUI para criar aplicativos multilíngües modelados nos mesmos princípios que o suporte multilíngue no próprio sistema operacional Windows. Esses benefícios incluem:
    -   A capacidade de fornecer uma experiência de linguagem de exibição consistente com o que o próprio sistema operacional oferece.
    -   A capacidade de estender facilmente o suporte a idiomas para um aplicativo.
    -   A capacidade de manter e atender facilmente ao aplicativo.
    -   A capacidade de habilitar a implantação de imagem única de aplicativos por OEMs.
-   [Benefícios para as empresas](benefits-of-mui-explained.md): o principal benefício que o MUI oferece para empresas é a capacidade de distribuir, dar suporte e manter a mesma imagem multilíngue em todo o mundo com uma única instalação. Outro ganho significativo é a capacidade de dar suporte a áreas de trabalho multilíngues que oferecem uma interação direta com os usuários com diferentes preferências de idioma.
-   [Benefícios para os OEMs](benefits-of-mui-explained.md): o principal benefício para os OEMs é a instalação de imagem única que o MUI habilita, com suporte para vários idiomas, o que permite um gerenciamento mais eficaz do inventário. Os OEMs também se beneficiam do suporte do MUI para o desenvolvimento de aplicativos, pois permitem que eles forneçam aplicativos com valor agregado em suas imagens, ao mesmo tempo em que se beneficiam da instalação de uma única imagem, desde que esses aplicativos estejam habilitados para MUI.

 

 





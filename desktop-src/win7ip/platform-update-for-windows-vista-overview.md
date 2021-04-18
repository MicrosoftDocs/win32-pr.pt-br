---
title: Sobre a atualização da plataforma para Windows Vista
description: Fornece uma visão geral da atualização da plataforma para o Windows Vista e a atualização da plataforma para o Windows Server 2008 e seus recursos.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Atualização de plataforma para o Windows Server 2008
- Atualização da plataforma para Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bcd3e94f8784ce3d060a8e56c0b089a065d288
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105764122"
---
# <a name="about-platform-update-for-windows-vista"></a>Sobre a atualização da plataforma para Windows Vista

A atualização da plataforma para o Windows Vista e a atualização da plataforma para Windows Server 2008 são atualizações do sistema operacional do usuário final que dão suporte ao uso de tecnologias selecionadas do Windows 7 em versões anteriores do sistema operacional Windows. As atualizações incluem um conjunto de bibliotecas de tempo de execução que permitem que os desenvolvedores de aplicativos direcionem versões atuais, o Windows 7 e o Windows Server 2008 R2, bem como versões anteriores, o Windows Vista e o Windows Server 2008.

## <a name="summary-of-supported-api-by-technology"></a>Resumo da API com suporte por tecnologia

Cada tecnologia com suporte da atualização da plataforma para o Windows Vista e a atualização de plataforma para atualizações do Windows Server 2008 inclui um conjunto de APIs que podem ser usadas em um aplicativo que tem como alvo a versão anterior do Windows.

Para obter mais informações sobre como usar APIs com suporte nas atualizações em um aplicativo que tem como alvo versões anteriores do Windows, consulte [desenvolvendo aplicativos para versões anteriores do Windows](developing-applications-for-previous-versions-of-windows.md).

> [!Note]  
> Algumas APIs que estão associadas a uma tecnologia podem não ter suporte e o comportamento, o desempenho ou os requisitos para algumas APIs com suporte podem variar em versões do Windows. Para obter detalhes sobre a API com suporte para uma tecnologia específica, clique no link em uma das tabelas de resumo para ir para a seção sobre essa tecnologia.

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a>Tecnologias compatíveis com a atualização de plataforma para Windows Vista

Para obter detalhes sobre a API com suporte para uma tecnologia específica, clique no link em uma das tabelas de resumo para ir para a seção sobre essa tecnologia.

As tecnologias com suporte para o Windows Vista e o Windows XP com a atualização de plataforma para Windows Vista são mostradas na tabela a seguir.

| Tecnologia                                                                                    | Windows Vista | Windows XP |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [API de automação do Windows](#windows-automation-api)                                             | Sim           | Sim        |
| [Gráficos do Windows, biblioteca de imagens e XPS](#windows-graphics-imaging-and-xps-library)        | Sim           | Não         |
| [Biblioteca de Ribbon e Gerenciador de animação do Windows](#windows-ribbon-and-animation-manager-library) | Sim           | Não         |
| [Plataforma de dispositivos portáteis do Windows](#windows-portable-devices-platform)                       | Sim           | Não         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a>Tecnologias com suporte com a atualização de plataforma para Windows Server 2008

Para obter detalhes sobre a API com suporte para uma tecnologia específica, clique no link em uma das tabelas de resumo para ir para a seção sobre essa tecnologia.

As tecnologias com suporte para o Windows Server 2008 e o Windows Server 2003 com a atualização de plataforma para Windows Server 2008 são mostradas na tabela a seguir.

| Tecnologia                                                                                    | Windows Server 2008 | Windows Server 2003 |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [API de automação do Windows](#windows-automation-api)                                             | Sim                 | Sim                 |
| [Gráficos do Windows, biblioteca de imagens e XPS](#windows-graphics-imaging-and-xps-library)        | Sim                 | Não                  |
| [Biblioteca de Ribbon e Gerenciador de animação do Windows](#windows-ribbon-and-animation-manager-library) | Sim                 | Não                  |
| [Plataforma de dispositivos portáteis do Windows](#windows-portable-devices-platform)                       | Não                  | Não                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a>Descrições da API com suporte por tecnologia

Para obter detalhes sobre a API com suporte para uma tecnologia específica, clique no link em uma das tabelas de resumo para ir para a seção sobre essa tecnologia.

-   [API de automação do Windows](#windows-automation-api)
-   [Gráficos do Windows, biblioteca de imagens e XPS](#windows-graphics-imaging-and-xps-library)
-   [Biblioteca de Ribbon e Gerenciador de animação do Windows](#windows-ribbon-and-animation-manager-library)
-   [Plataforma de dispositivos portáteis do Windows](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a>API de automação do Windows

A API de automação do Windows 3,0 é um conjunto de DLLs e elementos de API que permitem que produtos de tecnologia assistencial (AT) forneçam melhor acesso ao computador para pessoas que têm dificuldades físicas ou cognitivas, deficiências ou deficiências. Além disso, como a API de automação do Windows 3,0 permite que os aplicativos acessem e manipulem elementos da interface do usuário de outros aplicativos, trata-se de uma tecnologia ideal para implementar ferramentas automatizadas de teste.

O Microsoft Acessibilidade Ativa (MSAA) e a automação da interface do usuário são semelhantes, pois ambos fornecem meios para expor e coletar informações sobre elementos da interface do usuário e controles para dar suporte à acessibilidade da interface do usuário e à automação de teste de software. A automação da interface do usuário é uma implementação do Windows da especificação de automação da interface do usuário. É uma tecnologia mais nova que aborda muitas das limitações do MSAA.

Para obter mais informações sobre a API de automação do Windows 3,0, consulte [API de automação do Windows: visão geral](/windows/desktop/WinAuto/windows-automation-api-overview).

A atualização de plataforma para Windows Vista e a atualização de plataforma para Windows Server 2008 dão suporte à seguinte API de automação do Windows 3,0:

-   [Microsoft Acessibilidade Ativa (MSAA)](#microsoft-active-accessibility-msaa)
-   [Automação da Interface do Usuário](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a>Edições do Windows qualificadas para as atualizações

A atualização de plataforma para Windows Vista e a atualização de plataforma para Windows Server 2008 habilitam o suporte à API de automação do Windows 3,0 nas edições do Windows mostradas na tabela a seguir.



<table>
<thead>
<tr class="header">
<th>Versão do Windows</th>
<th>Edições qualificadas para atualização</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Iniciador com SP2 (x86)<br />
Home Basic com SP2 (x86 e AMD64)<br />
Home Premium com SP2 (x86 e AMD64)<br />
Negócios com SP2 (x86 e AMD64)<br />
Enterprise com SP2 (x86 e AMD64)<br />
Ultimate com SP2 (x86 e AMD64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows XP</td>
<td><dl> Windows XP Home com SP3 (x86)<br />
Windows XP Professional com SP3 (x86)<br />
</dl></td>
</tr>
<tr class="odd">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 com SP2 (x86 e AMD64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2003</td>
<td><dl> Windows Server 2003 com SP2 (x86 e AMD64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a>Microsoft Acessibilidade Ativa (MSAA)

O Microsoft Acessibilidade Ativa (MSAA) é uma tecnologia herdada que foi introduzida pela primeira vez com o Windows 95. É um conjunto de APIs que melhora o modo como os produtos de tecnologia assistencial (em) funcionam com aplicativos em execução no Microsoft Windows. A API fornece interfaces e métodos de programação para expor informações sobre elementos da interface do usuário.

Para obter mais informações sobre o Microsoft Acessibilidade Ativa, consulte a [visão geral técnica](/windows/desktop/WinAuto/technical-overview).

### <a name="supported-microsoft-active-accessibility-api-elements"></a>Elementos da API do Microsoft Acessibilidade Ativa com suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.

### <a name="ui-automation"></a>Automação da Interface de Usuário

A automação da interface do usuário é uma tecnologia mais nova que implementa a especificação de automação da interface do usuário e aborda muitas das limitações do Microsoft Acessibilidade Ativa. É um conjunto de APIs que fornece acesso programático aos elementos de interface do usuário dos aplicativos. A API fornecida ajuda produtos de tecnologia assistencial e ferramentas de teste automatizadas a acessar, identificar e manipular os elementos de interface do usuário padrão e personalizados de um aplicativo.

Para obter mais informações sobre automação da interface do usuário, consulte [API de automação do Windows: automação da interface do usuário](../winauto/entry-uiauto-win32.md).

### <a name="supported-ui-automation-api-elements"></a>Elementos da API de automação da interface do usuário com suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.

### <a name="running-ui-automation-on-previous-windows-versions"></a>Executando a automação da interface do usuário em versões anteriores do Windows

Devido às diferenças em como os controles comuns e os controles padrão do Windows são implementados em diferentes versões do Windows, pode haver pequenas diferenças nas informações que os proxies de automação da interface do usuário recuperam para esses controles de uma versão para outra.

### <a name="windows-graphics-imaging-and-xps-library"></a>Gráficos do Windows, biblioteca de imagens e XPS

A atualização da plataforma para o Windows Vista dá suporte às seguintes APIs do Windows 7 a partir da biblioteca de gráficos, imagens e XPS do Windows:

-   [Direct2D](#direct2d)
-   [Direct3D](#direct3d)
-   [DirectWrite](#directwrite)
-   [Empacotamento](#packaging)
-   [Windows Imaging Component](#windows-imaging-component)
-   [Documento XPS](#xps-document)
-   [Impressão XPS](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a>Edições do Windows qualificadas para as atualizações

A atualização da plataforma para o Windows Vista e a atualização da plataforma para Windows Server 2008 habilitam gráficos do Windows, imagens e suporte à biblioteca XPS nas edições do Windows mostradas na tabela a seguir.



<table>
<thead>
<tr class="header">
<th>Versão do Windows</th>
<th>Edições qualificadas para atualização</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Iniciador com SP2 (x86)<br />
Home Basic com SP2 (x86 e AMD64)<br />
Home Premium com SP2 (x86 e AMD64)<br />
Negócios com SP2 (x86 e AMD64)<br />
Enterprise com SP2 (x86 e AMD64)<br />
Ultimate com SP2 (x86 e AMD64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 com SP2 (x86 e AMD64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a>Direct2D

A API do Direct2D é uma nova API de gráficos de modo imediato e acelerada por hardware que fornece alto desempenho e renderização de alta qualidade para geometria, bitmaps e texto 2D. A API Direct2D foi projetada para interoperar bem com o código existente que usa GDI, GDI+ ou Direct3D.

Para obter mais informações sobre o Direct2D, consulte [about Direct2D](/windows/desktop/Direct2D/direct2d-overview).

### <a name="supported-direct2d-api-elements"></a>Elementos da API Direct2D com suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.

### <a name="running-direct2d-on-previous-windows-versions"></a>Executando o Direct2D em versões anteriores do Windows

Se o driver do WDDM 1,1 estiver faltando no Windows Vista, o desempenho da interoperabilidade Direct2D/GDI degrada.

### <a name="direct3d"></a>Direct3D

A atualização de plataforma para o Windows Vista fornece suporte de superfície BGRA para caminhos de código Direct3D10 e Direct3D 10.1. O Direct3D10Level9 permite que a funcionalidade Direct3D10 funcione em hardware de Direct3D9. O Direct3D WARP10 é um rasterizador de software de alto desempenho para aplicativos Direct3D10. O Direct3D11, a versão mais recente do Direct3D, fornece novos recursos, como suporte a multithread aprimorado, mosaico, funcionalidade de DirectCompute e vinculação dinâmica de sombreador.

Se você criar aplicativos que usam o Direct3D, o [SDK do DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) é necessário.

Para obter mais informações sobre o Direct3D, consulte [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .

### <a name="supported-direct3d-api-elements"></a>Elementos de API do Direct3D com suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.

### <a name="directwrite"></a>DirectWrite

A API DirectWrite é uma nova API de texto que fornece várias camadas de funcionalidade, incluindo layout de texto, processamento de scripts, renderização de glifos e sistema de fontes. O DirectWrite usa fontes OpenType e renderização de ClearType de sub-pixel para aprimorar a experiência de texto fornecida pelos aplicativos. A renderização de texto é acelerada pelo hardware quando usada com Direct2D.

Para obter mais informações sobre DirectWrite, consulte [Introducing DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).

### <a name="supported-directwrite-api-elements"></a>Elementos da API DirectWrite com suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.

### <a name="running-directwrite-on-previous-windows-versions"></a>Executando o DirectWrite em versões anteriores do Windows

Os seguintes problemas comportamentais podem afetar o uso da API DirectWrite em versões anteriores do Windows:

-   Os scripts novos para o Windows 7 podem não ser renderizados totalmente corretamente em versões anteriores do Windows.
-   As localidades não disponíveis nas versões anteriores do Windows retornam ao comportamento padrão.
-   O sintonizador ClearType não está disponível em versões anteriores do Windows.
-   A interoperabilidade GDI tem um custo de memória maior em alguns cenários em versões anteriores do Windows.

### <a name="packaging"></a>Empacotamento

A atualização de plataforma para o Windows Vista dá suporte a um subconjunto limitado de APIs de empacotamento que são necessárias para executar tarefas com a API de documento XPS em aplicativos não gerenciados.

Para obter mais informações sobre APIs de empacotamento, consulte a [visão geral da API de empacotamento](/previous-versions/windows/desktop/opc/packaging-api-overview).

### <a name="supported-packaging-api-elements"></a>Elementos da API de empacotamento com suporte

Há suporte apenas para as seguintes interfaces de empacotamento:

-   IOpcUri
-   IOpcPartUri
-   IOpcFactory (há suporte apenas para os métodos a seguir)
    -   CreatePackageRootUri
    -   CreatePartUri
    -   CreateStreamOnFile

APIs de empacotamento com suporte podem ser usadas para criar fluxos em arquivos, bem como para criar e interagir com o URI baseado em pacote.

### <a name="running-packaging-api-on-previous-windows-versions"></a>Executando a API de empacotamento em versões anteriores do Windows

O comportamento e o desempenho de interfaces e métodos de empacotamento com suporte são os mesmos em todas as plataformas com suporte.

Se um aplicativo tentar instanciar ou chamar uma interface ou um método de empacotamento sem suporte, a tentativa falhará. Se a chamada for para um método [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) sem suporte, o código de \_ erro E NOTIMPL será retornado.

### <a name="windows-imaging-component"></a>Windows Imaging Component

Os novos recursos do Windows Imaging Component (WIC) incluem segurança aprimorada, suporte para alta cor e melhor interoperabilidade de metadados. Além disso, o Windows Imaging Component amplia sua conformidade com os padrões fornecendo suporte para decodificação de imagem progressiva, recursos de PNG expandidos, metadados GIF, atualizações de foto de HD e metadados que abrangem segmentos APPn.

Para obter mais informações sobre o Windows Imaging Component, consulte a [visão geral do Windows Imaging Component](/windows/desktop/wic/-wic-about-windows-imaging-codec).

### <a name="supported-wic-api-elements"></a>Elementos de API do WIC com suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.

### <a name="xps-document"></a>Documento XPS

As APIs de documento XPS dão suporte à criação, modificação e salvamento de documentos XPS em aplicativos não gerenciados

Para obter mais informações sobre APIs de documento XPS, consulte o [Guia de programação de documento XPS.](/previous-versions//dd372978(v=vs.85))

### <a name="supported-xps-document-api-elements"></a>Elementos de API de documento XPS com suporte

Somente as interfaces de [assinaturas digitais XPS](/previous-versions/windows/desktop/dd372947(v=vs.85)) não têm suporte em versões de sistema operacional de nível inferior.

### <a name="xps-print"></a>Impressão XPS

As APIs de impressão do XPS dão suporte à impressão de documentos XPS de aplicativos baseados no Windows.

Para obter mais informações sobre APIs de impressão do XPS, consulte a [API do XpsPrint](/windows/desktop/printdocs/xpsprint-api).

### <a name="supported-xps-print-api-elements"></a>Elementos da API de impressão XPS com suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.

### <a name="windows-ribbon-and-animation-manager-library"></a>Biblioteca de Ribbon e Gerenciador de animação do Windows

A atualização da plataforma para o Windows Vista dá suporte às seguintes APIs do Windows 7 na faixa de opções e na biblioteca de animações do Windows:

-   [Estrutura da faixa de dasgem do Windows](#windows-ribbon-and-animation-manager-library)
-   [Gerenciador de animação do Windows](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a>Edições do Windows qualificadas para as atualizações

A atualização da plataforma para o Windows Vista e a atualização da plataforma para o Windows Server 2008 habilite o suporte da faixa de opções do Windows e da biblioteca do Gerenciador de animação nas edições do Windows mostradas na tabela a seguir.



<table>
<thead>
<tr class="header">
<th>Versão do Windows</th>
<th>Edições qualificadas para atualização</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Iniciador com SP2 (x86)<br />
Home Basic com SP2 (x86 e AMD64)<br />
Home Premium com SP2 (x86 e AMD64)<br />
Negócios com SP2 (x86 e AMD64)<br />
Enterprise com SP2 (x86 e AMD64)<br />
Ultimate com SP2 (x86 e AMD64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 com SP2 (x86 e AMD64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a>Estrutura da faixa de dasgem do Windows

A estrutura de faixa de ferramentas do Windows (faixa de ferramentas) é um sistema de apresentação de comando avançado que fornece uma alternativa moderna para os menus, barras de tarefas e painéis de tarefa de aplicativos tradicionais do Windows.

A estrutura é uma coleção de APIs do Microsoft Win32 que fornece um host de novos recursos de interface do usuário para desenvolvedores do Windows e inclui a faixa de opções e um sistema de menus de contexto.

Para obter mais informações sobre a estrutura da faixa de faixas, consulte [Introducing the Windows Ribbon Framework](../windowsribbon/windowsribbon-introduction.md).

### <a name="supported-ribbon-framework-api-elements"></a>Elementos da API da estrutura da faixa de faixas com suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.

### <a name="windows-animation-manager"></a>Gerenciador de animação do Windows

O Windows Animation Manager (animação do Windows) é uma interface programática que dá suporte à animação de elementos visuais de aplicativos do Windows. A animação do Windows foi projetada para simplificar o desenvolvimento e a manutenção de sequências de animação e permitir que os desenvolvedores implementem animações que são consistentes e intuitivas. A animação do Windows pode ser usada com qualquer plataforma gráfica, incluindo Direct2D, Direct3D ou GDI+.

A animação do Windows é uma API COM de thread único que fornece tudo o que um desenvolvedor precisa para criar, gerenciar e orientar a animação da interface do usuário.

Para obter mais informações sobre o Gerenciador de animação do Windows, consulte [introdução à animação do Windows](/windows/desktop/UIAnimation/introducing-windows-animation-manager).

### <a name="supported-animation-manager-api-elements"></a>Elementos da API do Gerenciador de animação com suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.

### <a name="windows-portable-devices-platform"></a>Plataforma de dispositivos portáteis do Windows

A atualização da plataforma para o Windows Vista dá suporte às extensões do Windows 7 para a plataforma de dispositivos portáteis do Windows (WPD). Esse recurso permite que os computadores se comuniquem com dispositivos de mídia e armazenamento anexados. O WPD fornece uma maneira flexível e robusta para que os computadores se comuniquem com câmeras digitais, players de música, celulares e muitos outros tipos de dispositivos conectados.

Para obter mais informações sobre dispositivos portáteis do Windows, consulte [dispositivos portáteis do Windows](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .

### <a name="windows-editions-eligible-for-the-updates"></a>Edições do Windows qualificadas para as atualizações

A atualização da plataforma para o Windows Vista e a atualização da plataforma para Windows Server 2008 habilitam o suporte a dispositivos portáteis do Windows (WPD) nas edições do Windows mostradas na tabela a seguir.



<table>
<thead>
<tr class="header">
<th>Versão do Windows</th>
<th>Edições qualificadas para atualização</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Iniciador com SP2 (x86)<br />
Home Basic com SP2 (x86 e AMD64)<br />
Home Premium com SP2 (x86 e AMD64)<br />
Negócios com SP2 (x86 e AMD64)<br />
Enterprise com SP2 (x86 e AMD64)<br />
Ultimate com SP2 (x86 e AMD64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a>Elementos de API WPD com suporte

A tabela a seguir identifica os recursos com suporte para o Windows 7, Windows Vista e Windows Vista com a atualização de plataforma para versões do Windows Vista do sistema operacional Windows.

| Recurso WPD                    | Windows 7 | Windows Vista | Windows Vista com atualização de plataforma para Windows Vista |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| MTP sobre USB                   | Sim       | Sim           | Sim                                                  |
| MTP sobre IP                    | Sim       | Sim           | Sim                                                  |
| MTP em Bluetooth             | Sim       | Não            | Sim                                                  |
| Serviços de dispositivos WPD e MTP    | Sim       | Não            | Sim                                                  |
| Automação WPD                 | Sim       | Não            | Não                                                   |
| Multifuncional/multi-transporte | Sim       | Não            | Não                                                   |
| Device Stage                   | Sim       | Não            | Não                                                   |
| Plataforma de sincronização de dispositivo           | Sim       | Não            | Não                                                   |



 

Para edições do Windows 7 e do Windows Vista que não têm o Microsoft Windows Media Player instalado por padrão (as edições N e KN), você deve instalar o [SDK do Windows Media Format 11]( ../audio-and-video.md) ( https://msdn.microsoft.com/windows/bb190326.aspx) para habilitar a funcionalidade WPD. Para obter mais informações, consulte o [artigo da base de dados de conhecimento](https://support.microsoft.com/kb/953693) ( https://go.microsoft.com/fwlink/p/?linkid=158715) , que foi publicado originalmente como uma resolução para o Windows Vista.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atualização da plataforma para Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Visões gerais**
</dt> <dt>

[Sobre a atualização da plataforma para Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Artigo da base de dados de conhecimento sobre a atualização da plataforma para Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 
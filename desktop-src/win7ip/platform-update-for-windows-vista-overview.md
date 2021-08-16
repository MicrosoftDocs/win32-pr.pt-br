---
title: Sobre a atualização de plataforma para Windows Vista
description: Fornece uma visão geral da Atualização de Plataforma para Windows Vista e a Atualização de Plataforma para Windows Server 2008 e seus recursos.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Atualização de plataforma para Windows Server 2008
- Atualização de plataforma para Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9751331bf764ee486afe20a9dccd7f6b4691fee15e5000ccf8157561656409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964565"
---
# <a name="about-platform-update-for-windows-vista"></a>Sobre a atualização de plataforma para Windows Vista

A Atualização de Plataforma para Windows Vista e a Atualização da Plataforma para o Windows Server 2008 são atualizações do sistema operacional do usuário final que suportam o uso de tecnologias do Windows 7 selecionadas em versões anteriores do sistema operacional Windows. As atualizações incluem um conjunto de bibliotecas de runtime que permitem aos desenvolvedores de aplicativos direcionar versões atuais, Windows 7 e Windows Server 2008 R2, bem como versões anteriores, Windows Vista e Windows Server 2008.

## <a name="summary-of-supported-api-by-technology"></a>Resumo da API com suporte por tecnologia

Cada tecnologia com suporte da Atualização de Plataforma para o Windows Vista e a Atualização de Plataforma para atualizações do Windows Server 2008 inclui um conjunto de API que pode ser usado em um aplicativo destinado à versão anterior do Windows.

Para obter mais informações sobre como usar APIs com suporte nas atualizações em um aplicativo destinado a versões anteriores do Windows, consulte Desenvolvendo aplicativo para versões anteriores [do Windows](developing-applications-for-previous-versions-of-windows.md).

> [!Note]  
> Algumas APIs associadas a uma tecnologia podem não ter suporte e o comportamento, o desempenho ou os requisitos para algumas APIs com suporte podem variar entre Windows versões. Para obter detalhes sobre a API com suporte para uma tecnologia específica, clique no link em uma das tabelas de resumo para acessar a seção sobre essa tecnologia.

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a>Tecnologias com suporte com atualização de plataforma para Windows Vista

Para obter detalhes sobre a API com suporte para uma tecnologia específica, clique no link em uma das tabelas de resumo para acessar a seção sobre essa tecnologia.

As tecnologias com suporte para Windows Vista e Windows XP com a Atualização de Plataforma para Windows Vista são mostradas na tabela a seguir.

| Tecnologia                                                                                    | Windows Vista | Windows XP |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [Windows API de Automação](#windows-automation-api)                                             | Sim           | Sim        |
| [Windows Gráficos, imagens e biblioteca XPS](#windows-graphics-imaging-and-xps-library)        | Sim           | Não         |
| [Windows Biblioteca do Gerenciador de Animação e Faixa de Opções](#windows-ribbon-and-animation-manager-library) | Sim           | Não         |
| [Windows Plataforma de Dispositivos Portáteis](#windows-portable-devices-platform)                       | Sim           | Não         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a>Tecnologias com suporte com a Atualização de Plataforma para Windows Server 2008

Para obter detalhes sobre a API com suporte para uma tecnologia específica, clique no link em uma das tabelas de resumo para acessar a seção sobre essa tecnologia.

As tecnologias com suporte para o Windows Server 2008 e o Windows Server 2003 com a Atualização de Plataforma para o Windows Server 2008 são mostradas na tabela a seguir.

| Tecnologia                                                                                    | Windows Server 2008 | Windows Server 2003 |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [Windows API de Automação](#windows-automation-api)                                             | Sim                 | Sim                 |
| [Windows Gráficos, imagens e biblioteca XPS](#windows-graphics-imaging-and-xps-library)        | Sim                 | Não                  |
| [Windows Biblioteca do Gerenciador de Animação e Faixa de Opções](#windows-ribbon-and-animation-manager-library) | Sim                 | Não                  |
| [Windows Plataforma de Dispositivos Portáteis](#windows-portable-devices-platform)                       | Não                  | Não                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a>Descrições da API com suporte por tecnologia

Para obter detalhes sobre a API com suporte para uma tecnologia específica, clique no link em uma das tabelas de resumo para acessar a seção sobre essa tecnologia.

-   [Windows API de Automação](#windows-automation-api)
-   [Windows Gráficos, imagens e biblioteca XPS](#windows-graphics-imaging-and-xps-library)
-   [Windows Biblioteca do Gerenciador de Animação e Faixa de Opções](#windows-ribbon-and-animation-manager-library)
-   [Windows Plataforma de Dispositivos Portáteis](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a>Windows API de Automação

Windows A API de Automação 3.0 é um conjunto de DLLs e elementos de API que permitem que os produtos da AT (Tecnologia Adaptativa) forneçam melhor acesso ao computador para pessoas com dificuldades físicas ou cognitivas, deficiências ou deficiências. Além disso, como Windows API de Automação 3.0 permite que os aplicativos acessem e manipulem os elementos da interface do usuário de outros aplicativos, essa é uma tecnologia ideal para implementar ferramentas de teste automatizados.

Microsoft Active Accessibility (MSAA) e Automação da Interface do Usuário são semelhantes, pois ambos fornecem um meio para expor e coletar informações sobre elementos e controles de interface do usuário para dar suporte à acessibilidade da interface do usuário e à automação de teste de software. Automação da Interface do Usuário é uma implementação Windows da especificação Automação da Interface do Usuário dados. É uma tecnologia mais nova que aborda muitas das limitações da MSAA.

Para obter mais informações sobre a API Windows Automação 3.0, consulte [API Windows automação: visão geral.](/windows/desktop/WinAuto/windows-automation-api-overview)

A Atualização da Plataforma para Windows Vista e a Atualização da Plataforma para Windows Server 2008 são suportadas pelas seguintes APIs de Automação Windows 3.0:

-   [Microsoft Active Accessibility (MSAA)](#microsoft-active-accessibility-msaa)
-   [Automação da Interface do Usuário](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Edições Qualificadas para as Atualizações

A Atualização da Plataforma para Windows Vista e a Atualização da Plataforma para o Windows Server 2008 habilitam o suporte à API de Automação do Windows 3.0 nas edições Windows mostradas na tabela a seguir.



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
<td><dl> Starter com SP2 (x86)<br />
Home Basic com SP2 (x86 e amd64)<br />
Home Premium com SP2 (x86 e amd64)<br />
Negócios com SP2 (x86 e amd64)<br />
Enterprise com SP2 (x86 e amd64)<br />
Ultimate com SP2 (x86 e amd64)<br />
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
<td><dl> Windows Servidor 2008 com SP2 (x86 e amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2003</td>
<td><dl> Windows Servidor 2003 com SP2 (x86 e amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a>Microsoft Active Accessibility (MSAA)

Microsoft Active Accessibility (MSAA) é uma tecnologia herdado que foi introduzida pela primeira vez com Windows 95. É um conjunto de APIs que melhora a maneira como os produtos da AT (Tecnologia Adaptativa) funcionam com aplicativos em execução no Microsoft Windows. A API fornece interfaces de programação e métodos para expor informações sobre elementos de interface do usuário.

Para obter mais informações sobre Microsoft Active Accessibility, consulte Visão [geral técnica.](/windows/desktop/WinAuto/technical-overview)

### <a name="supported-microsoft-active-accessibility-api-elements"></a>Elementos de API Microsoft Active Accessibility suporte

Todas as APIs têm suporte em versões anteriores do Windows que são qualificadas para a Atualização de Plataforma para Windows Vista ou a Atualização de Plataforma para Windows Server 2008.

### <a name="ui-automation"></a>Automação da Interface de Usuário

Automação da Interface do Usuário é uma tecnologia mais nova que implementa a especificação Automação da Interface do Usuário e aborda muitas das limitações de Microsoft Active Accessibility. É um conjunto de APIs que fornece acesso programático aos elementos de interface do usuário de aplicativos. A API fornecida ajuda produtos de Tecnologia Adaptativa e ferramentas de teste automatizado acessam, identificam e manipulam os elementos de interface do usuário padrão e personalizados de um aplicativo.

Para obter mais informações sobre Automação da Interface do Usuário, consulte [API de Automação Windows: Automação da Interface do Usuário](../winauto/entry-uiauto-win32.md).

### <a name="supported-ui-automation-api-elements"></a>Elementos de API Automação da Interface do Usuário suporte

Todas as APIs têm suporte em versões anteriores do Windows que são qualificadas para a Atualização de Plataforma para Windows Vista ou a Atualização de Plataforma para Windows Server 2008.

### <a name="running-ui-automation-on-previous-windows-versions"></a>Executando Automação da Interface do Usuário em versões Windows anteriores

Devido às diferenças em como os controles comuns e os controles padrão Windows são implementados em diferentes versões do Windows, pode haver pequenas diferenças nas informações que os proxies Automação da Interface do Usuário recuperam para esses controles de uma versão para outra.

### <a name="windows-graphics-imaging-and-xps-library"></a>Windows Gráficos, imagens e biblioteca XPS

A Atualização de Plataforma para Windows Vista dá suporte às seguintes APIs Windows 7 da biblioteca Windows Graphics, Imaging e XPS:

-   [Direct2D](#direct2d)
-   [Direct3D](#direct3d)
-   [DirectWrite](#directwrite)
-   [Empacotamento](#packaging)
-   [Windows Imaging Component](#windows-imaging-component)
-   [Documento XPS](#xps-document)
-   [XPS Print](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Edições Qualificadas para as Atualizações

A Atualização de Plataforma para Windows Vista e a Atualização da Plataforma para Windows Server 2008 permitem o suporte Windows Graphics, Imaging e XPS Library nas edições do Windows mostradas na tabela a seguir.



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
<td><dl> Starter com SP2 (x86)<br />
Home Basic com SP2 (x86 e amd64)<br />
Home Premium com SP2 (x86 e amd64)<br />
Negócios com SP2 (x86 e amd64)<br />
Enterprise com SP2 (x86 e amd64)<br />
Ultimate com SP2 (x86 e amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Servidor 2008 com SP2 (x86 e amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a>Direct2D

A API Direct2D é uma nova API de gráficos 2D acelerada por hardware e modo imediato que fornece renderização de alto desempenho e alta qualidade para geometria, bitmaps e texto 2D. A API Direct2D é projetada para interoperar bem com o código existente que usa GDI, GDI+ ou Direct3D.

Para obter mais informações sobre Direct2D, consulte [Sobre Direct2D](/windows/desktop/Direct2D/direct2d-overview).

### <a name="supported-direct2d-api-elements"></a>Elementos de API Direct2D suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a Atualização de Plataforma para Windows Vista ou a Atualização de Plataforma para Windows Server 2008.

### <a name="running-direct2d-on-previous-windows-versions"></a>Executando Direct2D em versões Windows anteriores

Se o driver WDDM 1.1 estiver ausente no Windows Vista, o desempenho da interoperabilidade Direct2D/GDI será degradado.

### <a name="direct3d"></a>Direct3D

A Atualização de Plataforma para Windows Vista fornece suporte à superfície BGRA para caminhos de código Direct3D10 e Direct3D10.1. O Direct3D10Level9 permite que a funcionalidade direct3D10 funcione no hardware Direct3D9. Direct3D WARP10 é um rasterizador de software de desempenho para aplicativos Direct3D10. O Direct3D11, a versão mais recente do Direct3D, fornece novos recursos, como suporte a multithreading aprimorado, mosaico, funcionalidade do DirectCompute e vinculação dinâmica do sombreador.

Se você criar aplicativos que usam o Direct3D, o [SDK do DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) será necessário.

Para obter mais informações sobre o Direct3D, [consulte Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .

### <a name="supported-direct3d-api-elements"></a>Elementos de API direct3D com suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a Atualização de Plataforma para Windows Vista ou a Atualização de Plataforma para Windows Server 2008.

### <a name="directwrite"></a>DirectWrite

A API DirectWrite é uma nova API de texto que fornece várias camadas de funcionalidade, incluindo layout de texto, processamento de script, renderização de glifo e o sistema de fontes. DirectWrite usa fontes OpenType e renderização ClearType de sub pixel para aprimorar a experiência de texto fornecida pelos aplicativos. A renderização de texto é acelerada por hardware quando usada com Direct2D.

Para obter mais informações sobre DirectWrite, consulte [Introdução DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).

### <a name="supported-directwrite-api-elements"></a>Elementos de API DirectWrite suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a Atualização de Plataforma para Windows Vista ou a Atualização de Plataforma para Windows Server 2008.

### <a name="running-directwrite-on-previous-windows-versions"></a>Executando DirectWrite em versões Windows anteriores

Os seguintes problemas comportamentais podem afetar o uso de DirectWrite API em versões Windows anteriores:

-   Scripts novos para Windows 7 podem não renderizar totalmente corretamente nas versões Windows anteriores.
-   As localidades não disponíveis nas versões Windows anteriores se enquadram no comportamento padrão.
-   O ClearType Tuner não está disponível nas versões Windows anteriores.
-   A interoperabilidade de GDI tem um custo de memória mais alto em alguns cenários nas versões Windows anteriores.

### <a name="packaging"></a>Empacotamento

A Atualização de Plataforma para Windows Vista dá suporte a um subconjunto limitado das APIs de Empacotamento que são necessárias para executar tarefas com a API de Documento XPS em aplicativos não gerenciamento.

Para obter mais informações sobre APIs de empacotamento, consulte Visão [geral da API de empacotamento](/previous-versions/windows/desktop/opc/packaging-api-overview).

### <a name="supported-packaging-api-elements"></a>Elementos da API de empacotamento com suporte

Há suporte apenas para as seguintes interfaces de empacotamento:

-   IOpcUri
-   IOpcPartUri
-   IOpcFactory (há suporte apenas para os métodos a seguir)
    -   CreatePackageRootUri
    -   CreatePartUri
    -   CreateStreamOnFile

ApIs de empacotamento com suporte podem ser usadas para criar fluxos por arquivos, bem como para criar e interagir com o URI baseado em pacote.

### <a name="running-packaging-api-on-previous-windows-versions"></a>Executando a API de Empacotamento em versões Windows anteriores

O comportamento e o desempenho de métodos e interfaces de empacotamento com suporte são os mesmos em todas as plataformas com suporte.

Se um aplicativo tentar inferência ou chamar um método ou interface de empacotamento sem suporte, a tentativa falhará. Se a chamada for para um método [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) sem suporte, o código de erro E \_ NOTIMPL será retornado.

### <a name="windows-imaging-component"></a>Windows Imaging Component

Os novos recursos para o WIC (Windows de geração de dados) incluem segurança aprimorada, suporte para alta cor e melhor interoperabilidade de metadados. Além disso, o componente Windows Imaging amplia sua conformidade de padrões fornecendo suporte para decodificação de imagem progressiva, recursos de PNG expandidos, metadados GIF, , atualizações de HD Photo e metadados que abrangem segmentos APPn.

Para obter mais informações sobre o Windows de imagens, consulte a Visão [geral Windows componente de imagens.](/windows/desktop/wic/-wic-about-windows-imaging-codec)

### <a name="supported-wic-api-elements"></a>Elementos da API WIC com suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a Atualização de Plataforma para Windows Vista ou a Atualização de Plataforma para Windows Server 2008.

### <a name="xps-document"></a>Documento XPS

As APIs de Documento XPS são suportadas pela criação, modificação e economia de documentos XPS em aplicativos não planejados

Para obter mais informações sobre APIs de documento XPS, consulte o Guia [de Programação de Documentos XPS.](/previous-versions//dd372978(v=vs.85))

### <a name="supported-xps-document-api-elements"></a>Elementos de API de documento XPS com suporte

Somente as [interfaces de Assinaturas](/previous-versions/windows/desktop/dd372947(v=vs.85)) Digitais XPS não têm suporte em versões de sistema operacional de nível inferior.

### <a name="xps-print"></a>XPS Print

As APIs de Impressão XPS suportam a impressão de documentos XPS de Windows baseados em aplicativos.

Para obter mais informações sobre APIs de impressão XPS, consulte a [API xpsPrint.](/windows/desktop/printdocs/xpsprint-api)

### <a name="supported-xps-print-api-elements"></a>Elementos da API de Impressão XPS com suporte

Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a Atualização de Plataforma para Windows Vista ou a Atualização de Plataforma para Windows Server 2008.

### <a name="windows-ribbon-and-animation-manager-library"></a>Windows Biblioteca do Gerenciador de Animação e Faixa de Opções

A Atualização de Plataforma para Windows Vista dá suporte às seguintes APIs Windows 7 da Faixa de Opções Windows e Biblioteca de Animação:

-   [Windows Estrutura da Faixa de Opções](#windows-ribbon-and-animation-manager-library)
-   [Windows Gerenciador de Animação](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Edições Qualificadas para as Atualizações

A Atualização de Plataforma para Windows Vista e a Atualização da Plataforma para o Windows Server 2008 habilitam o suporte à Faixa de Opções do Windows e à Biblioteca do Gerenciador de Animação nas edições Windows mostradas na tabela a seguir.



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
<td><dl> Starter com SP2 (x86)<br />
Home Basic com SP2 (x86 e amd64)<br />
Home Premium com SP2 (x86 e amd64)<br />
Negócios com SP2 (x86 e amd64)<br />
Enterprise com SP2 (x86 e amd64)<br />
Ultimate com SP2 (x86 e amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Servidor 2008 com SP2 (x86 e amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a>Windows Estrutura da Faixa de Opções

a estrutura da faixa de opção da Windows (ribbon) é um sistema de apresentação de comando avançado que fornece uma alternativa moderna para os menus, barras de ferramentas e painéis de tarefas em camadas de aplicativos tradicionais de Windows.

a estrutura é uma coleção de APIs do Microsoft Win32 que fornece um host de novos recursos de interface do usuário para Windows desenvolvedores e inclui a faixa de opções e um sistema de menus de contexto.

para obter mais informações sobre a estrutura da faixa de faixas, consulte [introducing the Windows ribbon framework](../windowsribbon/windowsribbon-introduction.md).

### <a name="supported-ribbon-framework-api-elements"></a>Elementos da API da estrutura da faixa de faixas com suporte

todas as APIs têm suporte em versões anteriores do Windows que são elegíveis para a atualização da plataforma para Windows Vista ou a atualização de plataforma para Windows Server 2008.

### <a name="windows-animation-manager"></a>Windows Gerenciador de animação

o gerenciador de animação de Windows (Windows animação) é uma interface programática que dá suporte à animação de elementos visuais de aplicativos de Windows. Windows A animação foi projetada para simplificar o desenvolvimento e a manutenção de sequências de animação e para permitir que os desenvolvedores implementem animações que são consistentes e intuitivas. Windows a animação pode ser usada com qualquer plataforma gráfica, incluindo Direct2D, Direct3D ou GDI+.

Windows A animação é uma API COM de thread único que fornece tudo o que um desenvolvedor precisa para criar, gerenciar e orientar a animação da interface do usuário.

para obter mais informações sobre o gerenciador de animação Windows, consulte [introdução Windows animação](/windows/desktop/UIAnimation/introducing-windows-animation-manager).

### <a name="supported-animation-manager-api-elements"></a>Elementos da API do Gerenciador de animação com suporte

todas as APIs têm suporte em versões anteriores do Windows que são elegíveis para a atualização da plataforma para Windows Vista ou a atualização de plataforma para Windows Server 2008.

### <a name="windows-portable-devices-platform"></a>Windows Plataforma de dispositivos portáteis

a atualização da plataforma para o Windows Vista dá suporte às extensões do Windows 7 para a plataforma Windows dispositivos portáteis (WPD). Esse recurso permite que os computadores se comuniquem com dispositivos de mídia e armazenamento anexados. O WPD fornece uma maneira flexível e robusta para que os computadores se comuniquem com câmeras digitais, players de música, celulares e muitos outros tipos de dispositivos conectados.

para obter mais informações sobre Windows dispositivos portáteis, consulte [Windows dispositivos portáteis](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Edições qualificadas para as atualizações

a atualização de plataforma para Windows Vista e a atualização de plataforma para Windows Server 2008 habilitam Windows suporte a dispositivos portáteis (WPD) nas edições do Windows mostrado na tabela a seguir.



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
Premium inicial com SP2 (x86 e amd64)<br />
Negócios com SP2 (x86 e AMD64)<br />
Enterprise com SP2 (x86 e amd64)<br />
Ultimate com SP2 (x86 e AMD64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a>Elementos de API WPD com suporte

a tabela a seguir identifica os recursos com suporte para o Windows 7, Windows vista e Windows vista com atualização de plataforma para versões Windows Vista do sistema operacional Windows.

| Recurso WPD                    | Windows 7 | Windows Vista | Windows vista com atualização de plataforma para o Windows Vista |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| MTP sobre USB                   | Sim       | Sim           | Sim                                                  |
| MTP sobre IP                    | Sim       | Sim           | Sim                                                  |
| MTP Bluetooth             | Sim       | Não            | Sim                                                  |
| Serviços de dispositivos WPD e MTP    | Sim       | Não            | Sim                                                  |
| Automação WPD                 | Sim       | Não            | Não                                                   |
| Multifuncional/multi-transporte | Sim       | Não            | Não                                                   |
| Device Stage                   | Sim       | Não            | Não                                                   |
| Plataforma de sincronização de dispositivo           | Sim       | Não            | Não                                                   |



 

para edições do Windows 7 e Windows Vista que não têm o Microsoft Windows Media Player instalado por padrão (as edições N e KN), você deve instalar o [SDK do Windows Media Format 11]( ../audio-and-video.md) ( https://msdn.microsoft.com/windows/bb190326.aspx) para habilitar a funcionalidade WPD. para obter mais informações, consulte o [artigo da Base de dados de conhecimento](https://support.microsoft.com/kb/953693) ( https://go.microsoft.com/fwlink/p/?linkid=158715) , que foi publicado originalmente como uma resolução para o Windows Vista.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[atualização da plataforma para o Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Visões gerais**
</dt> <dt>

[sobre a atualização de plataforma para o Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[artigo da Base de dados de conhecimento sobre a atualização da plataforma para Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 
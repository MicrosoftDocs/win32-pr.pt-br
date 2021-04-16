---
title: Visão geral de automação da interface do usuário
description: A automação da interface do usuário da Microsoft é uma estrutura de acessibilidade para o Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Automação da interface do usuário, sobre
- Automação da interface do usuário, acessibilidade
- Automação da interface do usuário, componentes
- Automação da interface do usuário, API do provedor
- Automação da interface do usuário, API do cliente
- Automação da interface do usuário, arquivos de cabeçalho
- Automação da interface do usuário, modelo
- components
- acessibilidade
- API do provedor
- API do cliente
- arquivos de cabeçalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ea29b0abd4c6ed791ae3195f36a0f8184c8596
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365508"
---
# <a name="ui-automation-overview"></a>Visão geral de automação da interface do usuário

A automação da interface do usuário da Microsoft é uma estrutura de acessibilidade para o Windows. Ele fornece acesso programático à maioria dos elementos da interface do usuário na área de trabalho. Ele permite que produtos de tecnologia assistencial, como leitores de tela, forneçam informações sobre a interface do usuário aos usuários finais e manipulem a interface do usuário por meio de entrada padrão. A automação da interface do usuário também permite que scripts de teste automatizados interajam com a interface do usuário

A automação da interface do usuário foi disponibilizada pela primeira vez no Windows XP como parte da estrutura de Microsoft .NET. Embora uma API C++ não gerenciada também tenha sido publicada nesse momento, a utilidade das funções de cliente era limitada devido a problemas de interoperabilidade. Para o Windows 7, a API foi reescrita na Component Object Model (COM).

> [!Note]  
> Embora as funções de biblioteca introduzidas na versão anterior da automação da interface do usuário ainda estejam documentadas, elas não devem ser usadas em novos aplicativos.

 

Os aplicativos cliente de automação da interface do usuário podem ser escritos com a garantia de que funcionarão em várias estruturas de controle do Microsoft Windows. O núcleo de automação da interface do usuário mascara quaisquer diferenças nas estruturas que se basear em várias partes da interface do usuário. Por exemplo, a propriedade **Content** de um botão Windows Presentation Foundation (WPF), a propriedade **Caption** de um botão do Microsoft Win32 e a propriedade **ALT** de uma imagem HTML são todas mapeadas para uma única propriedade, **Name**, no modo de exibição de automação da interface do usuário.

A automação da interface do usuário fornece funcionalidade completa no Windows XP, no Windows Server 2003 e em sistemas operacionais posteriores.

Provedores de automação de interface do usuário são componentes que implementam o suporte à automação da interface do usuário em controles e oferecem suporte a aplicativos cliente do Microsoft Acessibilidade Ativa, por meio de um serviço de ponte interno.

> [!Note]  
> A automação da interface do usuário não permite a comunicação entre os processos iniciados por usuários diferentes por meio do comando **Executar como** .

 

Este tópico inclui as seções a seguir.

-   [Componentes de automação da interface do usuário](#ui-automation-components)
-   [Arquivos de cabeçalho da automação da interface do usuário](#ui-automation-header-files)
-   [Modelo de automação da interface do usuário](#ui-automation-model)
-   [Tópicos relacionados](#related-topics)

## <a name="ui-automation-components"></a>Componentes de automação da interface do usuário

A automação da interface do usuário tem quatro componentes principais, conforme mostrado na tabela a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>API do provedor</td>
<td>Um conjunto de interfaces COM que são implementadas por provedores de automação de interface do usuário. Provedores de automação de interface do usuário são objetos que fornecem informações sobre elementos de interface do usuário e respondem à entrada programática.</td>
</tr>
<tr class="even">
<td>API do cliente</td>
<td>Um conjunto de interfaces COM que permite que os aplicativos cliente obtenham informações sobre a interface do usuário e enviem entradas para controles.
<blockquote>
[!Note]<br />
As funções descritas em <a href="uiauto-entry-cpfunctions.md">funções de padrão de controle</a> preteridas e funções de <a href="uiauto-entry-uianodefunctions.md">nó preteridas</a> são preteridas. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário descritas em <a href="uiauto-entry-uiautoclientinterfaces.md">interfaces de elementos de automação da interface do usuário para clientes</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>UIAutomationCore.dll</td>
<td>A biblioteca de tempo de execução, às vezes chamada de núcleo de automação da interface do usuário, que lida com a comunicação entre provedores e clientes.</td>
</tr>
<tr class="even">
<td>Oleacc.dll</td>
<td>A biblioteca de tempo de execução para o Microsoft Acessibilidade Ativa e os objetos de proxy. A biblioteca também fornece objetos proxy usados pelo Microsoft Microsoft Acessibilidade Ativa para o proxy de automação da interface do usuário para dar suporte a controles Win32.</td>
</tr>
</tbody>
</table>



 

Há duas maneiras de usar a automação da interface do usuário: para criar suporte para controles personalizados usando a API do provedor e para criar aplicativos cliente que usam o núcleo de automação da interface do usuário para se comunicar com o e recuperar informações sobre os elementos da interface do usuário. Dependendo do seu foco, você deve consultar diferentes partes da documentação. Se você precisar criar suporte para controles personalizados, consulte [Guia do programador do provedor de automação de IU](uiauto-providerportal.md). Se você precisar se comunicar com ou recuperar informações sobre elementos da interface do usuário, consulte [Guia do programador do cliente de automação da interface do usuário](uiauto-clientportal.md).

## <a name="ui-automation-header-files"></a>Arquivos de cabeçalho da automação da interface do usuário

A API de automação da interface do usuário é definida em vários arquivos de cabeçalho do C/C++ diferentes que estão incluídos no SDK (Software Development Kit) do Windows. Os arquivos de cabeçalho da automação da interface do usuário são descritos na tabela a seguir:



| Arquivo de cabeçalho           | Descrição                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UIAutomationClient. h  | Define as interfaces e os elementos de programação relacionados usados por clientes de automação da interface do usuário.                                                                                                                                                                                           |
| UIAutomationCore. h    | Define as interfaces e os elementos de programação relacionados usados pelos provedores de automação da interface do usuário.                                                                                                                                                                                         |
| UIAutomationCoreApi. h | Define constantes, GUIDs, tipos de dados e estruturas gerais usadas por clientes e provedores de automação da interface do usuário. Ele também contém definições para as funções de padrão de nó e controle preteridas.                                                                                    |
| Automação da IU. h        | Inclui todos os outros arquivos de cabeçalho de automação da interface do usuário. Como a maioria dos aplicativos de automação de interface do usuário requer elementos de todos os arquivos de cabeçalho de automação da interface do usuário, é melhor incluir automação da IU. h em seus projetos de aplicativo de automação da interface do usuário em vez de incluir cada arquivo individualmente |



 

Se você estiver desenvolvendo um aplicativo que usa a API de automação da interface do usuário, deverá incluir automação da IU. h em seu projeto. Se seu aplicativo der suporte ao Microsoft Acessibilidade Ativa, inclua o arquivo de cabeçalho OleAcc. h. Os aplicativos de automação da interface do usuário que usam GUIDs também exigem o arquivo de cabeçalho Initguid. h. Se necessário, Initguid. h deve ser incluído antes de automação da IU. h.

## <a name="ui-automation-model"></a>Modelo de automação da interface do usuário

A automação da interface do usuário expõe todos os elementos da interface do usuário para aplicativos cliente como um objeto representado pela interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . Os elementos estão contidos em uma estrutura de árvore, com a área de trabalho como o elemento raiz. Os clientes podem filtrar a exibição bruta da árvore como uma exibição de controle ou de conteúdo. Essas exibições padrão da estrutura podem ser facilmente vistas usando o aplicativo de [inspeção](inspect-objects.md) incluído no SDK do Windows. Os aplicativos também podem criar exibições personalizadas.

Um elemento de automação de interface do usuário expõe propriedades do elemento de controle ou de interface do usuário que ele representa. Uma dessas propriedades é o tipo de controle, que define a aparência básica e a funcionalidade do elemento de controle ou de interface do usuário como uma única entidade reconhecível, por exemplo, um botão ou caixa de seleção. Para obter mais informações sobre tipos de controle, consulte [visão geral de tipos de controle de automação da interface do usuário](uiauto-controltypesoverview.md).

Além disso, um elemento de automação da interface do usuário expõe um ou mais padrões de controle. Um padrão de controle fornece um conjunto de propriedades que são específicas a um determinado tipo de controle. Um padrão de controle também expõe métodos que permitem que aplicativos cliente obtenham mais informações sobre o elemento e forneçam entrada para o elemento. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).

> [!Note]  
> Não há nenhuma correspondência de um para um entre tipos de controle e padrões de controle. Um padrão de controle pode ser suportado por vários tipos de controle, e um controle pode dar suporte a vários padrões de controle, cada um dos quais expõe diferentes aspectos de seu comportamento. Por exemplo, uma caixa de combinação tem pelo menos dois padrões de controle: um que representa sua capacidade de expandir e recolher e outro que representa o mecanismo de seleção. No entanto, um controle pode exibir apenas um único tipo de controle.

 

A automação da interface do usuário fornece informações para aplicativos cliente por meio de eventos. Ao contrário de WinEvents, os eventos de automação da interface do usuário não são baseados em um mecanismo de difusão. Os clientes de automação da interface do usuário se registram para notificações de eventos específicas e podem solicitar que propriedades específicas e informações de padrão de controle sejam passadas para seus manipuladores de eventos. Além disso, um evento de automação da interface do usuário contém uma referência ao elemento que o gerou. Os provedores podem melhorar o desempenho gerando eventos de forma seletiva, dependendo se algum cliente está ouvindo. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> </dl>

 

 






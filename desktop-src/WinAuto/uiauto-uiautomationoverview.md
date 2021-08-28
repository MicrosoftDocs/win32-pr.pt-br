---
title: Visão geral de automação da interface do usuário
description: O Microsoft Automação da Interface do Usuário é uma estrutura de acessibilidade para Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Automação da Interface do Usuário, sobre
- Automação da Interface do Usuário, acessibilidade
- Automação da Interface do Usuário,componentes
- Automação da Interface do Usuário, API do provedor
- Automação da Interface do Usuário, API do cliente
- Automação da Interface do Usuário, arquivos de header
- Automação da Interface do Usuário,modelo
- components
- acessibilidade
- API do provedor
- API do cliente
- arquivos de cabeçalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3664866280d570f9fa5f07acc6245ca2b4c1bff7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470053"
---
# <a name="ui-automation-overview"></a>Visão geral de automação da interface do usuário

O Microsoft Automação da Interface do Usuário é uma estrutura de acessibilidade para Windows. Ele fornece acesso programático à maioria dos elementos da interface do usuário na área de trabalho. Ele permite que os produtos de tecnologia adaptativa, como leitores de tela, forneçam informações sobre a interface do usuário para os usuários finais e manipulem a interface do usuário por meios diferentes da entrada padrão. Automação da Interface do Usuário também permite que scripts de teste automatizados interajam com a interface do usuário.

Automação da Interface do Usuário estava disponível pela primeira vez no Windows XP como parte do Microsoft .NET Framework. Embora uma API do C++ não gerenciamento também tenha sido publicada na época, a utilidade das funções de cliente era limitada devido a problemas de interoperabilidade. Por Windows 7, a API foi reescrita no COM (Component Object Model).

> [!Note]  
> Embora as funções de biblioteca introduzidas na versão anterior do Automação da Interface do Usuário ainda sejam documentadas, elas não devem ser usadas em novos aplicativos.

 

Automação da Interface do Usuário aplicativos cliente podem ser escritos com a garantia de que funcionarão em várias estruturas de controle Windows Microsoft. O Automação da Interface do Usuário principal mascara as diferenças nas estruturas que se baseam em várias partes da interface do usuário. Por exemplo, a propriedade **Content** de um botão Windows Presentation Foundation (WPF), a propriedade **Caption** de um botão Do Microsoft Win32 e a **propriedade ALT** de uma imagem HTML são mapeadas para uma única propriedade, **Name**, na exibição Automação da Interface do Usuário.

Automação da Interface do Usuário fornece funcionalidade completa no Windows XP, Windows Server 2003 e sistemas operacionais posteriores.

Automação da Interface do Usuário provedores são componentes que implementam Automação da Interface do Usuário suporte em controles e oferecem suporte para aplicativos cliente Microsoft Active Accessibility, por meio de um serviço de ponte integrado.

> [!Note]  
> Automação da Interface do Usuário permite a comunicação entre processos iniciados por usuários diferentes por meio do **comando Executar como.**

 

Este tópico inclui as seções a seguir.

-   [Automação da Interface do Usuário componentes](#ui-automation-components)
-   [Automação da Interface do Usuário de Automação da Interface do Usuário de texto](#ui-automation-header-files)
-   [Automação da Interface do Usuário modelo](#ui-automation-model)
-   [Tópicos relacionados](#related-topics)

## <a name="ui-automation-components"></a>Automação da Interface do Usuário componentes

Automação da Interface do Usuário tem quatro componentes principais, conforme mostrado na tabela a seguir.




| Componente | Descrição | 
|-----------|-------------|
| API do provedor | Um conjunto de interfaces COM que são implementadas por Automação da Interface do Usuário provedores. Automação da Interface do Usuário provedores são objetos que fornecem informações sobre elementos da interface do usuário e respondem à entrada programática. | 
| API do cliente | Um conjunto de interfaces COM que permitem que aplicativos cliente obtenham informações sobre a interface do usuário e enviem entrada para controles.<blockquote>[!Note]<br />As funções descritas <a href="uiauto-entry-cpfunctions.md">em Funções padrão</a> de controle preterido e funções <a href="uiauto-entry-uianodefunctions.md">de</a> nó preterido são preterida. Em vez disso, os aplicativos cliente devem usar Automação da Interface do Usuário interfaces COM descritas <a href="uiauto-entry-uiautoclientinterfaces.md">em interfaces de</a>elemento Automação da Interface do Usuário para clientes .</blockquote><br /> | 
| UIAutomationCore.dll | A biblioteca em tempo de executar, às vezes chamada Automação da Interface do Usuário núcleo, que lida com a comunicação entre provedores e clientes. | 
| Oleacc.dll | A biblioteca em tempo de Microsoft Active Accessibility e os objetos proxy. A biblioteca também fornece objetos de proxy usados pelo Microsoft Microsoft Active Accessibility para Automação da Interface do Usuário Proxy para dar suporte a controles Win32. | 




 

Há duas maneiras de usar o Automação da Interface do Usuário: criar suporte para controles personalizados usando a API do provedor e criar aplicativos cliente que usam o núcleo Automação da Interface do Usuário para se comunicar e recuperar informações sobre os elementos da interface do usuário. Dependendo do seu foco, você deve consultar diferentes partes da documentação. Se você precisar criar suporte para controles personalizados, consulte Automação da Interface do Usuário Guia do [Programador do Provedor](uiauto-providerportal.md). Se você precisar se comunicar com ou recuperar informações sobre elementos da interface do usuário, [consulte Guia do](uiauto-clientportal.md)programador do Automação da Interface do Usuário cliente .

## <a name="ui-automation-header-files"></a>arquivos Automação da Interface do Usuário de Automação da Interface do Usuário

A API Automação da Interface do Usuário é definida em vários arquivos de header C/C++ diferentes incluídos no SDK (Software Development Kit) do Windows. Os Automação da Interface do Usuário de Automação da Interface do Usuário são descritos na tabela a seguir:



| Arquivo de cabeçalho           | Descrição                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UIAutomationClient.h  | Define as interfaces e os elementos de programação relacionados usados por Automação da Interface do Usuário clientes.                                                                                                                                                                                           |
| UIAutomationCore.h    | Define as interfaces e os elementos de programação relacionados usados por Automação da Interface do Usuário provedores.                                                                                                                                                                                         |
| UIAutomationCoreApi.h | Define constantes gerais, GUIDs, tipos de dados e estruturas usadas por Automação da Interface do Usuário clientes e provedores. Ele também contém definições para as funções de padrão de controle e nó preterido.                                                                                    |
| UIAutomation.h        | Inclui todos os outros arquivos de Automação da Interface do Usuário de texto. Como Automação da Interface do Usuário aplicativos do Automação da Interface do Usuário exigem elementos de todos os arquivos de Automação da Interface do Usuário, é melhor incluir UIAutomation.h em seus projetos de aplicativo Automação da Interface do Usuário em vez de incluir cada arquivo individualmente. |



 

Se você estiver desenvolvendo um aplicativo que usa a API Automação da Interface do Usuário, inclua UIAutomation.h em seu projeto. Se o aplicativo for compatível Microsoft Active Accessibility, inclua o arquivo de título Oleacc.h. Automação da Interface do Usuário aplicativos que usam GUIDs também exigem o arquivo de título Initguid.h. Se necessário, Initguid.h deve ser incluído antes de UIAutomation.h.

## <a name="ui-automation-model"></a>Automação da Interface do Usuário modelo

Automação da Interface do Usuário expõe todos os elementos da interface do usuário para aplicativos cliente como um objeto representado pela interface [**IUIAutomationElement.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) Os elementos estão contidos em uma estrutura de árvore, com a área de trabalho como o elemento raiz. Os clientes podem filtrar a exibição bruta da árvore como uma exibição de controle ou uma exibição de conteúdo. Essas exibições padrão da estrutura podem ser vistas facilmente usando o aplicativo [Inspecionar](inspect-objects.md) que está incluído no SDK Windows aplicativo. Os aplicativos também podem criar exibições personalizadas.

Um Automação da Interface do Usuário expõe propriedades do controle ou do elemento de interface do usuário que ele representa. Uma dessas propriedades é o tipo de controle, que define a aparência básica e a funcionalidade do elemento de controle ou interface do usuário como uma única entidade reconhecível, por exemplo, um botão ou caixa de seleção. Para obter mais informações sobre tipos de controle, [consulte Visão geral Automação da Interface do Usuário tipos de controle](uiauto-controltypesoverview.md).

Além disso, um Automação da Interface do Usuário expõe um ou mais padrões de controle. Um padrão de controle fornece um conjunto de propriedades que são específicas para um tipo de controle específico. Um padrão de controle também expõe métodos que permitem que aplicativos cliente recebam mais informações sobre o elemento e forneçam entrada para o elemento. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).

> [!Note]  
> Não há correspondência um-para-um entre tipos de controle e padrões de controle. Um padrão de controle pode ser suportado por vários tipos de controle e um controle pode dar suporte a vários padrões de controle, cada um deles expõe diferentes aspectos de seu comportamento. Por exemplo, uma caixa de combinação tem pelo menos dois padrões de controle: um que representa sua capacidade de expansão e ressalção e outro que representa o mecanismo de seleção. No entanto, um controle pode exibir apenas um único tipo de controle.

 

Automação da Interface do Usuário fornece informações para aplicativos cliente por meio de eventos. Ao contrário do WinEvents, Automação da Interface do Usuário eventos não são baseados em um mecanismo de difusão. Automação da Interface do Usuário clientes se registram para notificações de eventos específicas e podem solicitar que propriedades específicas e informações de padrão de controle sejam passadas para seus manipuladores de eventos. Além disso, um Automação da Interface do Usuário contém uma referência ao elemento que o gerou. Os provedores podem melhorar o desempenho aprimorando eventos seletivamente, dependendo se algum cliente está escutando. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> </dl>

 

 






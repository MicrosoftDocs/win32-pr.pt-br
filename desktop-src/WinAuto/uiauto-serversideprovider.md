---
title: Implementar um provedor Server-Side Automação da Interface do Usuário dados
description: Este tópico descreve como implementar um provedor microsoft Automação da Interface do Usuário do lado do servidor para um controle personalizado escrito em C++.
ms.assetid: c3a919b2-8b8c-4dde-ad71-587f3845a9f5
keywords:
- Automação da Interface do Usuário, implementação do provedor do lado do servidor
- Automação da Interface do Usuário, implementação do provedor
- Automação da Interface do Usuário, implementando provedores do lado do servidor
- Automação da Interface do Usuário, implementando provedores
- provedores do lado do servidor, implementando
- provedores do lado do servidor, interfaces
- provedores do lado do servidor, valores de propriedade
- provedores do lado do servidor, eventos
- provedores do lado do servidor, atribuindo um novo pai
- eventos, provedores do lado do servidor
- interfaces, provedores do lado do servidor
- provedores, implementando
- implementando provedores do lado do servidor
- Implementando provedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 583b9a5f91bb8be53a3e8b0e356ce558978b8ea28d5b726b56f52420cd7bff37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413436"
---
# <a name="implement-a-server-side-ui-automation-provider"></a>Implementar um provedor Server-Side Automação da Interface do Usuário dados

Este tópico descreve como implementar um provedor microsoft Automação da Interface do Usuário do lado do servidor para um controle personalizado escrito em C++. Ele contém as seções a seguir:

-   [Interfaces do provedor](#provider-interfaces)
-   [Funcionalidade necessária para provedores Automação da Interface do Usuário serviços](#required-functionality-for-ui-automation-providers)
-   [Valores da propriedade](#property-values)
-   [Eventos de provedores](#events-from-providers)
-   [Navegação do provedor](#provider-navigation)
-   [Atribuindo um novo pai](#assigning-a-new-parent)
-   [Reposicionamento de provedor](#provider-repositioning)
-   [Desconectando provedores](#disconnecting-providers)
-   [Tópicos relacionados](#related-topics)

Para exemplos de código que mostram como implementar provedores do lado do servidor, consulte Tópicos de ida e Automação da Interface do Usuário [provedores](uiauto-howto-topics-for-uiautomation-providers.md).

## <a name="provider-interfaces"></a>Interfaces do provedor

As interfaces COM (Component Object Model) a seguir fornecem funcionalidade para controles personalizados. Para fornecer funcionalidade básica, cada Automação da Interface do Usuário provedor deve implementar pelo menos a interface [**IRawElementProviderSimple.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) As interfaces [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) e [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) são opcionais, mas devem ser implementadas para elementos em um controle complexo para fornecer funcionalidade adicional.



| Interface                                                                         | Descrição                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Irawelementprovidersimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)             | Fornece funcionalidade básica para um controle hospedado em uma janela, incluindo suporte para padrões de controle e propriedades.                                                         |
| [**Irawelementproviderfragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)         | Adiciona funcionalidade para um elemento em um controle complexo, incluindo a navegação no fragmento, a definição do foco e o retorno do retângulo delimitativo do elemento.             |
| [**Irawelementproviderfragmentroot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) | Adiciona funcionalidade para o elemento raiz em um controle complexo, incluindo localizar um elemento filho em coordenadas especificadas e definir o estado de foco para todo o controle. |



 

> [!Note]  
> Na API Automação da Interface do Usuário para código gerenciado, essas interfaces formam uma hierarquia de herança. Esse não é o caso no C++, em que as interfaces são completamente separadas.

 

As interfaces a seguir fornecem funcionalidade adicionada, mas a implementação é opcional.



| Interface                                                                         | Descrição                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | Permite que o provedor acompanhe solicitações de eventos.                                      |
| [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) | Habilita o reposicionamento de elementos baseados em janela Automação da Interface do Usuário árvore de um fragmento. |



 

## <a name="required-functionality-for-ui-automation-providers"></a>Funcionalidade necessária para provedores Automação da Interface do Usuário serviços

Para se comunicar com Automação da Interface do Usuário, seu controle deve implementar as principais áreas de funcionalidade descritas na tabela a seguir.



| Funcionalidade                                              | Implementação                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Expor o provedor ao Automação da Interface do Usuário.                      | Em resposta a [**uma mensagem \_ WM GETOBJECT**](wm-getobject.md) enviada para a janela de controle, retorne o objeto que implementa [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple). Para fragmentos, esse deve ser o provedor para a raiz do fragmento.                                           |
| Forneça valores de propriedade.                                   | Implemente [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) para fornecer ou substituir valores.                                                                                                                                                             |
| Permitir que o cliente interaja com o controle .            | Implemente interfaces que deem suporte a cada padrão de controle apropriado, [**como IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider). Retorne esses provedores de padrão de controle em sua implementação [**de IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider). |
| Aumente eventos.                                              | [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent), métodos de [**IProxyProviderWinEventSink**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iproxyproviderwineventsink).                                                                                                                                                |
| Habilita a navegação e o foco em um fragmento.              | Implemente [**IRawElementProviderFragment para**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) cada elemento dentro do fragmento. Não é necessário para elementos que não fazem parte de um fragmento.                                                                                                                         |
| Habilita o foco e a localização de elementos filho em um fragmento. | Implemente [**IRawElementProviderFragmentRoot.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) Não é necessário para elementos que não são raízes de fragmento.                                                                                                                                                          |



 

## <a name="property-values"></a>Valores da propriedade

Automação da Interface do Usuário provedores para controles personalizados devem dar suporte a determinadas propriedades que podem ser usadas por Automação da Interface do Usuário e por aplicativos cliente. Para elementos hospedados no Windows, Automação da Interface do Usuário pode recuperar algumas propriedades do provedor de janela padrão, mas deve obter outras do provedor personalizado.

Normalmente, os provedores para controles baseados em janela não precisam fornecer as seguintes propriedades identificadas por **PROPERTYID**:

-   [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ProcessIdPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ClassNamePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ HasKeyboardFocusPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsEnabledPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ RuntimeIdPropertyId**](uiauto-automation-element-propids.md)

A propriedade RuntimeId de um elemento simples ou raiz de fragmento hospedada em uma janela é obtida da janela. No entanto, os elementos de fragmento abaixo da raiz, como itens de lista em uma caixa de listagem, devem fornecer seus próprios identificadores. Para obter mais informações, [**consulte IRawElementProviderFragment::GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid).

A propriedade IsKeyboardFocusable deve ser retornada para provedores hospedados em um controle Windows Forms. Nesse caso, o provedor de janela padrão pode não conseguir recuperar o valor correto.

A propriedade Name geralmente é fornecida pelo provedor de host.

## <a name="events-from-providers"></a>Eventos de provedores

Automação da Interface do Usuário provedores devem auar eventos para notificar os aplicativos cliente de alterações no estado da interface do usuário. As funções a seguir são usadas para auar eventos.



| Função                                                                                   | Descrição                                                                                                              |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)                  | Gera vários eventos, incluindo eventos disparados por padrões de controle.                                                   |
| [**UiaRaiseAutomationPropertyChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent) | Gera um evento quando uma propriedade Automação da Interface do Usuário é alterada.                                                               |
| [**UiaRaiseStructureChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)      | Gera um evento quando a estrutura da árvore de automação da interface do usuário é alterada, por exemplo, removendo ou adicionando um elemento. |



 

A finalidade de um evento é notificar o cliente sobre algo que está ocorrendo na interface do usuário. Os provedores devem gerar um evento independentemente se a alteração foi disparada pela entrada do usuário ou por um aplicativo cliente usando a automação da interface do usuário. Por exemplo, o evento identificado por [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md) deve ser gerado sempre que o controle é invocado, seja por meio de entrada direta do usuário ou pelo aplicativo cliente chamando [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke).

Para otimizar o desempenho, um provedor poderá acionar eventos seletivamente ou não gerar nenhum evento se nenhum aplicativo cliente estiver registrado para recebê-los. Os seguintes elementos de API são usados para otimização.



| Elemento API                                                                       | Descrição                                                                                                                                                       |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)           | Essa função determina se algum aplicativo cliente assinou eventos de automação da interface do usuário.                                                                 |
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | A implementação dessa interface em uma raiz de fragmento permite que o provedor seja avisado quando os clientes registram e cancelam o registro de manipuladores de eventos para eventos no fragmento. |



 

> [!Note]  
> Semelhante à implementação da contagem de referência na programação COM, é importante que os provedores de automação da interface do usuário tratem os métodos [**IRawElementProviderAdviseEvents:: AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) e [**AdviseEventRemoved**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventremoved) como os métodos [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . Desde que **AdviseEventAdded** tenha sido chamado mais vezes do que **AdviseEventRemoved** para um evento ou propriedade específica, o provedor deve continuar a gerar eventos correspondentes, pois alguns clientes ainda estão ouvindo. Como alternativa, os provedores de automação da interface do usuário podem usar a função [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening) para determinar se pelo menos um cliente está ouvindo e, em caso afirmativo, gera todos os eventos apropriados.

 

## <a name="provider-navigation"></a>Navegação do provedor

Provedores para controles simples, como um botão personalizado hospedado em uma janela, não precisam dar suporte à navegação na árvore de automação da interface do usuário. A navegação de e para o elemento é manipulada pelo provedor padrão para a janela do host, que é especificada na implementação de [**IRawElementProviderSimple:: HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider). No entanto, quando você implementa um provedor para um controle personalizado complexo, deve dar suporte à navegação entre o nó raiz do fragmento e seus descendentes e entre nós irmãos.

> [!Note]  
> Elementos de um fragmento diferente da raiz devem retornar **NULL** de [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider), porque eles não são hospedados diretamente em uma janela, e nenhum provedor padrão pode dar suporte à navegação de e para eles.

 

A estrutura do fragmento é determinada pela implementação de [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate). Para cada direção possível de cada fragmento, esse método retorna o objeto do provedor para o elemento nessa direção. Se não houver nenhum elemento nessa direção, o método retornará **NULL**.

A raiz do fragmento dá suporte à navegação somente para elementos filho. Por exemplo, uma caixa de listagem retorna o primeiro item da lista quando a direção é **NavigateDirection \_ FirstChild** e retorna o último item quando a direção é **NavigateDirection \_ LastChild**. A raiz do fragmento não dá suporte à navegação para um pai ou para irmãos; Isso é tratado pelo provedor de janela do host.

Elementos de um fragmento que não são a raiz devem dar suporte à navegação para o pai e a quaisquer irmãos e filhos que eles têm.

## <a name="assigning-a-new-parent"></a>Atribuindo um novo pai

As janelas pop-up são, na verdade, janelas de nível superior e, por padrão, aparecem na árvore de automação da interface do usuário como filhos da área de trabalho. Em muitos casos, no entanto, janelas pop-up são logicamente filhos de algum outro controle. Por exemplo, a lista suspensa de uma caixa de combinação é logicamente um filho da caixa de combinação. Da mesma forma, uma janela pop-up de menu é logicamente um filho do menu. A automação da interface do usuário fornece suporte para atribuir um novo pai a uma janela pop-up para que pareça ser um filho do controle associado.

Para atribuir um novo pai a uma janela pop-up:

1.  Crie um provedor para a janela pop-up. Isso requer que a classe da janela pop-up seja conhecida com antecedência.
2.  Implemente todas as propriedades e padrões de controle como de costume para esse pop-up, como se fosse um controle por si só.
3.  Implemente a propriedade [**IRawElementProviderSimple:: HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider) para que ela retorne o valor obtido de [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd), em que o parâmetro é o identificador da janela pop-up.
4.  Implemente [**IRawElementProviderFragment:: Navegue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) para a janela pop-up e seu pai para que a navegação seja manipulada corretamente do pai lógico para os filhos lógicos e entre filhos irmãos.

Quando a automação da interface do usuário encontra a janela pop-up, ela reconhece que a navegação está sendo substituída do padrão e ignora a janela pop-up quando ela é encontrada como um filho da área de trabalho. Em vez disso, o nó só pode ser acessado por meio do fragmento.

A atribuição de um novo pai não é adequada para casos em que um controle pode hospedar uma janela de qualquer classe. Por exemplo, um controle rebar pode hospedar qualquer tipo de janela em suas bandas. Para lidar com esses casos, a automação da interface do usuário dá suporte a uma forma alternativa de realocação de janela, conforme descrito na próxima seção.

## <a name="provider-repositioning"></a>Reposicionamento do provedor

Fragmentos de automação da interface do usuário podem conter dois ou mais elementos que estão contidos em uma janela. Como cada janela tem seu próprio provedor padrão que considera que a janela é um filho de uma janela recipiente, a árvore de automação da interface do usuário, por padrão, mostrará as janelas no fragmento como filhos da janela pai. Na maioria dos casos, esse comportamento é desejável, mas às vezes pode levar à confusão porque não corresponde à estrutura lógica da interface do usuário.

Um bom exemplo disso é um controle rebar. Um controle rebar contém bandas, e cada uma delas pode, por sua vez, conter um controle baseado em janela, como uma barra de ferramentas, uma caixa de edição ou uma caixa de combinação. O provedor de janela padrão da janela rebar vê as janelas de controle de banda como filhas, e o provedor de rebar vê as faixas como filhas. Como o provedor de janela e o provedor de rebar estão trabalhando em tandem e combinando seus filhos, as faixas e os controles baseados em janela aparecem como filhos do controle rebar. No entanto, logicamente, somente as faixas devem aparecer como filhos do controle rebar, e cada provedor de banda deve ser acoplado ao provedor de janela padrão para o controle que ele contém.

Para fazer isso, o provedor raiz do fragmento do controle rebar expõe um conjunto de filhos representando as faixas. Cada banda tem um único provedor que pode expor propriedades e padrões de controle. Em sua implementação de [**IRawElementProviderSimple:: HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider), o provedor de banda retorna o provedor de janela padrão para a janela de controle, que é obtido chamando [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd), passando o identificador de janela do controle (**hWnd**). Por fim, o provedor raiz do fragmento para o rebar implementa a interface [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) e, em sua implementação de [**IRawElementProviderHwndOverride:: GetOverrideProviderForHwnd**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderhwndoverride-getoverrideproviderforhwnd), ele retorna o provedor de banda apropriado para o controle contido na janela especificada.

## <a name="disconnecting-providers"></a>Desconectando provedores

Normalmente, os aplicativos criam controles conforme eles são necessários e os destrói posteriormente. Depois de destruir um controle, os recursos do provedor de automação da interface do usuário associados ao controle devem ser liberados chamando o [**UiaDisconnectProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider).

Da mesma forma, um aplicativo deve usar a função [**UiaDisconnectAllProviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders) para liberar todos os recursos de automação da interface do usuário mantidos por todos os provedores no aplicativo antes de desligar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia do programador do provedor de automação de interface do usuário](uiauto-providerportal.md)
</dt> </dl>

 

 
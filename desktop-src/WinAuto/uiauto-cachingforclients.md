---
title: Caching Automação da Interface do Usuário propriedades e padrões de controle
description: Ao usar o Microsoft Automação da Interface do Usuário, os clientes geralmente precisam recuperar várias propriedades para vários elementos de automação.
ms.assetid: 948b3bb9-75a9-4197-9680-e6fe7bb86feb
keywords:
- cache, Automação da Interface do Usuário propriedades
- cache, propriedades
- cache, Automação da Interface do Usuário de controle
- cache, padrões de controle
- Automação da Interface do Usuário, propriedades de cache
- Automação da Interface do Usuário, cache de propriedade
- clientes, propriedades de Automação da Interface do Usuário cache
- clientes, cache e Automação da Interface do Usuário de controle
- Automação da Interface do Usuário, padrões de controle de cache
- Automação da Interface do Usuário,cache de padrão de controle
- padrões de controle, cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae14fb607dd66ab1a4ea99cd9836f2f74e5c863afef8465843d3ea174186ef29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324970"
---
# <a name="caching-ui-automation-properties-and-control-patterns"></a>Caching Automação da Interface do Usuário propriedades e padrões de controle

Ao usar o Microsoft Automação da Interface do Usuário, os clientes geralmente precisam recuperar várias propriedades para vários elementos de automação. Um cliente pode recuperar propriedades individuais um elemento por vez usando os métodos de recuperação de propriedade, como [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) ou [**CurrentAccessKey**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentaccesskey). No entanto, esse método é lento e ineficiente porque requer uma chamada entre processos para cada propriedade que está sendo recuperada. Para melhorar o desempenho, os clientes podem usar os recursos de cache (também chamados de busca em massa) de Automação da Interface do Usuário. Caching permite que um cliente recupere todas as propriedades desejadas para todos os elementos desejados com uma única chamada de método. Em seguida, o cliente pode recuperar as propriedades individuais do cache conforme necessário e pode obter um novo instantâneo do cache periodicamente, geralmente em resposta a eventos que significam alterações na interface do usuário.

O aplicativo pode solicitar cache quando recupera um elemento Automação da Interface do Usuário usando um método, como [**IUIAutomation::ElementFromPointBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache), [**IUIAutomationTreeWalker::GetFirstChildElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-getfirstchildelementbuildcache)ou [**IUIAutomationElement::FindFirstBuildCache.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache)

Caching também ocorre quando você especifica uma solicitação de cache ao assinar eventos. O Automação da Interface do Usuário elemento passado para o manipulador de eventos como a origem de um evento contém as propriedades armazenadas em cache e os padrões de controle especificados pela solicitação de cache. As alterações feitas na solicitação de cache depois de assinar o evento não terão efeito.

Este tópico inclui as seções a seguir.

-   [Solicitações de cache](#cache-requests)
    -   [Especificando padrões de propriedade e controle a armazenar em cache](#specifying-property-and-control-patterns-to-cache)
    -   [Especificando o scoping e filtragem de uma solicitação Caching consulta](#specifying-the-scoping-and-filtering-of-a-caching-request)
    -   [Força das referências de elemento](#strength-of-element-references)
-   [Recuperando filhos e pais armazenados em cache](#retrieving-cached-children-and-parents)
-   [Recuperando um novo instantâneo do cache](#retrieving-a-new-snapshot-of-the-cache)
-   [Exemplos](#examples)
-   [Tópicos relacionados](#related-topics)

## <a name="cache-requests"></a>Solicitações de cache

Caching envolve determinar quais propriedades recuperar e de quais elementos recuperá-las e, em seguida, usar essas informações para criar uma solicitação de cache. Sempre que o cliente obtém uma interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para o item de interface do usuário, o Automação da Interface do Usuário armazena em cache as informações especificadas na solicitação de cache.

Para criar uma solicitação de cache, comece usando o método [**IUIAutomation::CreateCacheRequest**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createcacherequest) para recuperar um ponteiro de interface [**IUIAutomationCacheRequest.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) Em seguida, configure a solicitação de cache usando os métodos de **IUIAutomationCacheRequest**.

### <a name="specifying-property-and-control-patterns-to-cache"></a>Especificando padrões de propriedade e controle a armazenar em cache

Você pode especificar propriedades para armazenar em cache chamando [**IUIAutomationCacheRequest::AddProperty.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addproperty) Você pode especificar padrões de controle para armazenar em cache chamando [**IUIAutomationCacheRequest::AddPattern.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-addpattern) Quando um padrão de controle é armazenado em cache, suas propriedades não são armazenadas em cache automaticamente; você deve especificar as propriedades que deseja armazenar em cache usando **AddProperty**.

Você pode recuperar uma propriedade de padrão de [](uiauto-implementingvalue.md) controle (por exemplo, a propriedade Value do padrão de controle Valor), sem precisar recuperar todo o padrão de controle no cache. Você deve recuperar o padrão de controle somente se precisar usar um método de padrão de controle.

### <a name="specifying-the-scoping-and-filtering-of-a-caching-request"></a>Especificando o scoping e filtragem de uma solicitação Caching consulta

Você pode especificar os elementos cujas propriedades e padrões de controle você deseja armazenar em cache definindo a propriedade [**IUIAutomationCacheRequest::TreeScope**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) antes de usar a solicitação. O escopo é relativo aos elementos recuperados pelo método para o qual a solicitação de cache é passada. Por exemplo, se você definir apenas [**TreeScope \_ Children**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)e recuperar um elemento Automação da Interface do Usuário, as propriedades e os padrões de controle dos filhos desse elemento serão armazenados em cache, mas as propriedades e os padrões de controle do próprio elemento não serão armazenados em cache. Para garantir que o cache seja feito para o próprio elemento recuperado, você deve incluir o Elemento **TreeScope \_** na propriedade **IUIAutomationCacheRequest::TreeScope.** Não é possível definir o escopo como **TreeScope \_ Parent ou** **TreeScope \_ Ancestors**. No entanto, um elemento pai pode ser armazenado em cache quando um elemento filho é armazenado em cache; consulte Recuperando filhos e pais armazenados em cache neste tópico.

A extensão do cache também é afetada pela [**propriedade IUIAutomationCacheRequest::TreeFilter.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treefilter) Por padrão, o cache é executado somente para elementos que aparecem na exibição de controle da árvore Automação da Interface do Usuário dados. No entanto, você pode alterar essa propriedade para aplicar o cache a todos os elementos ou somente aos elementos que aparecem na exibição de conteúdo.

### <a name="strength-of-element-references"></a>Força das referências de elemento

Ao recuperar um elemento de automação, por padrão, você tem acesso a todas as propriedades e padrões de controle desse elemento, incluindo as propriedades e padrões de controle que não foram armazenados em cache. No entanto, você pode especificar que a referência ao elemento refere-se apenas a dados armazenados em cache, definindo a propriedade [**IUIAutomationCacheRequest::AutomationElementMode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_automationelementmode) como **AutomationElementMode \_ None**. Nesse caso, você não tem acesso a nenhuma propriedade não acessada e padrões de controle de elementos recuperados. Isso significa que você não pode acessar nenhuma propriedade atual, como [**IUIAutomationElement::CurrentIsEnabled**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisenabled) ou recuperar um padrão de controle usando [**IUIAutomationElement::GetCurrentPattern.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) Em padrões de controle armazenados em cache, você não pode chamar métodos que executam ações no controle, como [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke).

Um exemplo de um aplicativo que pode não precisar de referências completas a objetos é um leitor de tela, que pode pré-buscar as propriedades de nome e tipo de controle dos elementos em uma janela sem precisar dos próprios objetos de elemento de automação.

## <a name="retrieving-cached-children-and-parents"></a>Recuperando filhos e pais armazenados em cache

Quando você recupera um elemento de automação e o cache de solicitação para filhos desse elemento por meio da propriedade [**IUIAutomationCacheRequest::TreeScope**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationcacherequest-get_treescope) da solicitação, é possível obter os elementos filho chamando [**IUIAutomationElement::GetCachedChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedchildren) no elemento recuperado.

Se [**o \_ Elemento TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) tiver sido incluído no escopo da solicitação de cache, o elemento raiz da solicitação poderá ser recuperado chamando [**IUIAutomationElement::GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent) em qualquer um dos elementos filho.

> [!Note]  
> Não é possível armazenar em cache pais ou ancestrais do elemento raiz da solicitação.

 

## <a name="retrieving-a-new-snapshot-of-the-cache"></a>Recuperando um novo instantâneo do cache

O cache é válido apenas desde que nada mude na interface do usuário. Seu aplicativo é responsável por recuperar um novo instantâneo do cache, normalmente, em resposta a eventos.

Se você assinar um evento com uma solicitação de cache, obterá um novo instantâneo [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) do cache como a origem do evento sempre que o manipulador de eventos for chamado. Você também pode recuperar um novo instantâneo de informações armazenadas em cache para um elemento chamando [**IUIAutomationElement::BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache). Você pode passar o [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest) original para obter um novo instantâneo de todas as informações que foram armazenadas em cache anteriormente.

A recuperação de um novo instantâneo do cache não modifica as propriedades de nenhuma referência [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) existente.

## <a name="examples"></a>Exemplos

Para exemplos de código que mostram como usar os recursos de cache do Automação da Interface do Usuário, consulte [How to Use Caching](uiauto-howto-use-caching.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Obtendo elementos da automação interface do usuário](uiauto-obtainingelements.md)
</dt> <dt>

[Visão geral das propriedades de automação da interface do usuário](uiauto-propertiesoverview.md)
</dt> </dl>

 

 





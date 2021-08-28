---
title: Funções de nó preteridas
description: Funções de nó preteridas
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d700c506ee0bb0baf41cdd2facb85b0e7153d57
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476162"
---
# <a name="deprecated-node-functions"></a>Funções de nó preteridas

> [!Note]  
> As funções de padrão de controle descritas nesta seção são preteridas. Os aplicativos cliente devem usar as interfaces de Component Object Model (COM) descritas nas seções a seguir:
>
> -   [Interfaces de elementos de automação da interface do usuário para clientes](uiauto-entry-uiautoclientinterfaces.md)
> -   [Interface de condição de propriedade para clientes](uiauto-client-propconditioninterfaces.md)
> -   [Interfaces de padrão de controle para clientes](uiauto-client-controlpatterninterfaces.md)
> -   [Interfaces de manipulação de eventos para clientes](uiauto-client-eventhandlinginterfaces.md)
> -   [Interfaces de fábrica de proxy para clientes](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>Nesta seção




| Função | Descrição | 
|----------|-------------|
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário da Microsoft.</blockquote><br /> Adiciona um ouvinte para eventos em um nó na árvore de automação da interface do usuário.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Adiciona uma janela ao ouvinte de eventos.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Uma função implementada pelo cliente que é chamada pela automação da interface do usuário quando é gerado um evento que o cliente assinou.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Remove uma janela do ouvinte de eventos.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Recupera um ou mais nós de automação da interface do usuário que correspondem aos critérios de pesquisa.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Obtém uma cadeia de caracteres de erro para que possa ser passada para o cliente. Esse método não é usado diretamente pelos clientes.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Recupera um <em>padrão de controle</em>.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Recupera o valor de uma propriedade de automação da interface do usuário.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Recupera o nó de automação da interface do usuário raiz.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Recupera o identificador de tempo de execução de um nó de automação de interface do usuário.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Atualiza o cache de valores de propriedade e padrões de controle.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Obtém um objeto de padrão de controle de um tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Obtém um intervalo de texto de um tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Obtém um HUIANODE de um tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Obtém o identificador de inteiro que pode ser usado em métodos que exigem uma PROPERTYid, o PATTERNid, o CONTROLTYPEid, o textattributeid ou EVENTID.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Navega na árvore de automação da interface do usuário, recuperando opcionalmente as informações armazenadas em cache.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Recupera o nó de automação da interface do usuário para o elemento de interface do usuário que atualmente tem o foco de entrada.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Recupera o nó de automação da interface do usuário associado a uma janela.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Recupera o nó de automação da interface do usuário para o elemento no ponto especificado.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Recupera o nó de automação da interface do usuário para um provedor de elementos brutos.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.</blockquote><br /> Exclui um nó da memória.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Os aplicativos cliente devem usar as interfaces AUTOMAÇÃO DA INTERFACE DO USUÁRIO COM.</blockquote><br /> Exclui um objeto padrão alocado da memória.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Os aplicativos cliente devem usar as interfaces AUTOMAÇÃO DA INTERFACE DO USUÁRIO COM.</blockquote><br /> Uma função definida pelo aplicativo que é chamada Automação da Interface do Usuário para obter um provedor do lado do cliente para um elemento.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Os aplicativos cliente devem usar as interfaces AUTOMAÇÃO DA INTERFACE DO USUÁRIO COM.</blockquote><br /> Obtém um valor booliana que especifica se um retângulo tem todas as suas coordenadas definidas como 0.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Os aplicativos cliente devem usar as interfaces AUTOMAÇÃO DA INTERFACE DO USUÁRIO COM.</blockquote><br /> Define os elementos de uma <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>estrutura UiaRect</strong></a> como 0.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Os aplicativos cliente devem usar as interfaces AUTOMAÇÃO DA INTERFACE DO USUÁRIO COM.</blockquote><br /> Registra o método definido pelo aplicativo que é chamado pelo Automação da Interface do Usuário para obter um provedor para um elemento.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Os aplicativos cliente devem usar as interfaces AUTOMAÇÃO DA INTERFACE DO USUÁRIO COM.</blockquote><br /> Remove um ouvinte para eventos em um nó na árvore Automação da Interface do Usuário dados.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Os aplicativos cliente devem usar as interfaces AUTOMAÇÃO DA INTERFACE DO USUÁRIO COM.</blockquote><br /> Define o foco de entrada para o elemento especificado na interface do usuário.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a><br /> | <blockquote>[!Note]<br />Esta função é preterida. Os aplicativos cliente devem usar as interfaces AUTOMAÇÃO DA INTERFACE DO USUÁRIO COM.</blockquote><br /> Exclui um objeto de intervalo de texto alocado da memória.<br /> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Automação da Interface do Usuário clientes](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 


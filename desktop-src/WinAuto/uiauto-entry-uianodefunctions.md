---
title: Funções de nó preteridas
description: Funções de nó preteridas
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7273ffd6c704c9db6408165d1eba3a293f3d1cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103917749"
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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário da Microsoft.
</blockquote>
<br/> Adiciona um ouvinte para eventos em um nó na árvore de automação da interface do usuário.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Adiciona uma janela ao ouvinte de eventos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Uma função implementada pelo cliente que é chamada pela automação da interface do usuário quando é gerado um evento que o cliente assinou.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Remove uma janela do ouvinte de eventos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera um ou mais nós de automação da interface do usuário que correspondem aos critérios de pesquisa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Obtém uma cadeia de caracteres de erro para que possa ser passada para o cliente. Esse método não é usado diretamente pelos clientes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera um <em>padrão de controle</em>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera o valor de uma propriedade de automação da interface do usuário.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera o nó de automação da interface do usuário raiz.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera o identificador de tempo de execução de um nó de automação de interface do usuário.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Atualiza o cache de valores de propriedade e padrões de controle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Obtém um objeto de padrão de controle de um tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Obtém um intervalo de texto de um tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Obtém um HUIANODE de um tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Obtém o identificador de inteiro que pode ser usado em métodos que exigem uma PROPERTYid, o PATTERNid, o CONTROLTYPEid, o textattributeid ou EVENTID.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Navega na árvore de automação da interface do usuário, recuperando opcionalmente as informações armazenadas em cache.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera o nó de automação da interface do usuário para o elemento de interface do usuário que atualmente tem o foco de entrada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera o nó de automação da interface do usuário associado a uma janela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera o nó de automação da interface do usuário para o elemento no ponto especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera o nó de automação da interface do usuário para um provedor de elementos brutos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Exclui um nó da memória.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Exclui um objeto de padrão alocado da memória.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Uma função definida pelo aplicativo que é chamada pela automação da interface do usuário para obter um provedor do lado do cliente para um elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Obtém um valor booliano que especifica se um retângulo tem todas as suas coordenadas definidas como 0.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Define os elementos de uma estrutura <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> como 0.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Registra o método definido pelo aplicativo que é chamado pela automação da interface do usuário para obter um provedor de um elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Remove um ouvinte de eventos em um nó na árvore de automação da interface do usuário.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Define o foco de entrada para o elemento especificado na interface do usuário.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Exclui um objeto de intervalo de texto alocado da memória.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes de automação da interface do usuário](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 


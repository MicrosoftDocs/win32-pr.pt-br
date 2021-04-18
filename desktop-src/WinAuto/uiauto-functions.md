---
title: Funções para provedores
description: Esta seção descreve as funções do provedor de automação de interface do usuário para aplicativos Microsoft Win32.
ms.assetid: 76012ec7-0114-4b6b-a35e-5cfde5b90230
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0542c3d0b313e1bed8ec040924349e37a29fea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105788091"
---
# <a name="functions-for-providers"></a>Funções para provedores

Esta seção descreve as funções do provedor de automação de interface do usuário para aplicativos Microsoft Win32.

## <a name="in-this-section"></a>Nesta seção



| Função                                                                                                 | Descrição                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)<br/>                       | Obtém um valor que indica se algum aplicativo cliente é assinado para eventos de automação da interface do usuário da Microsoft.<br/>                                             |
| [**UiaDisconnectAllProviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders)<br/>                         | Libera todos os recursos de automação da interface do usuário que são mantidos por todos os provedores associados ao processo de chamada. <br/>                                               |
| [**UiaDisconnectProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider)<br/>                                 | Libera Todas as referências que um provedor específico mantém aos objetos de automação da interface do usuário.<br/>                                                                      |
| [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue)<br/> | Recupera um valor reservado que indica que o valor de um atributo de texto de automação de interface de usuário varia dentro de um intervalo de texto.<br/>                                      |
| [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue)<br/>     | Recupera um valor reservado que indica que uma propriedade de automação da interface do usuário ou um atributo de texto não tem suporte.<br/>                                               |
| [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)<br/>                     | Obtém o provedor de host para uma janela.<br/>                                                                                                                    |
| [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider)<br/>                   | Recupera uma implementação de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que fornece dados da Microsoft acessibilidade ativa em nome de um provedor de automação de interface do usuário.<br/> |
| [**UiaProviderForNonClient**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfornonclient)<br/>                     | Obtém o provedor para toda a área não cliente de uma janela ou para um controle na área não cliente de uma janela.<br/>                                      |
| [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible)<br/>               | Cria um provedor de automação de interface do usuário com base no objeto especificado do Microsoft Acessibilidade Ativa.<br/>                                                          |
| [**UiaRaiseAsyncContentLoadedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseasynccontentloadedevent)<br/>     | Chamado por um provedor para notificar o núcleo de automação da interface do usuário que o conteúdo está sendo carregado de forma assíncrona.<br/>                                                      |
| [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)<br/>                     | Notifica os ouvintes de um evento.<br/>                                                                                                                         |
| [**UiaRaiseAutomationPropertyChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent)<br/>    | Chamado pelos provedores para notificar o núcleo de automação da interface do usuário de que uma propriedade do elemento foi alterada.<br/>                                                              |
| [**UiaRaiseChangesEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisechangesevent)<br/>                           | Chamado pelos provedores para notificar o núcleo de automação da interface do usuário que ocorreu uma alteração.<br/>                                                                        |
| [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**)<br/>             | Chamado pelos provedores para iniciar um evento de notificação.<br/>                                                                                                   |
| [**UiaRaiseStructureChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)<br/>         | Chamado por um provedor para notificar o núcleo de automação da interface do usuário que a estrutura de árvore alterou.<br/>                                                              |
| [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent)<br/>   | Chamado por um provedor para notificar o núcleo de automação da interface do usuário que um controle de texto alterou o texto de forma programática.<br/>                                            |
| [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)<br/>             | Obtém uma interface para o provedor de automação de interface do usuário para uma janela.<br/>                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedores de automação da interface do usuário](uiauto-entry-uiautoprovidersforwin32apps.md)
</dt> </dl>

 


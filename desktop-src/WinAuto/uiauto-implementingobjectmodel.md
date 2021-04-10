---
title: Padrão de controle ObjectModel
description: Descreve as diretrizes e convenções para implementar o IObjectModelProvider, incluindo informações sobre métodos. O padrão de controle ObjectModel é usado para expor um ponteiro para o modelo de objeto subjacente de um documento.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Automação da interface do usuário, implementando o padrão de controle ObjectModel
- Automação da interface do usuário, padrão de controle ObjectModel
- Automação da interface do usuário, IObjectModelProvider
- IObjectModelProvider
- Implementando o padrão de controle ObjectModel Automation UI
- Padrão de controle ObjectModel
- padrões de controle, IObjectModelProvider
- padrões de controle, implementando a automação da interface do usuário ObjectModel
- padrões de controle, ObjectModel
- interfaces, IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ff115233faf19f93963153a0b2a0a1ff52c3f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294275"
---
# <a name="objectmodel-control-pattern"></a>Padrão de controle ObjectModel

Descreve as diretrizes e convenções para implementar o [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), incluindo informações sobre métodos. O padrão de controle **ObjectModel** é usado para expor um ponteiro para o modelo de objeto subjacente de um documento.

Muitos aplicativos implementam modelos de objetos avançados que agregam valor além do que a automação da interface do usuário da Microsoft fornece. Esse padrão de controle permite que um cliente navegue de um elemento de automação da interface do usuário para o modelo de objeto subjacente.

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IObjectModelProvider**](#required-members-for-iobjectmodelprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **ObjectModel** , observe as seguintes diretrizes e convenções:

-   O método [**IObjectModelProvider:: GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) deve retornar um ponteiro para o objeto que é o mais próximo possível do elemento de interface do usuário de origem. Por exemplo, em um navegador da Web, um provedor de automação de interface do usuário para um único elemento deve retornar um ponteiro de modelo de objeto para o elemento. Retornar um ponteiro de modelo de objeto para a raiz do documento seria muito menos útil.
-   Espera-se que o cliente do padrão de controle **ObjectModel** tenha o IID para a interface que ele está procurando, que é o motivo pelo qual é suficiente retornar um ponteiro simples [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .
-   Como a automação da interface do usuário realiza marshaling do ponteiro para o processo do cliente, o provedor deve esperar que o cliente acesse o modelo de objeto usando práticas COM (Standard Component Object Model).

## <a name="required-members-for-iobjectmodelprovider"></a>Membros necessários para **IObjectModelProvider**

O método a seguir é necessário para implementar a interface [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) .



| Membros necessários                                                                             | Tipo de membro | Observações                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | Método      | Retorna um ponteiro COM para o modelo de objeto subjacente. Espera-se que o cliente chame o método [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar ponteiros de modelo de objeto específicos. |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 
---
title: Padrão de controle ObjectModel
description: Descreve diretrizes e convenções para implementar IObjectModelProvider, incluindo informações sobre métodos. O padrão de controle ObjectModel é usado para expor um ponteiro para o modelo de objeto subjacente de um documento.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle ObjectModel
- Automação da Interface do Usuário, padrão de controle ObjectModel
- Automação da Interface do Usuário,IObjectModelProvider
- IObjectModelProvider
- implementando Automação da Interface do Usuário padrão de controle ObjectModel
- Padrão de controle ObjectModel
- padrões de controle, IObjectModelProvider
- padrões de controle, implementando Automação da Interface do Usuário ObjectModel
- padrões de controle, ObjectModel
- interfaces,IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62081f8fb841e7827f589fd2441c7b6411810f9a71c1c1962a0dfcf8b0e37180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114989"
---
# <a name="objectmodel-control-pattern"></a>Padrão de controle ObjectModel

Descreve diretrizes e convenções para implementar [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), incluindo informações sobre métodos. O **padrão de controle ObjectModel** é usado para expor um ponteiro para o modelo de objeto subjacente de um documento.

Muitos aplicativos implementam modelos de objeto avançados que agregam valor além do que o Microsoft Automação da Interface do Usuário fornece. Esse padrão de controle permite que um cliente navegue de um Automação da Interface do Usuário para o modelo de objeto subjacente.

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IObjectModelProvider**](#required-members-for-iobjectmodelprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle ObjectModel,** observe as seguintes diretrizes e convenções:

-   O [**método IObjectModelProvider::GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) deve retornar um ponteiro para o objeto que é o mais próximo possível do elemento de interface do usuário de origem. Por exemplo, em um navegador da Web, um provedor Automação da Interface do Usuário para um único elemento deve retornar um ponteiro de modelo de objeto para o elemento . Retornar um ponteiro de modelo de objeto para a raiz do documento seria muito menos útil.
-   Espera-se que o cliente do padrão de controle **ObjectModel** tenha o IID para a interface que está procurando, por isso é suficiente retornar um ponteiro [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) simples.
-   Como Automação da Interface do Usuário marshals do ponteiro para o processo do cliente, o provedor deve esperar que o cliente acesse o modelo de objeto usando as práticas PADRÃO Component Object Model (COM).

## <a name="required-members-for-iobjectmodelprovider"></a>Membros necessários para **IObjectModelProvider**

O método a seguir é necessário para implementar a interface [**IObjectModelProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider)



| Membros necessários                                                                             | Tipo de membro | Observações                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | Método      | Retorna um ponteiro COM para o modelo de objeto subjacente. Espera-se que o cliente chame o [**método IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar ponteiros específicos do modelo de objeto. |



 

Esse padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 
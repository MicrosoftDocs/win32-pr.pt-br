---
title: Padrão de controle textchild
description: Apresenta diretrizes e convenções para implementar ITextChildProvider, incluindo informações sobre propriedades e métodos. O padrão de controle textchild é usado para acessar o ancestral mais próximo de um elemento que dá suporte ao padrão de controle de texto.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- Automação da interface do usuário, implementando padrão de controle textchild
- Automação da interface do usuário, padrão de controle textfilho
- Automação da interface do usuário, ITextChildProvider
- ITextChildProvider
- Implementando padrões de controle textchild da automação da interface do usuário
- Padrões de controle textchild
- padrões de controle, ITextChildProvider
- padrões de controle, implementando a automação da interface do usuário
- padrões de controle, textchild
- interfaces, ITextChildProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5c7bfb1852a02efc7baa789e137a4c05e2c2e85a65606109b26a622dfafcf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929029"
---
# <a name="textchild-control-pattern"></a>Padrão de controle textchild

Apresenta diretrizes e convenções para implementar [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), incluindo informações sobre propriedades e métodos. O padrão de controle **textchild** é usado para acessar o ancestral mais próximo de um elemento que dá suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) .

Por exemplo, suponha que o texto em um documento contenha uma imagem inserida e um hiperlink, conforme mostrado na imagem a seguir.

![captura de tela mostrando o texto que contém uma imagem inserida e um hiperlink](images/textchild-pattern.png)

Se você usar as ferramentas de automação da interface do usuário da Microsoft para examinar a árvore de automação da interface do usuário desse conteúdo do documento, ele poderá mostrar um elemento de documento com um elemento filho que representa a imagem e outro elemento filho que representa o hiperlink. Por exemplo:

![captura de tela mostrando inspecionar relatórios um exemplo de árvore de elementos de automação da interface do usuário](images/textchild-pattern-tree.png)

Normalmente, o elemento Document no exemplo anterior dá suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) , mas os dois filhos do elemento Document não. Se um aplicativo cliente de automação da interface do usuário tiver uma referência ao elemento Image ou ao elemento Hyperlink, o cliente poderá usar o padrão de controle **textchild** como uma maneira conveniente de acessar o padrão TextControl exposto pelo elemento de documento que o contém.

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar a interface [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) , observe as seguintes diretrizes e convenções:

-   A propriedade [**ITextChildProvider:: TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) deve especificar o elemento ancestral mais próximo que dá suporte à interface [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) , independentemente de os elementos mais altos na cadeia ancestral também oferecerem suporte a **ITextProvider**.
-   Um elemento não deve dar suporte à interface [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [ITextChildProvider * *](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .
- Um elemento que implementa [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) deve ser um filho, ou descendente, de um elemento que implementa [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider). Não é necessário que esse elemento também implemente o [padrão de controle de texto](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).
-   A propriedade [**ITextChildProvider:: TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) deve especificar o mesmo intervalo de texto que o elemento do provedor de texto que o contém retorna quando sua função [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) é chamada com o elemento filho Text como o elemento filho incluído.

## <a name="required-members-for-itextchildprovider"></a>Membros necessários para **ITextChildProvider**

Essas propriedades e métodos são necessários para implementar a interface [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .



| Membros necessários                                                     | Tipo de membro | Observações |
|----------------------------------------------------------------------|-------------|-------|
| [**TextContainer**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | Propriedade    | Nenhum  |
| [**TextRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | Propriedade    | Nenhum  |



 

Este padrão de controle não tem nenhum método ou evento associado.

## <a name="related-topics"></a>Tópicos relacionados

**Conceitua**

- [Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
- [Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
- [Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
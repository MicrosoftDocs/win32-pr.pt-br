---
title: Padrão de controle de anotação
description: Descreve diretrizes e convenções para implementar IAnnotationProvider, incluindo informações sobre propriedades e métodos. O padrão de controle Anotação é usado para expor as propriedades de uma anotação em um documento.
ms.assetid: 5A334991-66AF-4A82-9A09-09D5BDAAA771
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle de anotação
- Automação da Interface do Usuário,padrão de controle de anotação
- Automação da Interface do Usuário,IAnnotationProvider
- IAnnotationProvider
- implementando Automação da Interface do Usuário padrão de controle de anotação
- padrão de controle de anotação
- padrões de controle, IAnnotationProvider
- padrões de controle, implementando Automação da Interface do Usuário anotação
- padrões de controle, anotação
- interfaces,IAnnotationProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cdc5c37c61878513b5d01812ab73c086f87d182d4b2c955efaf8706d52e4bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505247"
---
# <a name="annotation-control-pattern"></a>Padrão de controle de anotação

Descreve diretrizes e convenções para implementar [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider), incluindo informações sobre propriedades e métodos. O **padrão de controle** Anotação é usado para expor as propriedades de uma anotação em um documento.

Um exemplo é um balão de comentário que está na margem de um documento e está conectado a algum texto do documento ou a uma célula de planilha.

A ilustração a seguir mostra um exemplo de uma anotação. Para exemplos de controles que implementam esse padrão de controle, consulte [Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

![captura de tela mostrando um comentário em um documento](images/annotation.png)

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IAnnotationProvider**](#required-members-for-iannotationprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle** De anotação, observe as seguintes diretrizes e convenções:

-   Há muitos tipos diferentes de anotações. O arquivo de header UIAutomationClient.h define um conjunto de valores constantes nomeados que identificam os tipos de anotações que a Microsoft Automação da Interface do Usuário dá suporte. Para obter mais informações, consulte [**Identificadores de tipo de anotação**](uiauto-annotation-type-identifiers.md).
-   Se você usar [**AnnotationType \_ Unknown**](uiauto-annotation-type-identifiers.md), deverá implementar a propriedade [**IAnnotationProvider::AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) para permitir que os clientes descubram o nome do tipo de anotação. Você não precisa implementar **AnnotationTypeName** para um tipo de anotação padrão porque Automação da Interface do Usuário fornece um nome padrão, mas pode implementá-lo se precisar substituir o nome padrão.
-   A [**propriedade IAnnotationProvider::Author**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author) é opcional.
-   A [**propriedade IAnnotationProvider::D ateTime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime) é opcional.
-   A propriedade [**IAnnotationProvider::Target**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target) é necessária porque vincula uma anotação a um elemento de interface do usuário, permitindo que um cliente navegue da anotação de volta para o elemento de interface do usuário ao qual a anotação se refere.
-   Como as anotações podem assumir muitas formas diferentes, a interface [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) não define uma propriedade para armazenar o valor ou o texto de uma anotação. Uma anotação simples deve expor a interface [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) e a propriedade [**IValueProvider::Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) deve retornar um valor somente leitura que especifica o texto da anotação. Uma anotação mais rica deve expor a interface [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) para fornecer texto mais rico aos clientes.
-   Navegar de um elemento de interface do usuário para uma anotação no elemento depende do tipo de elemento que está sendo anotado, da seguinte forma:
    -   Para células de planilha, implemente o método [**ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) para se referir à anotação.
    -   Para conteúdo textual, implemente o atributo de texto [**AnnotationObjects**](uiauto-textattribute-ids.md) na interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) para se referir à anotação.
-   Alguns tipos de anotações não exigem uma implementação completa da interface [**IAnnotationProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) Por exemplo, um indicador de erro de ortografia simples pode ser representado fazendo com que a interface [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) retorne um atributo de texto [**AnnotationTypes**](uiauto-textattribute-ids.md) de [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)e um valor nulo para o atributo de texto [**AnnotationObjects.**](uiauto-textattribute-ids.md)
-   Pode ser útil implementar a interface [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) em um elemento de interface do usuário que não está visível. Por exemplo, você pode criar um elemento Automação da Interface do Usuário que implementa **IAnnotationProvider** para fornecer informações estendidas sobre um erro de gramática.
-   As anotações em um controle baseado em texto poderão ser complexas se o controle contiver comentários sobrepostos. Use as seguintes diretrizes para lidar com anotações complexas:
    -   Um intervalo de texto sem anotações deve retornar uma matriz vazia para o atributo de texto [**AnnotationTypes**](uiauto-textattribute-ids.md) e uma matriz vazia para o atributo de texto [**AnnotationObjects.**](uiauto-textattribute-ids.md)
    -   Um intervalo de texto com uma anotação deve retornar uma matriz de um valor inteiro para o atributo de texto [**AnnotationTypes**](uiauto-textattribute-ids.md) e uma matriz de uma interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para o atributo de texto [**AnnotationObjects.**](uiauto-textattribute-ids.md)
    -   Um intervalo de texto com várias anotações deve retornar uma matriz de vários valores inteiros para o atributo de texto [**AnnotationTypes**](uiauto-textattribute-ids.md) e uma matriz de um número correspondente de interfaces [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para o atributo de texto [**AnnotationObjects.**](uiauto-textattribute-ids.md)
    -   Um intervalo de texto com anotações variadas, como um intervalo com texto anotado e não anotado, deve retornar a propriedade [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) para [**AnnotationTypes**](uiauto-textattribute-ids.md) e [**AnnotationObjects**](uiauto-textattribute-ids.md). Um cliente que recebe essa resposta pode subdividir o intervalo de texto para descobrir onde as anotações começam e terminam.

## <a name="required-members-for-iannotationprovider"></a>Membros necessários para **IAnnotationProvider**

As propriedades a seguir são necessárias para implementar a interface [**IAnnotationProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider)



| Membros necessários                                                                | Tipo de membro | Observações |
|---------------------------------------------------------------------------------|-------------|-------|
| [**AnnotationTypeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)     | Propriedade    | Nenhum. |
| [**AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) | Propriedade    | Nenhum. |
| [**Autor**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author)                         | Propriedade    | Nenhum. |
| [**Datetime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime)                     | Propriedade    | Nenhum. |
| [**Destino**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target)                         | Propriedade    | Nenhum. |



 

Esse padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 
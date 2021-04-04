---
title: Criando o objeto CUIAutomation
description: Esta seção descreve como começar a escrever um aplicativo cliente de automação da interface do usuário da Microsoft instanciando um objeto que implementa o IUIAutomation.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- clientes, criando objeto CUIAutomation
- clientes, objeto CUIAutomation
- Automação da interface do usuário, objeto CUIAutomation
- Automação da interface do usuário, criando objeto CUIAutomation
- Criando objeto CUIAutomation
- Objeto CUIAutomation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917362"
---
# <a name="creating-the-cuiautomation-object"></a>Criando o objeto CUIAutomation

Esta seção descreve como começar a escrever um aplicativo cliente de automação da interface do usuário da Microsoft instanciando um objeto que implementa o [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).

Este tópico inclui as seções a seguir.

-   [O objeto CUIAutomation](#the-cuiautomation-object)
-   [Criando o objeto](#creating-the-object)
-   [Tópicos relacionados](#related-topics)

## <a name="the-cuiautomation-object"></a>O objeto CUIAutomation

A primeira etapa no uso da automação da interface do usuário é criar um objeto da classe [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) . Esse objeto expõe a interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , que é o gateway para todos os outros objetos e interfaces que são usados por aplicativos cliente. Entre outras coisas, o **IUIAutomation** é usado para as seguintes tarefas:

-   Inscrevendo-se em eventos.
-   Criando condições. Condições são objetos usados para restringir o escopo de pesquisas para elementos de automação da interface do usuário.
-   Obter elementos de automação da interface do usuário diretamente da área de trabalho (o elemento raiz) ou de coordenadas de tela ou identificadores de janela.
-   Criação de objetos Tree Walker que podem ser usados para navegar pela hierarquia de elementos de automação da interface do usuário.
-   Convertendo tipos de dados.

## <a name="creating-the-object"></a>Criando o objeto

Para começar a usar a automação de interface do usuário em seu aplicativo, execute as seguintes etapas:

-   Inclua automação da IU. h em seus cabeçalhos de projeto. Automação da IU. h traz os outros cabeçalhos que definem a API.
-   Declare um ponteiro para [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).
-   Inicialize a Component Object Model (COM).
-   Crie uma instância de [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) e recupere a interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) em seu ponteiro.

A função de exemplo a seguir inicializa COM e, em seguida, cria o objeto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , recuperando a interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) no ponteiro *ppAutomation* .


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> <dt>

[Obtendo elementos da automação interface do usuário](uiauto-obtainingelements.md)
</dt> </dl>

 

 
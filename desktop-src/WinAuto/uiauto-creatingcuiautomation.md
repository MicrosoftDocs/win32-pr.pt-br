---
title: Criando o objeto CUIAutomation
description: Esta seção descreve como começar a escrever um aplicativo cliente microsoft Automação da Interface do Usuário, instando um objeto que implementa IUIAutomation.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- clientes, criando o objeto CUIAutomation
- clients, objeto CUIAutomation
- Automação da Interface do Usuário,objeto CUIAutomation
- Automação da Interface do Usuário, criando o objeto CUIAutomation
- criando o objeto CUIAutomation
- Objeto CUIAutomation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b9720ce31f883c4561ae3f82372d902a0dcc3fbfca4bae6de998ce438a6d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795486"
---
# <a name="creating-the-cuiautomation-object"></a>Criando o objeto CUIAutomation

Esta seção descreve como começar a escrever um aplicativo cliente microsoft Automação da Interface do Usuário, instando um objeto que implementa [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).

Este tópico inclui as seções a seguir.

-   [O objeto CUIAutomation](#the-cuiautomation-object)
-   [Criando o objeto](#creating-the-object)
-   [Tópicos relacionados](#related-topics)

## <a name="the-cuiautomation-object"></a>O objeto CUIAutomation

A primeira etapa no uso Automação da Interface do Usuário é criar um objeto da [**classe CUIAutomation.**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) Esse objeto expõe a interface [**IUIAutomation,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) que é o gateway para todos os outros objetos e interfaces usados por aplicativos cliente. Entre outras coisas, **IUIAutomation** é usado para as seguintes tarefas:

-   Assinando eventos.
-   Criando condições. As condições são objetos usados para restringir o escopo de pesquisas Automação da Interface do Usuário elementos.
-   Obter Automação da Interface do Usuário diretamente da área de trabalho (o elemento raiz) ou de coordenadas de tela ou alças de janela.
-   Criando objetos de árvore que podem ser usados para navegar na hierarquia de Automação da Interface do Usuário elementos.
-   Convertendo tipos de dados.

## <a name="creating-the-object"></a>Criando o objeto

Para começar a usar Automação da Interface do Usuário em seu aplicativo, tome as seguintes etapas:

-   Inclua UIAutomation.h em seus headers de projeto. UIAutomation.h traz os outros headers que definem a API.
-   Declare um ponteiro para [**IUIAutomation.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)
-   Inicialize o Component Object Model (COM).
-   Crie uma instância de [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) e recupere a interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) em seu ponteiro.

A função de exemplo a seguir inicializa COM e, em seguida, cria o objeto [**CUIAutomation,**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) recuperando a interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) no *ponteiro ppAutomation.*


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

**Conceitual**
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> <dt>

[Obtendo elementos da automação interface do usuário](uiauto-obtainingelements.md)
</dt> </dl>

 

 
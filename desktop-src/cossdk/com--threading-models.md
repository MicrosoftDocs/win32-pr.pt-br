---
description: Os modelos de Threading COM+ são projetados em uma coleção de objetos chamada Apartment. Um apartamento é uma coleção de contextos contidos em um processo.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Modelos de Threading COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f07b065861c042e68add633368a9c8b8ba41b2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "103663694"
---
# <a name="com-threading-models"></a>Modelos de Threading COM+

Os modelos de Threading COM+ são projetados em uma coleção de objetos chamada Apartment. Um apartamento é uma coleção de contextos contidos em um processo, conforme mostrado na ilustração a seguir.

![Diagrama que mostra uma coleção de contextos em uma atividade, dentro de um apartamento, dentro de um processo.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

Chamadas em um apartamento são diretas, enquanto chamadas entre Apartments (fora do processo) são indiretas e exigem código de proxy e stub. Apartments permitem objetos com diferentes propriedades de sincronização e reentrância e têm duas categorias: thread único e multithread. Os objetos em um STA (single-threaded apartment) são executados no thread específico em que foram criados. STAs permite que apenas um método seja executado de cada vez. Eles são projetados para interfaces do usuário e contam com a fila de mensagens do Microsoft Windows para processar chamadas de entrada.

Os objetos em um apartamento multithread (MTA) são executados em qualquer thread e permitem que qualquer número de métodos ocorra simultaneamente. MTAs dá suporte à reentrada implícita.

As classes COM+ são marcadas com uma propriedade **ThreadingModel** que permite que o com+ crie o objeto no apartamento apropriado. Para determinar em qual apartamento um objeto é criado, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa a propriedade **ThreadingModel** .

Os threads devem chamar [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) antes que possam usar com+. Isso os cria dentro do apartamento e do contexto corretos. O apartamento principal do thread é determinado como o primeiro STA chamado por **CoInitializeEx**. Isso geralmente é associado ao thread principal de um processo. **CoInitializeEx** indica o tipo de apartamento exigido pelo thread definindo os seguintes sinalizadores:

-   **COinit \_ Multithread**– localiza o thread no único apartamento multi-threaded.
-   **COinit \_ APARTMENTTHREADED**— coloca o thread em um novo Sta.

Os tópicos a seguir nesta seção fornecem mais informações sobre como usar modelos de threading e Apartments no COM+:

-   [Atributo de modelo de Threading](threading-model-attribute.md)
-   [Apartments neutro](neutral-apartments.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processos, threads e Apartments](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[**ThreadingModel**](components.md)
</dt> </dl>

 

 

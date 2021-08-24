---
description: Os modelos de threading COM+ são projetados em torno de uma coleção de objetos chamada apartment. Um apartment é uma coleção de contextos contidos em um processo.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Modelos de threading COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0949a27291be43b5981f24f4985fac6911937b2c9fa85785b4d662bd1bf546
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793667"
---
# <a name="com-threading-models"></a>Modelos de threading COM+

Os modelos de threading COM+ são projetados em torno de uma coleção de objetos chamada apartment. Um apartment é uma coleção de contextos contidos em um processo, conforme mostrado na ilustração a seguir.

![Diagrama que mostra uma coleção de contextos em uma atividade, dentro de um apartment, dentro de um processo.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

As chamadas em um apartment são diretas, enquanto as chamadas entre apartments (fora de processo) são indiretas e exigem código de proxy e stub. Apartments permitem objetos com diferentes propriedades de sincronização e reentração e têm duas categorias: single-threaded e multithreaded. Os objetos em um STA (single-threaded apartment) são executados no thread específico em que foram criados. STAs permitem que apenas um método seja executado por vez. Eles são projetados para interfaces do usuário e dependem da fila de mensagens do Microsoft Windows para processar chamadas de entrada.

Os objetos em um MTA (multithreaded apartment) são executados em qualquer thread e permitem que qualquer número de métodos ocorra simultaneamente. Os MTAs suportam a reentrância implicitamente.

As classes COM+ são marcadas **com uma propriedade ThreadingModel** que permite que COM+ crie o objeto no apartment adequado. Para determinar em qual apartment um objeto é criado, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa a **propriedade ThreadingModel.**

Os threads devem chamar [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) antes que possam usar COM+. Isso os cria dentro do apartment e do contexto corretos. O apartment do thread principal é determinado como o primeiro STA chamado por **CoInitializeEx.** Isso geralmente é associado ao thread principal de um processo. **CoInitializeEx** indica o tipo de apartment exigido pelo thread definindo os seguintes sinalizadores:

-   **COINIT \_ MULTITHREADED**— localiza o thread no único apartment multithreaded.
-   **COINIT \_ APARTMENTTHREADED**— coloca o thread em um novo STA.

Os tópicos a seguir nesta seção fornecem mais informações sobre como usar modelos de threading e apartments no COM+:

-   [Atributo de modelo de threading](threading-model-attribute.md)
-   [Apartments neutros](neutral-apartments.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processos, threads e apartments](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[**Threadingmodel**](components.md)
</dt> </dl>

 

 

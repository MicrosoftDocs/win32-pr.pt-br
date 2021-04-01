---
description: Adicionando objetos de efeito e transição
ms.assetid: fe82392f-33e2-432a-a6e3-710e475547b3
title: Adicionando objetos de efeito e transição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6d33ed27faa0c69a755a17c72d9c5b136a4670
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009952"
---
# <a name="adding-effect-and-transition-objects"></a>Adicionando objetos de efeito e transição

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

No DES, um efeito ou uma transição é representado por dois objetos:

-   Um *objeto de linha do tempo* representa o efeito ou a transição dentro da linha do tempo. Para efeitos, o objeto Timeline dá suporte à interface [**IAMTimelineEffect**](iamtimelineeffect.md) . Para transições, ele dá suporte à interface [**IAMTimelineTrans**](iamtimelinetrans.md) . Os dois tipos dão suporte à interface [**IAMTimelineObj**](iamtimelineobj.md) .
-   O *subobjeto* é um objeto que implementa o processamento de dados para o efeito ou a transição. O objeto Timeline contém um ponteiro para o subobjeto.

Para adicionar um efeito ou uma transição, execute as etapas a seguir.

**1. criar o objeto de linha do tempo**

Para criar o objeto Timeline, chame o método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) . Defina o tipo igual ao **\_ efeito de \_ tipo \_ principal da linha do tempo** para um efeito ou para a **\_ \_ \_ transição de tipo principal da linha do tempo** para uma transição.

O exemplo a seguir cria um objeto de transição:


```C++
IAMTimelineObj *pTransObj = NULL;
pTimeline->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);
```



**2. Especifique o subobjeto**

O objeto Timeline atua como um wrapper para outro objeto, chamado de *subobjeto*, que faz o trabalho real. O subobjeto implementa uma transformação de dados que produz o efeito ou a transição desejada. Para obter uma lista de transições e efeitos fornecidos com o DES, consulte [transições e efeitos](transitions-and-effects.md).

Para definir o subobjeto, chame o método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) no objeto Timeline, passando-o identificador de classe (CLSID) do subobjeto. O DirectShow fornece um enumerador para efeitos de vídeo e transições de vídeo, que você pode usar para obter o CLSID. Para obter mais informações, consulte [enumerando efeitos e transições](enumerating-effects-and-transitions.md).

O exemplo a seguir define a [transição de apagamento SMPTE](smpte-wipe-transition.md) como o subobjeto:


```C++
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe
```



**3. definir os horários de início e de término**

Para definir os horários de início e de parada, chame o método [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) . Esses tempos são relativos à hora de início do objeto pai. Os efeitos podem se sobrepor dentro do mesmo objeto, mas as transições não podem.

O exemplo a seguir define a hora de início como 5 segundos e a hora de término como 10 segundos:


```C++
const REFERENCE_TIME ONE_SECOND = 10000000
hr = pTransObj->SetStartStop(5 * ONE_SECOND, 10 * ONE_SECOND);
```



Quando uma transição é renderizada, o progresso da transição em cada quadro é calculado com base em uma propriedade **Progress** , que é normalizada para um intervalo de 0,0 a 1,0. O DES usa a hora de início de cada quadro para calcular o valor de progresso. Isso significa que se a hora de parada da transição for igual à hora de parada da origem, o valor de **progresso** nunca alcançará exatamente 1,0, pois a hora de início do último quadro será um pouco diferente da hora de parada. Para fazer com que a transição alcance 1,0, defina a hora de parada da transição como pelo menos um quadro anterior à hora de parada da origem.

**4. inserir o objeto na linha do tempo**

Para inserir o objeto na linha do tempo, chame um dos seguintes métodos no pai, dependendo do tipo de objeto:

-   Efeitos: [ **IAMTimelineEffectable:: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)
-   Transições: [ **IAMTimelineTransable:: TransAdd**](iamtimelinetransable-transadd.md)

No método [**IAMTimelineEffectable:: EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md) , você deve especificar a prioridade do efeito. Quando os efeitos se sobrepõem no mesmo objeto, eles são aplicados em ordem de prioridade. O efeito de áudio de envelope de volume é uma exceção; consulte a referência de [efeito de envelope de volume](volume-envelope-effect.md) para obter detalhes. Em uma composição, todas as faixas de áudio são misturadas antes que os efeitos de áudio para essa composição sejam aplicados.

Como as transições não podem se sobrepor no mesmo objeto, elas não têm um valor de prioridade.

O exemplo a seguir adiciona o objeto de transição a uma faixa:


```C++
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
```



O exemplo consulta o objeto Track para a interface [**IAMTimelineTransable**](iamtimelinetransable.md) antes de chamar addTrans.

**5. definir propriedades**

Muitos efeitos e transições dão suporte a propriedades personalizadas. Para obter informações, consulte [definindo propriedades em efeitos e transições](setting-properties-on-effects-and-transitions.md).

Exemplo

O exemplo de código a seguir adiciona uma [transição de apagamento SMPTE](smpte-wipe-transition.md) a uma faixa. Ele pressupõe que o objeto Track já existe na linha do tempo.


```C++
IAMTimeline *pTL;
IAMTimelineTrack *pTrack;

// Create timeline with track (not shown).

// Create the transition object. 
IAMTimelineObj *pTransObj = NULL;
hr = pTL->CreateEmptyNode(&pTransObj, TIMELINE_MAJOR_TYPE_TRANSITION);

// Set the subobject. 
hr = pTransObj->SetSubObjectGUID(CLSID_DxtJpeg);  // SMPTE Wipe

// Set the start and stop times. 
hr = pTransObj->SetStartStop(50000000, 100000000);

// Insert the transition object into the timeline. 
IAMTimelineTransable *pTransable = NULL;
hr = pTrack->QueryInterface(IID_IAMTimelineTransable, (void **)&pTransable);
hr = pTransable->TransAdd(pTransObj);  
pTransable->Release();
pTransObj->Release();
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com efeitos e transições](working-with-effects-and-transitions.md)
</dt> </dl>

 

 




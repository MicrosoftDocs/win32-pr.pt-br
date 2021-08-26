---
description: Criando objetos de linha do tempo
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Criando objetos de linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c0a2a88b2cd931e6a9d12274f4a2503b4c97d52348b6ed2629c22bf204f302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054776"
---
# <a name="creating-timeline-objects"></a>Criando objetos de linha do tempo

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

O código de exemplo apresentado neste artigo começa com uma linha do tempo vazia, mas as mesmas etapas se aplicam se você carregar um projeto existente e quiser adicionar objetos a ele.

Para criar qualquer tipo de objeto na linha do tempo, chame o método [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) . Por exemplo, o código a seguir cria um novo grupo:


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



O segundo parâmetro é um membro da enumeração [**de \_ \_ tipo principal da linha do tempo**](timeline-major-type.md) . Especifica o tipo de objeto de linha do tempo a ser criado, como um grupo ou uma faixa.

O método **CreateEmptyNode** cria o objeto e retorna um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto. Ele também incrementa a contagem de referência na interface **IAMTimelineObj** , portanto, você deve liberar a interface quando terminar de usá-la. Não chame a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) . Em vez disso, sempre use **CreateEmptyNode** para criar um objeto de linha do tempo, porque ele inicializa o novo objeto para uso em uma linha do tempo.

A interface [**IAMTimelineObj**](iamtimelineobj.md) é uma interface genérica. Ele fornece métodos que são comuns a todos os tipos de objeto de linha do tempo. Cada tipo de objeto também expõe outras interfaces. Por exemplo, os grupos expõem a interface [**IAMTimelineGroup**](iamtimelinegroup.md) , entre outros. Você pode obter ponteiros para as outras interfaces chamando **QueryInterface**.

Depois de criar um objeto, ele ainda não faz parte da linha do tempo. O método para adicionar um objeto à linha do tempo depende do tipo de objeto. A seção a seguir descreve como adicionar grupos, composições e faixas à linha do tempo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Construindo uma linha do tempo](constructing-a-timeline.md)
</dt> </dl>

 

 

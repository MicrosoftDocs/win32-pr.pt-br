---
description: Adicionando uma fonte
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Adicionando uma fonte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab2440ff50bbb4a3a610f9341405538a88dc6bf16ce2153a327f3b4578f3aec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690526"
---
# <a name="adding-a-source"></a>Adicionando uma fonte

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Crie um objeto de origem da mesma maneira que cria outros objetos de linha do tempo. Antes de inseri-lo na linha do tempo, no entanto, você deve especificar pelo menos as propriedades a seguir na origem.

-   Os horários de início e de término, em relação à linha do tempo. Chame o método [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) .
-   O arquivo de mídia a ser usado como origem. Chame o método [**IAMTimelineSrc:: Setmedianame**](iamtimelinesrc-setmedianame.md) com uma cadeia de caracteres largo representando o nome do arquivo.
-   Os horários de início e de término da mídia, que são relativos ao arquivo original. Chame o método [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) . para obter mais informações sobre os tempos de mídia, consulte [tempo em DirectShow serviços de edição](time-in-directshow-editing-services.md).

No exemplo a seguir, o clipe de origem inicia quatro segundos no arquivo. A duração da mídia é de 10 segundos, duas vezes o comprimento da duração da linha do tempo, o que significa que a fonte será reproduzida em duas vezes a velocidade normal. As unidades de constante são definidas como 10 milhões (10 ^ 7) e são iguais a um segundo.


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> Atualmente, o DES não pode renderizar simultaneamente mais de 75 fontes que foram compactadas com codecs do VCM (Gerenciador de compactação de vídeo). Além disso, se o projeto como um todo contiver mais de 75 fontes, você deverá usar a reconexão dinâmica ou o DES não poderá visualizar o projeto. Para obter mais informações, consulte [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

 

Para obter mais informações sobre fontes, consulte [trabalhando com fontes](working-with-sources.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Construindo uma linha do tempo](constructing-a-timeline.md)
</dt> </dl>

 

 




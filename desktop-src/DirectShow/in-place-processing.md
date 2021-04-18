---
description: Processamento de In-Place
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: Processamento de In-Place
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105766304"
---
# <a name="in-place-processing"></a>Processamento de In-Place

Determinadas transformações de dados podem ser realizadas com a modificação direta dos dados. Isso é chamado *de* processamento in-loco. Muitos efeitos de áudio e vídeo podem ser feitos dessa maneira. Se um DMO der suporte ao processamento in-loco, ele expõe a interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) . O processamento in-loco é geralmente mais eficiente do que usar buffers separados para a saída. (Uma exceção principal é quando o buffer reside na memória de vídeo. Nessa situação, as operações de leitura são muito mais lentas do que as operações de gravação, portanto, o processamento in-loco não é recomendado.)

Para processar dados no local, o cliente faz uma única chamada para o método [**IMediaObjectInPlace::P modelos**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) , em vez de chamadas separadas para **ProcessInput** e **ProcessOutput**. O método **process** é síncrono; todo o processamento ocorre dentro da chamada. Além disso, o processamento in-loco não usa objetos **IMediaBuffer** . O método **process** usa um ponteiro diretamente para o buffer de memória.

Um DMO que dá suporte ao processamento in-loco ainda deve implementar a interface **IMediaObject** , incluindo os métodos **ProcessInput** e **ProcessOutput** . O cliente pode escolher se deseja usar o processamento in-loco ou usar buffers separados. No entanto, não misture os dois tipos de processamento. Se você chamar **process**, não chame **ProcessInput** ou **ProcessOutput**, e vice-versa.

**Caudas de efeito**

Um DMO in-loco pode criar uma saída adicional depois que a entrada é interrompida. Isso é chamado de *cauda de efeito*. Por exemplo, um efeito de reverberação continua depois que a entrada chega a silêncio. Se houver um final de efeito, o método **process** retornará S \_ false. Depois que o aplicativo processa todos os seus dados, ele pode gerar a cauda do efeito enviando buffers vazios para o método **process** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hospedando diretamente um DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 




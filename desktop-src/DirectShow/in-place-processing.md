---
description: In-Place processamento
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: In-Place processamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b1a72b6bad2311a9c96bdd94e7e63acdc7e4961b51e106324dbe38de9510ad2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818791"
---
# <a name="in-place-processing"></a>In-Place processamento

Determinadas transformações de dados podem ser realizadas modificando diretamente os dados. Isso é chamado *de processamento in-place.* Muitos efeitos de áudio e vídeo podem ser feitos dessa maneira. Se um DMO dá suporte ao processamento in-loco, ele expõe a interface [**IMediaObjectInPlace.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) O processamento in-locar geralmente é mais eficiente do que usar buffers separados para a saída. (Uma exceção principal é quando o buffer reside na memória de vídeo. Nessa situação, as operações de leitura são muito mais lentas do que as operações de gravação, portanto, o processamento in-locar não é recomendado.)

Para processar dados no local, o cliente faz uma única chamada para o método [**IMediaObjectInPlace::P rocess,**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) em vez de chamadas separadas para **ProcessInput** e **ProcessOutput.** O **método** Process é síncrono; todo o processamento ocorre dentro da chamada. Além disso, o processamento in-loco não usa **objetos IMediaBuffer.** O **método** Process leva um ponteiro diretamente para o buffer de memória.

Um DMO que dá suporte ao processamento in-loco ainda deve implementar a interface **IMediaObject,** incluindo os métodos **ProcessInput** e **ProcessOutput.** O cliente pode escolher se deve usar o processamento in-locar ou usar buffers separados. No entanto, não misture os dois tipos de processamento. Se você chamar **Process**, não chame **ProcessInput** ou **ProcessOutput** e vice-versa.

**Efeito Tails**

Uma configuração in-locar DMO pode criar alguma saída adicional após a parada da entrada. Isso é chamado de cauda *de efeito.* Por exemplo, um efeito reverb continua depois que a entrada atinge o silêncio. Se houver uma cauda de efeito, o **método Process** retornará S \_ FALSE. Depois que o aplicativo processar todos os seus dados, ele poderá gerar a parte final do efeito enviando buffers vazios para o **método** Process.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Hospedando diretamente um DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 




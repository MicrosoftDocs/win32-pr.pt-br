---
description: Arquitetura de DMO
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: Arquitetura de DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105752071"
---
# <a name="dmo-architecture"></a>Arquitetura de DMO

Esta seção descreve a arquitetura geral de um DMO.

**Fluxos**

Um DMO é um objeto que usa *m* entradas e produz *n* saídas. As entradas e saídas são chamadas de *fluxos*. Todo DMO tem pelo menos um fluxo. Fluxos não são objetos; Eles são simplesmente referenciados no DMO por número de índice. O número de fluxos é fixo no tempo de design.

**Tipos de mídia**

Todos os dados são digitados usando um *tipo de mídia*, que define como interpretar o conteúdo dos dados. Por exemplo, o vídeo RGB de 320 x 240 24 bits é um tipo; 44,1-kilohertz (kHz) o áudio PCM do estéreo de 16 bits é outro tipo. Os tipos de mídia são descritos usando a estrutura do [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Antes que o cliente possa processar quaisquer dados, ele deve definir o tipo de mídia para cada fluxo no DMO.

Normalmente, um fluxo pode aceitar um intervalo de tipos de mídia. Alguns DMOs dão suporte a um intervalo mais amplo de tipos do que outros. As interfaces DMO definem métodos para o cliente descobrirem os tipos com suporte. Por exemplo, um DMO pode dar suporte a vídeo RGB a qualquer profundidade de bits, enquanto outro pode dar suporte apenas a RGB de 24 bits. Além disso, um DMO pode ser limitado a determinadas combinações de entradas e saídas. Por exemplo, se o tipo de entrada é vídeo de 16 bits, o fluxo de saída pode exigir a mesma profundidade de bits. O cliente pode enumerar os tipos preferenciais de cada fluxo e, em seguida, testar combinações específicas.

**Buffers**

No modelo de DMO padrão, o cliente aloca buffers de entrada separados e buffers de saída. Ele preenche os buffers de entrada com os dados e os entrega para o DMO, e o DMO grava novos dados nos buffers de saída.

Opcionalmente, um DMO pode dar suporte ao processamento "in-loco". Com o processamento in-loco, o DMO grava a saída diretamente no buffer de entrada, nos dados originais. O processamento in-loco elimina a necessidade de buffers separados. Por outro lado, ele altera os dados originais, o que pode não ser aceitável para alguns aplicativos.

O modelo de buffer padrão (não no local) é suportado por meio da interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . Todos os DMOs devem implementar essa interface. Se um DMO der suporte ao processamento in-loco, ele também expõe a interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) . O cliente é responsável por alocar todos os buffers, entrada e saída.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o DMOs](about-dmos.md)
</dt> </dl>

 

 




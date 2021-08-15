---
description: Vantagens do streaming multimídia
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Vantagens do streaming multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06df23ce833462aee9b7d4b3840c1fae2d4f3b15c4ee6daee2e4a421259493a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537536"
---
# <a name="advantages-of-multimedia-streaming"></a>Vantagens do streaming multimídia

> [!Note]  
> Essas APIs foram preterida. Os aplicativos devem usar [**o filtro Grabber de**](sample-grabber-filter.md) exemplo ou implementar um filtro personalizado para obter dados de um DirectShow de filtro.

 

Quando os desenvolvedores usam streaming multimídia em seus aplicativos, isso reduz consideravelmente a quantidade de programação específica de formato necessária. Normalmente, um aplicativo que deve obter dados de mídia de um arquivo ou fonte de hardware deve saber tudo sobre o formato de dados e o dispositivo de hardware. O aplicativo deve lidar com a conexão, a transferência de dados, qualquer conversão de dados necessária e a renderização de dados real ou o armazenamento de arquivos. Como cada formato e dispositivo é ligeiramente diferente, esse processo geralmente é complexo e complicado. O streaming multimídia, por outro lado, negocia automaticamente a transferência e a conversão de dados da origem para o aplicativo. As interfaces de streaming fornecem um método uniforme e previsível de acesso e controle de dados, o que torna mais fácil para um aplicativo reproduzir os dados, independentemente de sua origem ou formato original.

As etapas a seguir mostram como implementar o streaming, do dispositivo de hardware à reprodução renderizada.

1.  Uma fonte de dados de vídeo, como DirectShow, expõe as interfaces de streaming.
2.  O desenvolvedor de aplicativos usa as interfaces de streaming multimídia para lidar com a conversão de formato de dados.
3.  O desenvolvedor de aplicativos usa as interfaces do DirectDraw para renderizar os dados resultantes.

A especificação para fluxos multimídia é composta por várias interfaces; cada interface inclui métodos que controlam um determinado aspecto do processo de streaming ou lidam com determinado tipo de dados. Consulte [Lista de interfaces de streaming multimídia](list-of-multimedia-streaming-interfaces.md) para obter informações adicionais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a arquitetura de streaming multimídia](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 




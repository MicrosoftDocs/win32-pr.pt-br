---
description: Vantagens do streaming de multimídia
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Vantagens do streaming de multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd907d9b8e91cb61709479a2d600323d6d420958
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091875"
---
# <a name="advantages-of-multimedia-streaming"></a>Vantagens do streaming de multimídia

> [!Note]  
> Essas APIs são preteridas. Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.

 

Quando os desenvolvedores usam o streaming de multimídia em seus aplicativos, reduz consideravelmente a quantidade de programação específica de formato necessária. Normalmente, um aplicativo que deve obter dados de mídia de uma fonte de arquivo ou de hardware deve saber tudo sobre o formato de dados e o dispositivo de hardware. O aplicativo deve lidar com a conexão, a transferência de dados, qualquer conversão de dados necessária e o armazenamento de arquivos ou processamento de dados real. Como cada formato e dispositivo é ligeiramente diferente, esse processo geralmente é complexo e complicado. O streaming de multimídia, por outro lado, negocia automaticamente a transferência e a conversão de dados da origem para o aplicativo. As interfaces de streaming fornecem um método uniforme e previsível de acesso e controle de dados, o que torna mais fácil para um aplicativo reproduzir os dados, independentemente de sua origem ou formato original.

As etapas a seguir mostram como implementar o streaming, do dispositivo de hardware para a reprodução renderizada.

1.  Uma fonte de dados de vídeo, como o DirectShow, expõe as interfaces de streaming.
2.  O desenvolvedor de aplicativos usa as interfaces de streaming de multimídia para manipular a conversão de formato de dados.
3.  O desenvolvedor do aplicativo usa as interfaces do DirectDraw para renderizar os dados resultantes.

A especificação para fluxos de multimídia abrange várias interfaces; cada interface inclui métodos que controlam um determinado aspecto do processo de streaming ou lidam com um determinado tipo de dados. Confira a [lista de interfaces de streaming de multimídia](list-of-multimedia-streaming-interfaces.md) para obter informações adicionais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a arquitetura de streaming de multimídia](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 




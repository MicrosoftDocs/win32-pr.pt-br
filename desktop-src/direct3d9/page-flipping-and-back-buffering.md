---
description: A inversão de página é a chave em multimídia, animação e software de jogos; é análogo à maneira como você pode fazer uma animação com um painel de papel.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Inversão de página e buffer de fundo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bffad581c5d4250c7f36980ba1f278a9f770912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105764207"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a>Inversão de página e buffer de fundo (Direct3D 9)

A inversão de página é a chave em multimídia, animação e software de jogos; é análogo à maneira como você pode fazer uma animação com um painel de papel. Em cada página, o artista altera a figura ligeiramente, de modo que, quando você virar rapidamente entre as planilhas, o desenho aparecerá animado.

A inversão de página no software é semelhante a esse processo. O Direct3D implementa a funcionalidade de inversão de página por meio de uma cadeia de permuta, que é uma propriedade do dispositivo. Inicialmente, você configura uma série de buffers do Direct3D que se alternam para a tela da forma como o papel do artista é invertido para a próxima página. O primeiro buffer é referido como o buffer frontal de cor. Os buffers por trás dele são chamados buffers de fundo. Seu aplicativo grava em um buffer de fundo e, em seguida, inverte o buffer frontal de cor para que o buffer de fundo apareça na tela. Enquanto o sistema exibe a imagem, seu software está gravando novamente em um buffer de fundo. O processo continuará desde que você esteja animando, permitindo que você anime imagens com eficiência.

O Direct3D facilita a configuração de esquemas de inversão de página – a partir de um esquema simples de buffer duplo (um buffer frontal de cor com um buffer de fundo) para esquemas mais sofisticados com buffers de fundo adicionais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies de Direct3D](direct3d-surfaces.md)
</dt> <dt>

[O que é uma cadeia de permuta? (Direct3D 9)](what-is-a-swap-chain-.md)
</dt> </dl>

 

 




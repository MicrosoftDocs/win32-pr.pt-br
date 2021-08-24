---
description: A invertia de página é a chave em multimídia, animação e software de jogo; é análogo à maneira como você pode fazer animação com um bloco de papel.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Invertir e voltar ao buffer de página (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134f1797300a838e453abf6811ae35b8f576e46c89ca0e929d2326b43ffea274
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746926"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a>Invertir e voltar ao buffer de página (Direct3D 9)

A invertia de página é a chave em multimídia, animação e software de jogo; é análogo à maneira como você pode fazer animação com um bloco de papel. Em cada página, o artista altera ligeiramente a figura, de modo que, quando você inverte rapidamente entre planilhas, o desenho é exibido animado.

A invertia de página no software é semelhante a esse processo. O Direct3D implementa a funcionalidade de invertir página por meio de uma cadeia de permuta, que é uma propriedade do dispositivo. Inicialmente, você configura uma série de buffers Direct3D que se invertem para a tela da maneira que o papel do artista muda para a próxima página. O primeiro buffer é conhecido como buffer frontal de cor. Os buffers por trás dele são chamados de buffers de fundo. Seu aplicativo grava em um buffer de fundo e, em seguida, inverte o buffer frontal de cor para que o buffer de fundo apareça na tela. Enquanto o sistema exibe a imagem, seu software está escrevendo novamente em um buffer de fundo. O processo continua enquanto você está animando, permitindo animar imagens com eficiência.

O Direct3D facilita a configuração de esquemas de invertida de página – de um esquema simples em buffer duplo (um buffer frontal de cor com um buffer de fundo) a esquemas mais sofisticados com buffers de fundo adicionais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies Direct3D](direct3d-surfaces.md)
</dt> <dt>

[O que é uma cadeia de permuta? (Direct3D 9)](what-is-a-swap-chain-.md)
</dt> </dl>

 

 




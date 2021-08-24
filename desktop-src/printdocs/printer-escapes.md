---
description: os escapes de impressora fornecidos por Windows de 16 bits permitiram acesso a recursos especiais do dispositivo.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Escapes de impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd8bc842e60ca0019fc523b27a4657e66a623cda4802bfdb489213b694fd432
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711556"
---
# <a name="printer-escapes"></a>Escapes de impressora

os escapes de impressora fornecidos por Windows de 16 bits permitiram acesso a recursos especiais do dispositivo. a maioria desses escapes é obsoleta, mas alguns são fornecidos para simplificar a portabilidade de aplicativos baseados em Windows de 16 bits. O GDI dá suporte a um conjunto completo de funções de caminho que os aplicativos podem usar em vez dos escapes para desenhar caminhos em qualquer dispositivo. Para obter uma lista de funções que substituem alguns dos escapes, consulte a função [**escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) .

Dos escapes de impressora originais do 64, somente **QUERYESCSUPPORT** e **PassThrough** podem ser usados.

Há também uma função de escape estendida chamada [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Essa função permite que os aplicativos acessem os recursos de um determinado dispositivo que não está diretamente disponível por meio do GDI.

 

 




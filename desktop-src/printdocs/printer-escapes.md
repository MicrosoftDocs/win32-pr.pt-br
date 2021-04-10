---
description: Os escapes de impressora fornecidos pelo Windows de 16 bits permitiam acesso a recursos especiais do dispositivo.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Escapes de impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170119"
---
# <a name="printer-escapes"></a>Escapes de impressora

Os escapes de impressora fornecidos pelo Windows de 16 bits permitiam acesso a recursos especiais do dispositivo. A maioria desses escapes é obsoleta, mas alguns são fornecidos para simplificar a portabilidade de aplicativos baseados no Windows de 16 bits. O GDI dá suporte a um conjunto completo de funções de caminho que os aplicativos podem usar em vez dos escapes para desenhar caminhos em qualquer dispositivo. Para obter uma lista de funções que substituem alguns dos escapes, consulte a função [**escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) .

Dos escapes de impressora originais do 64, somente **QUERYESCSUPPORT** e **PassThrough** podem ser usados.

Há também uma função de escape estendida chamada [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Essa função permite que os aplicativos acessem os recursos de um determinado dispositivo que não está diretamente disponível por meio do GDI.

 

 




---
description: Explica os meios pelos quais um aplicativo ou provedor de serviços pode se conectar a um cartão inteligente usando o subsistema de cartão inteligente.
ms.assetid: 27f8f25f-1883-4070-94a4-0d3c51032378
title: Acessando um cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ae7a7954d9a48191884c8ed0fd7ee65ad3bb007aae18b00efc6581e5f2e6221
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101466"
---
# <a name="accessing-a-smart-card"></a>Acessando um cartão inteligente

O [*subsistema de*](/windows/desktop/SecGloss/s-gly) cartão inteligente fornece vários meios para um aplicativo ou provedor [*de serviços*](/windows/desktop/SecGloss/c-gly) se conectar a um cartão inteligente:

-   Um aplicativo pode chamar [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) para se conectar a um cartão que reside em um determinado leitor. Essa é a maneira mais simples de estabelecer a comunicação com um cartão inteligente.
-   Um aplicativo pode pesquisar um cartão inteligente específico dentro de um determinado grupo de leitores. O aplicativo identifica o cartão pelo nome de exibição e especifica uma lista de leitores na qual o cartão pode aparecer. O [*gerenciador de recursos*](/windows/desktop/SecGloss/r-gly) pesquisa na lista de leitores todos os cartões com uma cadeia de caracteres [*ATR*](/windows/desktop/SecGloss/a-gly) que corresponde ao cartão nomeado e retorna informações de status para o aplicativo. O [*subsistema de cartão inteligente*](/windows/desktop/SecGloss/s-gly) nunca coloca uma GUI ou interage com o cartão além de obter a cadeia de caracteres atr. No entanto, ele fornece informações suficientes para o aplicativo ou um controle comum para ser capaz de ajudar o usuário a localizar o tipo de cartão ou cartão desejado. Isso resulta no mapeamento da solicitação para um leitor específico, para o qual a E/S posterior é direcionada.
-   Um aplicativo pode solicitar uma lista de cartões que suportam um determinado conjunto de interfaces de cartão inteligente. O aplicativo pode usar a lista no caso anterior. Isso permite que os aplicativos se conectem a cartões com base em suas funcionalidades, sem considerar seus nomes.

Quando um aplicativo procura um cartão, ele fornece uma matriz de nomes de leitor no qual procurar. Para cada elemento de leitor na matriz, o gerenciador de recursos fornece as seguintes informações:

-   Se o leitor está disponível para uso por este aplicativo.
-   Se há um cartão inserido nesse leitor e, nesse caso, qual é sua cadeia de caracteres ATR.
-   Se a cadeia de caracteres ATR do cartão corresponde a qualquer uma das cadeias de caracteres ATR dos cartões solicitados.

O aplicativo usa as informações retornadas para aplicar mais filtros aos cartões ou para solicitar que o usuário selecione o cartão desejado. Observe que um ou mais da lista retornada de leitores pode ser aberta para uso exclusivo por outros aplicativos, portanto, o acesso a essa lista de leitores não é garantido.

 

 

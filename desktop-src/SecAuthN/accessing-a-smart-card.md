---
description: Explica o meio pelo qual um aplicativo ou provedor de serviços pode se conectar a um cartão inteligente usando o subsistema de cartão inteligente.
ms.assetid: 27f8f25f-1883-4070-94a4-0d3c51032378
title: Acessando um cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b155d467c9de28b1e02dea01511ea1e71d574eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748962"
---
# <a name="accessing-a-smart-card"></a>Acessando um cartão inteligente

O subsistema de [*cartão inteligente*](/windows/desktop/SecGloss/s-gly) fornece vários meios para que um aplicativo ou [*provedor de serviços*](/windows/desktop/SecGloss/c-gly) se conecte a um cartão inteligente:

-   Um aplicativo pode chamar [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) para se conectar a um cartão que reside em um determinado leitor. Essa é a maneira mais simples de estabelecer a comunicação com um cartão inteligente.
-   Um aplicativo pode pesquisar um cartão inteligente específico em um determinado grupo de leitores. O aplicativo identifica o cartão pelo seu nome de exibição e especifica uma lista de leitores na qual o cartão pode aparecer. O [*Gerenciador de recursos*](/windows/desktop/SecGloss/r-gly) pesquisa a lista de leitores de qualquer cartão com uma [*cadeia de caracteres ATR*](/windows/desktop/SecGloss/a-gly) que corresponda ao cartão nomeado e retorna informações de status para o aplicativo. O [*subsistema de cartão inteligente*](/windows/desktop/SecGloss/s-gly) nunca coloca uma GUI ou interage com o cartão além de obter a cadeia de caracteres ATR. No entanto, ele fornece informações suficientes para que o aplicativo ou um controle comum possa orientar o usuário localizando o cartão desejado ou o tipo de cartão. Isso resulta no mapeamento da solicitação para um leitor específico, ao qual e/s adicional é direcionada.
-   Um aplicativo pode solicitar uma lista de cartões que dão suporte a um determinado conjunto de interfaces de cartão inteligente. O aplicativo pode usar a lista no caso anterior. Isso permite que os aplicativos se conectem a cartões com base em seus recursos, sem considerar seus nomes.

Quando um aplicativo procura um cartão, ele fornece uma matriz de nomes de leitores a serem examinados. Para cada elemento de leitor na matriz, o Gerenciador de recursos fornece as seguintes informações:

-   Se o leitor está disponível para uso por este aplicativo.
-   Se há um cartão inserido nesse leitor e, em caso afirmativo, qual é sua cadeia de caracteres ATR.
-   Se a cadeia de caracteres ATR do cartão corresponde a qualquer uma das cadeias ATR das placas solicitadas.

O aplicativo usa as informações retornadas para aplicar filtros adicionais aos cartões ou para solicitar que o usuário selecione o cartão desejado. Observe que uma ou mais das listas de leitores retornadas podem ser abertas para uso exclusivo por outros aplicativos, portanto, o acesso a essa lista de leitores não é garantido.

 

 

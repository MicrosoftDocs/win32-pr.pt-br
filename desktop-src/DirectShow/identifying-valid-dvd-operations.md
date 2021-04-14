---
description: Identificando operações de DVD válidas
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identificando operações de DVD válidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370275"
---
# <a name="identifying-valid-dvd-operations"></a>Identificando operações de DVD válidas

Vários fatores determinam se você pode executar uma determinada operação de DVD:

-   O domínio atual. Alguns comandos são válidos somente em determinados domínios. Quando o domínio é alterado, o navegador envia um \_ evento de alteração de domínio de DVD do EC \_ \_ . Você também pode chamar [**IDvdInfo2:: GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) para obter o domínio atual.
-   Sinalizadores UOPS. Esses são sinalizadores gravados no disco que indicam quais operações são permitidas. Sempre que os sinalizadores são alterados, o navegador envia \_ um \_ evento de alteração UOPS válido de DVD do EC \_ \_ com os novos sinalizadores. Você também pode chamar [**IDvdInfo2:: GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) para obter os sinalizadores UOPS atuais.
-   Conteúdo do DVD. Alguns comandos podem não ser relevantes com base no conteúdo do DVD. Por exemplo, o método [**IDvdControl2:: SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) pode ser permitido de acordo com os sinalizadores de domínio e UOPS atuais, mas o vídeo pode ter apenas um ângulo. Nesse caso, a chamada **SelectAngle** é permitida, mas não é uma opção significativa.

Em caso de dúvida, permita uma ação. No pior, o método [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) falhará e você poderá fornecer comentários ao usuário. Os comentários devem ser relativamente discretos. Por exemplo, você pode piscar um pequeno X vermelho para alertar o usuário. O navegador de DVD retorna VFW \_ e \_ DVD \_ INVALIDDOMAIN quando o domínio proíbe uma operação e \_ \_ a operação de VFW e DVD é \_ \_ inibida quando os sinalizadores de UOPS proíbem uma operação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 




---
description: Um aplicativo preenche o interior de uma região chamando a função FillRgn e fornecendo um identificador que identifica um pincel específico.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Preenchendo regiões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62709869f5f25a6cde11812844efdab6162b1e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010728"
---
# <a name="filling-regions"></a>Preenchendo regiões

Um aplicativo preenche o interior de uma região chamando a função [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) e fornecendo um identificador que identifica um pincel específico. Quando um aplicativo chama FillRgn, o sistema preenche a região com o pincel usando o modo de preenchimento atual para o contexto do dispositivo especificado. Há dois modos de preenchimento: alternativo e enrolamento. O aplicativo pode definir o modo de preenchimento para um contexto de dispositivo chamando a função [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) . O aplicativo pode recuperar o modo de preenchimento atual para um contexto de dispositivo chamando a função [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) .

A ilustração a seguir mostra duas regiões idênticas: uma preenchida usando o modo alternativo e outra preenchida usando o modo de enrolamento.

![ilustração mostrando estrelas 2 5-pontas: uma preenchida apenas nos pontos, a outra preenchida completamente](images/csrgn-03.png)

## <a name="alternate-mode"></a>Modo alternativo

Para determinar quais pixels o sistema realça quando o modo alternativo é especificado, execute o seguinte teste:

1.  Selecione um pixel dentro do interior da região.
2.  Desenhe um raio de imaginário, na direção x positiva, desse pixel em direção ao infinito.
3.  Cada vez que Ray intercepta uma linha de limite, incrementa um valor de contagem.

O sistema realça o pixel se o valor da contagem for um número ímpar.

## <a name="winding-mode"></a>Modo de enrolamento

Para determinar quais pixels o sistema realça quando o modo de enrolamento é especificado, execute o seguinte teste:

1.  Determine a direção na qual cada linha de limite é desenhada.
2.  Selecione um pixel dentro do interior da região.
3.  Desenhe um raio de imaginário, na direção x positiva, do pixel em direção ao infinito.
4.  Cada vez que Ray intercepta uma linha de limite com um componente y positivo, incrementa um valor de contagem. Cada vez que Ray intercepta uma linha de limite com um componente y negativo, Decrementa o valor da contagem.

O sistema realça o pixel se o valor da contagem for diferente de zero.

 

 




---
description: Processando dados
ms.assetid: 823615df-ce50-4e20-957a-f83d3be66658
title: Processando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff417b3e37c3be43c42fd0cf8545bce6bfb00caa361d34d8044d690169f7c97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748166"
---
# <a name="processing-data"></a>Processando dados

**Analisando dados de mídia**

Se o filtro analisar os dados de mídia, não confie nos cabeçalhos ou outros dados autodescritivos no conteúdo. Por exemplo, não confie nos valores de tamanho que aparecem nas partes do AVI RIFF ou nos pacotes MPEG. Exemplos comuns desse tipo de erro incluem:

-   Leitura de *N* bytes de dados, em que o valor de *N* veio do conteúdo, sem verificar *N* em relação ao tamanho real do buffer.
-   Saltar para um deslocamento de byte dentro de um buffer, sem verificar se o deslocamento está dentro do buffer.

Outra classe comum de erros envolve não validar descrições de formato encontradas no conteúdo. Por exemplo:

-   Uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) pode ser seguida por uma tabela de cores. A estrutura **BITMAPINFO** é definida como uma estrutura **BITMAPINFOHEADER** seguida por uma matriz de valores **RGBQUAD** que compõem a tabela de cores. O tamanho da matriz é determinado pelo valor de **biClrUsed**. Nunca Copie uma tabela de cores em um **BITMAPINFO** sem primeiro verificar o tamanho do buffer que foi alocado para a estrutura **BITMAPINFO** .
-   Uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) pode ter informações de formato extras acrescentadas à estrutura. O membro **cbSize** especifica o tamanho das informações adicionais.

Durante a conexão do PIN, um filtro deve verificar se todas as estruturas de formato estão bem formadas e contêm valores razoáveis. Caso contrário, rejeite a conexão. No código que valida a estrutura de formato, seja especialmente cuidadoso com o estouro aritmético. Por exemplo, em um **BITMAPINFOHEADER**, a largura e a altura são valores **longos** de 32 bits, mas o tamanho da imagem (que é uma função do produto dos dois) é apenas um valor **DWORD** .

Se os dados de formato da origem forem maiores do que o buffer alocado, não truncará os dados de origem para copiá-los para o buffer. Isso pode criar uma estrutura cujo tamanho implícito seja maior do que seu tamanho real. Por exemplo, um cabeçalho de bitmap pode especificar uma tabela de paleta que não existe mais. Em vez disso, realoque o buffer ou simplesmente falhe a conexão.

**Erros durante o streaming**

Quando o grafo estiver em execução, se o filtro receber conteúdo malformado, ele deverá terminar o streaming. Faça o seguinte:

-   Retornar um código de erro de **Receive**.
-   Chame [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no filtro downstream.
-   Chame [**CBaseFilter:: NotifyEvent**](cbasefilter-notifyevent.md) para postar um evento de [**\_ ERRORABORT do EC**](ec-errorabort.md) .

**Alterações de formato**

Existem vários mecanismos para filtros para alterar os formatos de meio fluxo. Cada um deles envolve mais de uma etapa, o que cria o potencial para falsas aceitação. Se o filtro receber uma solicitação de alteração de formato dinâmico, ele deverá rejeitar a solicitação ou aceitar o novo formato quando chegar. Da mesma forma, nunca mude os formatos, a menos que o outro filtro concorde. Para obter mais informações, consulte [Dynamic Format Changes](dynamic-format-changes.md).

 

 

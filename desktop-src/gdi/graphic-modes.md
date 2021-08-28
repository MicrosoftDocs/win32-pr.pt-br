---
description: o Windows dá suporte a cinco modos gráficos que permitem que um aplicativo especifique como as cores são misturadas, onde a saída aparece, como a saída é dimensionada e assim por diante. Esses modos, que são armazenados em um controlador de domínio, são descritos na tabela a seguir.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Modos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c36461935c8279e38e09afe9f7802e2f758d1cf45380beaa16d1911f4ed965f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558766"
---
# <a name="graphic-modes"></a>Modos gráficos

o Windows dá suporte a cinco modos gráficos que permitem que um aplicativo especifique como as cores são misturadas, onde a saída aparece, como a saída é dimensionada e assim por diante. Esses modos, que são armazenados em um controlador de domínio, são descritos na tabela a seguir.



| Modo gráfico | Descrição                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| Segundo plano    | Define como as cores do plano de fundo são misturadas com as cores existentes da janela ou da tela para operações de bitmap e texto.              |
| Desenho       | Define como as cores de primeiro plano são misturadas com as cores existentes da janela ou da tela para as operações de caneta, pincel, bitmap e texto. |
| Mapeamento       | Define como a saída de gráficos é mapeada do espaço lógico (ou do mundo) na janela, na tela ou no papel da impressora.             |
| Polígono – preenchimento  | Define como o padrão de pincel é usado para preencher o interior de regiões complexas.                                             |
| Tira    | Define como as cores de bitmap são misturadas com as cores existentes da janela ou da tela quando o bitmap é compactado (ou reduzido).  |



 

Como acontece com objetos gráficos, o sistema inicializa um controlador de domínio com modos gráficos padrão. Um aplicativo pode recuperar e examinar esses modos padrão chamando as funções a seguir.



| Modo gráfico | Função                                       |
|---------------|------------------------------------------------|
| Segundo plano    | [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| Desenho       | [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| Mapeamento       | [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| Polígono – preenchimento  | [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| Tira    | [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

Um aplicativo pode alterar os modos padrão chamando uma das funções a seguir.



| Modo gráfico | Função                                       |
|---------------|------------------------------------------------|
| Segundo plano    | [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| Desenho       | [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| Mapeamento       | [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| Polígono – preenchimento  | [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| Tira    | [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 




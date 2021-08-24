---
description: Fontes de informações de região de DVD
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Fontes de informações de região de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729dc02d07b927dd2bb7938ba87c6435df04459ad3ebd1976ede808bd292552e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904086"
---
# <a name="sources-of-dvd-region-information"></a>Fontes de informações de região de DVD

Há três fontes de informações de região de DVD que funcionam em conjunto para determinar a região para reprodução de DVD em um Windows PC.

-   Título do DVD. A maioria dos títulos de DVD é marcada para uma região específica. Alguns títulos podem ser interpretados em apenas uma região, alguns podem ser interpretados em várias regiões e outros podem ser tocadas em todas as regiões. As regiões de 1 a 6 foram definidas na especificação de DVD-Video original. A região 7 está indefinida no momento. A Região 8 foi adicionada em 1999 para locais especiais, como avião. Os discos DVD-ROM (aqueles sem zona de vídeo) não devem conter nenhuma codificação de região.
-   Unidade DVD-ROM. Há dois tipos de unidades dvd-ROM: unidades RPC Fase 1 (RPC1) e unidades RPC Fase 2 (RPC2). As unidades RPC1 não têm suporte de hardware integrado para gerenciamento de região. Para essas unidades, Windows mantém as informações de contagem de alterações de região e a região pode ser alterada apenas uma vez. As unidades RPC2 mantêm as informações de contagem de alterações de região no hardware e, em geral, a região dessas unidades pode ser alterada até cinco vezes.
-   Decodificador de DVD. Alguns decodificadores de DVD, hardware ou software são definidos para uma região específica. Em geral, o usuário não pode alterar a região do decodificador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte para alteração de região de DVD Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 




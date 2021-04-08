---
description: Fontes de informações de região do DVD
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Fontes de informações de região do DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac426f995323bfd30d3430dccb4044c5f71a119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922150"
---
# <a name="sources-of-dvd-region-information"></a>Fontes de informações de região do DVD

Há três fontes de informações de região de DVD que funcionam em conjunto para determinar a região de reprodução de DVD em um computador Windows.

-   Título do DVD. A maioria dos títulos de DVD são marcados para uma região específica. Alguns títulos podem ser reproduzidos em apenas uma região, alguns podem ser reproduzidos em várias regiões e outros podem ser executados em todas as regiões. As regiões de 1 a 6 foram definidas na especificação de DVD-Video original. A região 7 não está definida no momento. A região 8 foi adicionada em 1999 para locais especiais, como aviões. Os discos de DVD-ROM (aqueles sem nenhuma zona de vídeo) não devem conter nenhuma codificação de região.
-   Unidade de DVD-ROM. Há dois tipos de unidades de DVD-ROM: unidades de RPC1 (RPC Phase 1) e unidades de RPC Phase 2 (RPC2). As unidades RPC1 não têm suporte interno de hardware para gerenciamento de região. Para essas unidades, o Windows mantém as informações de contagem de alteração de região e a região pode ser alterada apenas uma vez. As unidades RPC2 mantêm as informações de contagem de alteração de região em hardware e, em geral, a região dessas unidades pode ser alterada até 5 vezes.
-   Decodificador de DVD. Alguns decodificadores de DVD, hardware ou software são definidos para uma região específica. Em geral, o usuário não pode alterar a região do decodificador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte à alteração da região do DVD no Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 




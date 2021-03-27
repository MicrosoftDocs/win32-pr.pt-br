---
description: O exemplo em pincéis usa regiões para simular um &\# 0034; com zoom&\# 0034; exibição de um bitmap monocromático de 8 e 8 pixels.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Usando regiões para executar testes de clique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb50ca1f837213b85619af381b86c2bd76efcbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169135"
---
# <a name="using-regions-to-perform-hit-testing"></a>Usando regiões para executar testes de clique

O exemplo em [pincéis](brushes.md) usa regiões para simular uma exibição "ampliada" de um bitmap monocromático de 8 e 8 pixels. Ao clicar nos pixels neste bitmap, o usuário cria um pincel personalizado adequado para operações de desenho. O exemplo mostra como usar a função [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) para executar testes de clique e a função [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) para inverter as cores em uma região.

 

 




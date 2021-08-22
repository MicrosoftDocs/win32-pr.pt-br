---
description: O exemplo em Pincéis usa regiões para simular um &\# 0034;zoom&0034; exibição de um bitmap monocromático de 8 por \# 8 pixels.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Usando regiões para executar testes de acerto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d553eeaf37b954d0ec9d0b8897df98cf1a513d7ca7212ca82bc376afe1fc7163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558116"
---
# <a name="using-regions-to-perform-hit-testing"></a>Usando regiões para executar testes de acerto

O exemplo em [Pincéis](brushes.md) usa regiões para simular uma exibição "ampliada" de um bitmap monocromático de 8 por 8 pixels. Clicando nos pixels neste bitmap, o usuário cria um pincel personalizado adequado para operações de desenho. O exemplo mostra como usar a [**função PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) para executar testes de acerto e a [**função InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) para inverter as cores em uma região.

 

 




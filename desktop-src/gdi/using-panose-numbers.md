---
description: Os arquivos de fonte TrueType incluem números de PANOse, que os aplicativos podem usar para escolher uma fonte que corresponda de acordo com suas especificações.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Usando números de PANOse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a974a0d1e708cac931e06e386e2df0802cbea79e5c9d499ca460d6deb5b0bab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037454"
---
# <a name="using-panose-numbers"></a>Usando números de PANOse

Os arquivos de fonte TrueType incluem números de PANOse, que os aplicativos podem usar para escolher uma fonte que corresponda de acordo com suas especificações. O sistema PANOse classifica faces por 10 atributos diferentes. Para obter mais informações sobre esses atributos, consulte [**Panose**](/windows/win32/api/wingdi/ns-wingdi-panose). Uma estrutura **Panose** faz parte da estrutura [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (cujos valores são preenchidos chamando a função [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) ).

Os atributos PANOse são classificados individualmente em uma escala. Os valores resultantes são concatenados para produzir um número. Considerando esse número para uma fonte e uma métrica matemática para medir as distâncias no espaço PANOse, um aplicativo pode determinar os vizinhos mais próximos.

 

 




---
description: Um aplicativo cria uma região chamando uma função associada a uma forma específica. A tabela a seguir mostra as funções associadas a cada uma das formas padrão.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Criação e seleção de região
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ce2711b2d1ae9dc6641748c72fd586d02e25964102a8c034593d6e60cbaa33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092686"
---
# <a name="region-creation-and-selection"></a>Criação e seleção de região

Um aplicativo cria uma região chamando uma função associada a uma forma específica. A tabela a seguir mostra as funções associadas a cada uma das formas padrão.



| Forma                                   | Função                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Região retangular                      | [**CreateRectRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn) [**CreateRectRgnIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect) [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn) |
| Região retangular com cantos arredondados | [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| Região elíptica                       | [**CreateEllipticRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn) [ **CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)                   |
| Região poligonal                        | [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)                               |



 

Cada função de criação de região retorna um identificador que identifica a nova região. Um aplicativo pode usar esse handle para selecionar a região em um contexto de dispositivo chamando a [**função SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) e fornecendo esse handle como o segundo argumento. Depois que uma região é selecionada em um contexto de dispositivo, o aplicativo pode executar várias operações nele.

 

 




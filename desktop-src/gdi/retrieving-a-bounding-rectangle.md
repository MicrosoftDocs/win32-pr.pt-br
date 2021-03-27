---
description: Um aplicativo recupera as dimensões do retângulo delimitador de uma região chamando a função GetRgnBox.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Recuperando um retângulo delimitador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b214a3f2e8d4fcd81e7f03ecf6dddc72442e209b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661583"
---
# <a name="retrieving-a-bounding-rectangle"></a>Recuperando um retângulo delimitador

Um aplicativo recupera as dimensões do retângulo delimitador de uma região chamando a função [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) . Se a região for retangular, **GetRgnBox** retornará as dimensões da região. Se a região for elíptica, a função retornará as dimensões do menor retângulo que pode ser desenhada ao redor da elipse. Os lados longos do retângulo têm o mesmo comprimento que o eixo principal da elipse, e os lados curtos do retângulo têm o mesmo comprimento que o eixo secundário da elipse. Se a região for Polygon, **GetRgnBox** retornará as dimensões do menor retângulo que pode ser desenhado em todo o polígono.

 

 




---
description: Um aplicativo recupera as dimensões do retângulo delimitador de uma região chamando a função GetRgnBox.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Recuperando um retângulo delimitador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b7182d7c8f48fa8629855849710a601db9f93fd7e9180f9024d798b5ce2ebe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886138"
---
# <a name="retrieving-a-bounding-rectangle"></a>Recuperando um retângulo delimitador

Um aplicativo recupera as dimensões do retângulo delimitador de uma região chamando a função [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) . Se a região for retangular, **GetRgnBox** retornará as dimensões da região. Se a região for elíptica, a função retornará as dimensões do menor retângulo que pode ser desenhada ao redor da elipse. Os lados longos do retângulo têm o mesmo comprimento que o eixo principal da elipse, e os lados curtos do retângulo têm o mesmo comprimento que o eixo secundário da elipse. Se a região for Polygon, **GetRgnBox** retornará as dimensões do menor retângulo que pode ser desenhado em todo o polígono.

 

 




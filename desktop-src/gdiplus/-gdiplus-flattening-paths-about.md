---
description: Um objeto GraphicsPath armazena uma sequência de linhas e B&\# 233; ziers.
ms.assetid: 8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8
title: Nivelamento de caminhos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caee9b8d760d9702b6a3ea7711090f001a57912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987962"
---
# <a name="flattening-paths"></a>Nivelamento de caminhos

Um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) armazena uma sequência de linhas e uma linhagem de Bézier. Você pode adicionar vários tipos de curvas (elipses, arcos, splines Cardeal) a um caminho, mas cada curva é convertida em uma spline Bézier antes de ser armazenada no caminho. O nivelamento de um caminho consiste na conversão de cada spline de Bézier no caminho para uma sequência de linhas retas.

Para mesclar um caminho, chame o método [**GraphicsPath:: achata**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) de um objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) . O método **GraphicsPath:: achatado** recebe um argumento Flatness que especifica a distância máxima entre o caminho nivelado e o caminho original. A ilustração a seguir mostra um caminho antes e depois do nivelamento.

![ilustração mostrando uma sequência de polilinhas de Bézier conectadas em azul e as linhas correspondentes em vermelho](images/aboutgdip02-art32a.png)

 

 




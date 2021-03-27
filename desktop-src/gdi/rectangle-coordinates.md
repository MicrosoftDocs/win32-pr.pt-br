---
description: Um aplicativo deve usar uma estrutura RECT para definir um retângulo.
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: Coordenadas de retângulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8a3fbc3f42c6d69a3d0eac6555b85fbfc1eecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988788"
---
# <a name="rectangle-coordinates"></a>Coordenadas de retângulo

Um aplicativo deve usar uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para definir um retângulo. A estrutura especifica as coordenadas de dois pontos: os cantos superior esquerdo e inferior direito do retângulo. Os lados do retângulo se estendem desses dois pontos e são paralelos aos eixos x e y.

Os valores de coordenadas para um retângulo são expressos como inteiros assinados. O valor da coordenada do lado direito de um retângulo deve ser maior do que o do lado esquerdo. Da mesma forma, o valor da coordenada da parte inferior deve ser maior que o da parte superior.

Como os aplicativos podem usar retângulos para muitas finalidades diferentes, as funções de retângulo não usam uma unidade de medida explícita. Em vez disso, todas as coordenadas e dimensões de retângulo são dadas em valores lógicos assinados. O modo de mapeamento e a função na qual o retângulo é usado determinam as unidades de medida. Para obter mais informações sobre os modos de coordenadas e de mapeamento, consulte [espaços de coordenadas e transformações](coordinate-spaces-and-transformations.md).

 

 

---
title: Gerando coordenadas de textura
description: Em vez de fornecer explicitamente coordenadas de textura, você pode fazer com que o OpenGL as gere como uma função de outros dados de vértice usando glTexGen\ .
ms.assetid: 5c9ce163-6107-46a3-8c8d-fc87d2f8cf9a
keywords:
- Pipeline de processamento openGL, coordenadas de textura
- coordenadas de textura OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e7b6bc2d1263fac046f2d3078e2bab9bf8a789cacb335137ba27443b12b89d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082276"
---
# <a name="generating-texture-coordinates"></a>Gerando coordenadas de textura

Em vez de fornecer explicitamente coordenadas de textura, você pode fazer com que o OpenGL as gere como uma função de outros dados de vértice usando [glTexGen. \* ](gltexgen-functions.md) Depois que as coordenadas de textura foram especificadas ou geradas, elas são transformadas pela matriz de textura. Essa matriz é controlada com as mesmas funções usadas para transformações de matriz (consulte [Transformações de matriz](matrix-transformations.md)).

 

 





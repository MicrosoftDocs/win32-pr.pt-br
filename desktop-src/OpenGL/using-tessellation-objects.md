---
title: Usando objetos de mosaico
description: Como um polígono complexo está sendo descrito e mosaico, ele requer dados associados, como os vértices, as bordas e as funções de retorno de chamada.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- Utilitário OpenGL (GLU), objetos de mosaico
- GLU (utilitário OpenGL), objetos de mosaico
- objetos de mosaico OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291988"
---
# <a name="using-tessellation-objects"></a>Usando objetos de mosaico

Como um polígono complexo está sendo descrito e mosaico, ele requer dados associados, como os vértices, as bordas e as funções de retorno de chamada. Todos esses dados estão vinculados a um único objeto de mosaico. Para incluí um polígono, primeiro você usa a função [**gluNewTess**](glunewtess.md) , que cria um novo objeto de mosaico e retorna um ponteiro para ele. Um ponteiro nulo será retornado se a função falhar.

Se você não precisar mais de um objeto de mosaico, poderá excluí-lo e liberar toda a memória associada com [**gluDeleteTess**](gludeletetess.md).

Você pode reutilizar um único objeto de mosaico para todos os seus mosaicos. Esse objeto é necessário apenas porque as funções de biblioteca podem precisar fazer seus próprios mosaicos, e eles devem ser capazes de fazer isso sem interferir em qualquer mosaico que seu programa esteja executando. Vários objetos de mosaico também são úteis se você quiser usar diferentes conjuntos de retornos de chamada para diferentes mosaicos. Normalmente, no entanto, você aloca um único objeto de mosaico e o utiliza para todos os mosaicos. Não há necessidade real de liberá-lo, pois ele usa uma pequena quantidade de memória. Por outro lado, se você estiver escrevendo uma função de biblioteca que usa o mosaico GLU, tenha cuidado para liberar todos os objetos de mosaico que criar.

 

 





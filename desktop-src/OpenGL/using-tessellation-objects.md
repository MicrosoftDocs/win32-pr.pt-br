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
ms.openlocfilehash: efc2ca11fd037f79a88fed1568c97a24692060d723327cde0c8e8842ed21d084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011894"
---
# <a name="using-tessellation-objects"></a>Usando objetos de mosaico

Como um polígono complexo está sendo descrito e mosaico, ele requer dados associados, como os vértices, as bordas e as funções de retorno de chamada. Todos esses dados estão vinculados a um único objeto de mosaico. Para incluí um polígono, primeiro você usa a função [**gluNewTess**](glunewtess.md) , que cria um novo objeto de mosaico e retorna um ponteiro para ele. Um ponteiro nulo será retornado se a função falhar.

Se você não precisar mais de um objeto de mosaico, poderá excluí-lo e liberar toda a memória associada com [**gluDeleteTess**](gludeletetess.md).

Você pode reutilizar um único objeto de mosaico para todos os seus mosaicos. Esse objeto é necessário apenas porque as funções de biblioteca podem precisar fazer seus próprios mosaicos, e eles devem ser capazes de fazer isso sem interferir em qualquer mosaico que seu programa esteja executando. Vários objetos de mosaico também são úteis se você quiser usar diferentes conjuntos de retornos de chamada para diferentes mosaicos. Normalmente, no entanto, você aloca um único objeto de mosaico e o utiliza para todos os mosaicos. Não há necessidade real de liberá-lo, pois ele usa uma pequena quantidade de memória. Por outro lado, se você estiver escrevendo uma função de biblioteca que usa o mosaico GLU, tenha cuidado para liberar todos os objetos de mosaico que criar.

 

 





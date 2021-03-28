---
description: Um aplicativo pode desenhar o contorno de um caminho chamando a função StrokePath, ele pode preencher o interior de um caminho chamando a função FillPath e pode contornar e preencher o caminho chamando a função StrokeAndFillPath.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Caminhos de contorno e preenchidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735ee9ee5d7e69922241c5647b883e1800b525e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921287"
---
# <a name="outlined-and-filled-paths"></a>Caminhos de contorno e preenchidos

Um aplicativo pode desenhar o contorno de um caminho chamando a função [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) , ele pode preencher o interior de um caminho chamando a função [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) e pode contornar e preencher o caminho chamando a função [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) .

Sempre que um aplicativo preenche um caminho, o sistema usa o modo de preenchimento atual do DC. Um aplicativo pode recuperar esse modo chamando a função [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) e pode definir um novo modo de preenchimento chamando a função [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) . Para obter uma descrição dos dois modos de preenchimento, consulte [regiões](regions.md).

A ilustração a seguir mostra a seção cruzada de um objeto criado por um aplicativo CAD (design auxiliado por computador) usando caminhos que foram contornados e preenchidos.

![ilustração mostrando a exibição de seções cruzadas de um objeto, com várias partes indicadas por padrões de preenchimento diferentes](images/cspth-01.png)

 

 




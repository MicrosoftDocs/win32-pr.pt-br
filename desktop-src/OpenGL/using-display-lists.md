---
title: Usando listas de exibição
description: Usando listas de exibição
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, listas de exibição
- listas de exibição OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322721868f3bf994382a7604aa2cb76802f268aec7a1298aaa14e3066d5f6cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932796"
---
# <a name="using-display-lists"></a>Usando listas de exibição

Uma lista de exibição é um grupo de funções OpenGL que foi armazenado para execução subsequente. A [**função glNewList**](glnewlist.md) inicia a criação de uma lista de exibição e [**glEndList**](glendlist.md) a encerra. Com poucas exceções, as funções OpenGL chamadas entre **glNewList** e **glEndList** são anexadas à lista de exibição. (Consulte **glNewList** para ver uma lista das funções que você não pode armazenar e executar de dentro de uma lista de exibição.) Para disparar a execução de uma lista ou conjunto de listas, use [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) e fornece o número de identificação de uma lista ou lista específica. Você gerencia os índices usados para identificar listas de exibição com [**glGenLists,**](glgenlists.md) [**glListBase**](gllistbase.md)e [**glIsList.**](glislist.md) Para excluir um conjunto de listas de exibição, use [**glDeleteLists**](gldeletelists.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de listas de exibição](display-lists-reference.md)
</dt> </dl>

 

 





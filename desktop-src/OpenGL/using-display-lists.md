---
title: Usando listas de exibição
description: Usando listas de exibição
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, exibir listas
- Exibir listas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793ec78af0b19ac437e44f16e13b93db6eab32a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822468"
---
# <a name="using-display-lists"></a>Usando listas de exibição

Uma lista de exibição é um grupo de funções OpenGL que foi armazenado para execução subsequente. A função [**glNewList**](glnewlist.md) começa a criação de uma lista de exibição e a [**glEndList**](glendlist.md) a encerra. Com poucas exceções, as funções OpenGL chamadas entre **glNewList** e **glEndList** são acrescentadas à lista de exibição. (Consulte **glNewList** para obter uma lista das funções que você não pode armazenar e executar de dentro de uma lista de exibição.) Para disparar a execução de uma lista ou conjunto de listas, use [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) e forneça o número de identificação de uma lista ou listas específicas. Você gerencia os índices usados para identificar listas de exibição com [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md)e [**glIsList**](glislist.md). Para excluir um conjunto de listas de exibição, use [**glDeleteLists**](gldeletelists.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de listas de exibição](display-lists-reference.md)
</dt> </dl>

 

 





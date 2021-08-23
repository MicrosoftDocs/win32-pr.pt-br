---
title: Estrutura de carga Ray
description: Uma estrutura definida pelo usuário que é fornecida como um argumento Inout em uma chamada TraceRay e como um parâmetro Inout nos tipos de sombreador que podem acessar a carga Ray.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2c1c6944bc66d33ebd134d6e2d0899c1992624cfb4db3b0fc0aaa80a1ef99a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565626"
---
# <a name="ray-payload-structure"></a>Estrutura de carga Ray 

Uma estrutura definida pelo usuário que é fornecida como um argumento Inout em uma chamada [**TraceRay**](traceray-function.md) , e como um parâmetro Inout nos tipos de sombreador que podem acessar a carga Ray, que inclui [qualquer acesso, uma](any-hit-shader.md) [visita mais próxima](closest-hit-shader.md)e um sombreador [ausente](miss-shader.md) . Todos os sombreadores que acessam a carga Ray devem usar a mesma estrutura que aquela fornecida na chamada **TraceRay** de origem.  Mesmo que um desses sombreadores não referencie a carga de Ray, ele ainda deve especificar a carga correspondente como a chamada **TraceRay** de origem.


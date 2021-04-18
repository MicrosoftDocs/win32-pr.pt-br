---
title: Estrutura de carga Ray
description: Uma estrutura definida pelo usuário que é fornecida como um argumento Inout em uma chamada TraceRay e como um parâmetro Inout nos tipos de sombreador que podem acessar a carga Ray.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 9887bbadc2fd94b2e766c568a30fd6669f51e048
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "105764429"
---
# <a name="ray-payload-structure"></a>Estrutura de carga Ray 

Uma estrutura definida pelo usuário que é fornecida como um argumento Inout em uma chamada [**TraceRay**](traceray-function.md) , e como um parâmetro Inout nos tipos de sombreador que podem acessar a carga Ray, que inclui [qualquer acesso, uma](any-hit-shader.md) [visita mais próxima](closest-hit-shader.md)e um sombreador [ausente](miss-shader.md) . Todos os sombreadores que acessam a carga Ray devem usar a mesma estrutura que aquela fornecida na chamada **TraceRay** de origem.  Mesmo que um desses sombreadores não referencie a carga de Ray, ele ainda deve especificar a carga correspondente como a chamada **TraceRay** de origem.


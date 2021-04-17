---
title: Identificadores de propriedade/pares de deslocamento
description: A seguir a contagem do valor do conjunto de propriedades da propriedade é uma matriz de valores de conjunto de propriedades de identificadores de propriedade/pares de deslocamento.
ms.assetid: 341608a1-3ab1-4fa9-ab9a-4124c63c78a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b55ed20aef2c76dc97fcb3f4acfe981b9800308
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754097"
---
# <a name="property-identifiersoffset-pairs"></a>Identificadores de propriedade/pares de deslocamento

A seguir a contagem do valor do conjunto de propriedades da propriedade é uma matriz de valores de conjunto de propriedades de identificadores de propriedade/pares de deslocamento. Os identificadores de propriedade são valores de 32 bits que identificam exclusivamente uma propriedade dentro de uma seção. Os pares de deslocamento indicam a distância desde o início da seção até o início do par de tipo/valor da propriedade. Como os deslocamentos são relativos à seção, as seções podem ser copiadas como uma matriz de bytes.

Os identificadores de propriedade não são classificados em nenhuma ordem específica. As propriedades podem ser omitidas do conjunto de propriedades armazenadas; os leitores não devem confiar em uma ordem específica ou um intervalo de identificadores de propriedade.

 

 





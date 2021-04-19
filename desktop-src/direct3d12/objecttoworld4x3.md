---
description: Uma matriz para transformar de espaço de objeto em espaço mundial.
ms.assetid: ''
title: ObjectToWorld4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld4x3
api_type:
- NA
ms.openlocfilehash: 613b4c403f235819845114e7019e07051a25ec80
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807977"
---
# <a name="objecttoworld4x3"></a>ObjectToWorld4x3

Uma matriz para transformar de espaço de objeto em espaço mundial. Objeto-espaço refere-se ao espaço da estrutura de aceleração de nível inferior atual.

## <a name="syntax"></a>Sintaxe

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a>Comentários

A matriz é uma transposição da matriz **ObjectToWorld3x4** .

Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)





## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





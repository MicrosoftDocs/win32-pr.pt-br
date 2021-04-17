---
description: Retorna o valor passado como o parâmetro HitKind para ReportHit.
ms.assetid: ''
title: HitKind
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749523"
---
# <a name="hitkind"></a>HitKind

Retorna o valor passado como o parâmetro **HitKind** para [**ReportHit**](reporthit-function.md).

## <a name="syntax"></a>Sintaxe

```
uint HitKind();

```



## <a name="remarks"></a>Comentários

Se a interseção foi relatada pela interseção de triângulo de função fixa, **HitKind** será um dos tipos de toque na **\_ \_ \_ \_ face frontal** (254) ou no tipo de botão de **\_ \_ fundo de triângulo \_ \_** (255).

Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador de todos os cliques**](any-hit-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de interseção**](intersection-shader.md)





## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





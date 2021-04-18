---
description: Chamado de um sombreador qualquer clique para rejeitar o erro e encerrar o sombreador.
ms.assetid: ''
title: Função IgnoreHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770563"
---
# <a name="ignorehit-function"></a>Função IgnoreHit

Chamado de um [sombreador qualquer clique](any-hit-shader.md) para rejeitar o erro e encerrar o sombreador. A pesquisa de clique continua sem confirmar a distância e os atributos da visita atual.  A chamada [**ReportHit**](reporthit-function.md) no [sombreador de interseção](intersection-shader.md), se houver um, retornará false.  Todas as modificações feitas na carga Ray até esse ponto no sombreador qualquer clique são preservadas.

## <a name="syntax"></a>Sintaxe

```
void IgnoreHit();

```


## <a name="return-value"></a>Valor retornado

**void**

## <a name="remarks"></a>Comentários

Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador de todos os cliques**](any-hit-shader.md)




## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





---
description: Usado em um sombreador qualquer ocorrência para confirmar a ocorrência atual e, em seguida, parar de Pesquisar mais ocorrências para Ray.
ms.assetid: ''
title: Função AcceptHitAndEndSearch
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751747"
---
# <a name="accepthitandendsearch-function"></a>Função AcceptHitAndEndSearch

Usado em um [sombreador qualquer ocorrência](any-hit-shader.md) para confirmar a ocorrência atual e, em seguida, parar de Pesquisar mais ocorrências para Ray. Se houver um sombreador de interseção em execução, a execução será interrompida.  A execução passa para o [sombreador de clique mais próximo](closest-hit-shader.md), se habilitado, com a visita mais próxima registrada até agora.

## <a name="syntax"></a>Sintaxe

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a>Valor retornado

**void**

## <a name="remarks"></a>Comentários

Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador resgatável**](callable-shader.md)
* [**Sombreador do clique mais próximo**](closest-hit-shader.md)
* [**Sombreador de resolução**](miss-shader.md)
* [**Sombreador da geração de raio**](ray-generation-shader.md)



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





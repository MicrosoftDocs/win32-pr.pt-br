---
description: Chamado por um sombreador de interseção para relatar uma interseção de Ray.
ms.assetid: ''
title: Função ReportHit
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790623"
---
# <a name="reporthit-function"></a>Função ReportHit

Chamado por um [sombreador de interseção](intersection-shader.md) para relatar uma interseção de Ray.

## <a name="syntax"></a>Sintaxe
Essa definição de função intrínseca é equivalente ao seguinte modelo de função:

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a>Parâmetros

`THit`

Um valor float que especifica a distância paramétrica da interseção..

`HitKind`

Um inteiro sem sinal que identifica o tipo de ocorrência que ocorreu.  Este é um valor especificado pelo usuário no intervalo de 0-127.  O valor pode ser lido por [qualquer acesso](any-hit-shader.md) ou sombreadores de [tecle mais próximos](closest-hit-shader.md) com o intrínseco **HitKind** .

`Attributes`

A estrutura de [**estrutura de atributo de interseção**](intersection-attributes.md) definida pelo usuário que especifica os atributos de interseção.  

## <a name="return-value"></a>Valor Retornado

**bool** True se o pressionamento for aceito.  Um pressionamento será rejeitado se *THit* estiver fora do intervalo de Ray atual, ou se qualquer sombreador de clique chamar [**IgnoreHit**](ignorehit-function.md).  O intervalo de Ray atual é definido por **RayTMin** e **RayTCurrent**.

## <a name="remarks"></a>Comentários

Essa função pode ser chamada nos seguintes tipos de sombreador raytracing:

* [**Sombreador de interseção**](intersection-shader.md)





## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





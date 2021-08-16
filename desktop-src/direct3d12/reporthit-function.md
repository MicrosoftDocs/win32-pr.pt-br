---
description: Chamado por um sombreador de interseção para relatar uma interseção de raio.
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
ms.openlocfilehash: 8714cabc02f70ca12bcc78493de3a61482ba5aed5490087d309f6ec091cecf75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528104"
---
# <a name="reporthit-function"></a>Função ReportHit

Chamado por um [sombreador de interseção](intersection-shader.md) para relatar uma interseção de raio.

## <a name="syntax"></a>Syntax
Essa definição de função intrínseca é equivalente ao seguinte modelo de função:

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a>Parâmetros

`THit`

Um valor float que especifica a distância paramétrica da interseção..

`HitKind`

Um inteiro sem sinal que identifica o tipo de ocorrência que ocorreu.  Esse é um valor especificado pelo usuário no intervalo de 0 a 127.  O valor pode ser lido por [qualquer sombreadores](any-hit-shader.md) de [acerto](closest-hit-shader.md) ou de acerto mais próximos com o **intrínseco HitKind.**

`Attributes`

A estrutura Estrutura de Atributo de Interseção definida [**pelo**](intersection-attributes.md) usuário que especifica os atributos de interseção.  

## <a name="return-value"></a>Valor Retornado

**bool** True se o hit foi aceito.  Uma reação será rejeitada se *o THit* estiver fora do intervalo de raio atual ou se qualquer sombreador de acerto chamar [**IgnoreHit**](ignorehit-function.md).  O intervalo de raio atual é definido por **RayTMin** e **RayTCurrent.**

## <a name="remarks"></a>Comentários

Essa função pode ser chamada dos seguintes tipos de sombreador de raio:

* [**Sombreador de interseção**](intersection-shader.md)





## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência HLSL de raytracing do Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





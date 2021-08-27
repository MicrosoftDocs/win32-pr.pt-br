---
title: Função RWBuffer::Load(int)
description: Lê dados de buffer. | Função RWBuffer::Load(int)
ms.assetid: 3066E244-DE56-4F0D-8443-018B9EFEC1FF
keywords:
- Função de carregamento HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d3e3f9c9714cb4cc7f0f29bfa801e767b468d526836a7bd09f0f9823d9ff8868
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118296"
---
# <a name="rwbufferloadint-function"></a>Função RWBuffer::Load(int)

Lê dados de buffer.

## <a name="syntax"></a>Sintaxe


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localização* \[ Em\]
</dt> <dd>

Tipo: **int**

O local do buffer.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo:

O tipo de retorno corresponde ao tipo na declaração para o [**objeto RWBuffer.**](sm5-object-rwbuffer.md)

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](rwbuffer-load.md)
</dt> </dl>

 

 





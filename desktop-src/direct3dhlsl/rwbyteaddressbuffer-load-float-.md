---
title: Função RWByteAddressBuffer::Load(int)
description: Obtém um valor. | Função RWByteAddressBuffer::Load(int)
ms.assetid: C95C865E-E44D-46DC-A076-BD2903758432
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
ms.openlocfilehash: 4885a94041201eed790768cd6b75d07f8bd5ccd24b9d37ce56df734adced15ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672156"
---
# <a name="rwbyteaddressbufferloadint-function"></a>Função RWByteAddressBuffer::Load(int)

Obtém um valor.

## <a name="syntax"></a>Sintaxe


``` syntax
uint Load(
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

Tipo: **uint**

Um valor.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](rwbyteaddressbuffer-load.md)
</dt> </dl>

 

 





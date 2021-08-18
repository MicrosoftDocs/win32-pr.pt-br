---
title: Função RWTexture2DArray::Load(int)
description: Lê dados de textura. | Função RWTexture2DArray::Load(int)
ms.assetid: BC247B2A-1744-4E37-A501-22E4A592A32D
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
ms.openlocfilehash: 7459e0bfacda9075fd587be69f8a3d69adbefb855608e5f949e250d0e35de786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118790832"
---
# <a name="rwtexture2darrayloadint-function"></a>Função RWTexture2DArray::Load(int)

Lê dados de textura.

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

O local da textura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo:

O tipo de retorno corresponde ao tipo na declaração para o [**objeto RWTexture2DArray.**](sm5-object-rwtexture2darray.md)

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](rwtexture2darray-load.md)
</dt> </dl>

 

 





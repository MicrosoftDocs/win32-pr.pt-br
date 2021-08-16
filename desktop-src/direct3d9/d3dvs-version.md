---
description: Crie um token de número de versão do sombreador de vértice.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: D3DVS_VERSION macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 861295c9068bee9e40174d877a78628aa405b9cfa5d46414190fbb7b37904e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527252"
---
# <a name="d3dvs_version-macro"></a>Macro DE VERSÃO do D3DVS \_

Crie um token de número de versão do sombreador de vértice.

## <a name="syntax"></a>Sintaxe


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*\_Principal* 
</dt> <dd>

A versão principal do sombreador de vértice. Consulte comentários para ver os valores apropriados.

</dd> <dt>

*\_Secundária* 
</dt> <dd>

A versão do sombreador de vértice secundário. Consulte comentários para ver os valores apropriados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor DWORD que é uma versão do sombreador de vértice.

## <a name="remarks"></a>Comentários

Números de versão

O número de versão é uma combinação da versão principal e dos números de versão do sombreador de vértice secundário. Os números válidos são mostrados na tabela.



| Principal | Secundária | Exemplo             |
|-------|-------|---------------------|
| 1     | 1     | D3DVS \_ VERSÃO(1,1) |
| 2     | 0     | D3DVS \_ VERSÃO(2,0) |
| 3     | 0     | D3DVS \_ VERSÃO(3,0) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 





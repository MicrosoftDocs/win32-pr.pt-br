---
description: Crie um token de número de versão do sombreador de vértice.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: Macro D3DVS_VERSION (D3d9types. h)
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
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772634"
---
# <a name="d3dvs_version-macro"></a>Macro de versão do D3DVS \_

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

*\_Primária* 
</dt> <dd>

A versão principal do sombreador de vértice. Consulte comentários para obter os valores apropriados.

</dd> <dt>

*\_Secundária* 
</dt> <dd>

A versão secundária do sombreador de vértice. Consulte comentários para obter os valores apropriados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor DWORD que é uma versão de sombreador de vértice.

## <a name="remarks"></a>Comentários

Números de versão

O número de versão é uma combinação da versão principal e dos números de versão do sombreador de vértice secundário. Os números válidos são mostrados na tabela.



| Principal | Secundária | Exemplo             |
|-------|-------|---------------------|
| 1     | 1     | \_Versão D3DVS (1, 1) |
| 2     | 0     | \_Versão D3DVS (2, 0) |
| 3     | 0     | \_Versão D3DVS (3, 0) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 





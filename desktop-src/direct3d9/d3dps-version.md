---
description: Crie um token de versão do sombreador de pixel.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: Macro D3DPS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298659"
---
# <a name="d3dps_version-macro"></a>Macro de versão do D3DPS \_

Crie um token de versão do sombreador de pixel.

## <a name="syntax"></a>Sintaxe


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*\_Primária* 
</dt> <dd>

A versão principal do sombreador de pixels.

</dd> <dt>

*\_Secundária* 
</dt> <dd>

A versão do sombreador de pixel secundário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor DWORD que é uma versão do sombreador de pixel.

## <a name="remarks"></a>Comentários

Números de versão

O número de versão é uma combinação da versão principal e dos números de versão do sombreador de vértice secundário. Os números válidos são mostrados na tabela.



| Principal | Secundária | Exemplo             |
|-------|-------|---------------------|
| 1     | 1     | \_Versão D3DPS (1, 1) |
| 1     | 2     | \_Versão D3DPS (1, 2) |
| 1     | 3     | \_Versão D3DPS (1, 3) |
| 1     | 4     | \_Versão D3DPS (1, 4) |
| 2     | 0     | \_Versão D3DPS (2, 0) |
| 3     | 0     | \_Versão D3DPS (3, 0) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DCAPS9](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 





---
title: Função D3DX12GetBaseSubobjectType (D3dx12.h)
description: Retorna o tipo de subobjeto que corresponde à classe base do tipo de subobjeto passado.
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- Função D3DX12GetBaseSubobjectType
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd49b47e9fe603c0ebbdca015f3997eb06558a7039ddc866fb4d4667b8802b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989796"
---
# <a name="d3dx12getbasesubobjecttype-function"></a>Função D3DX12GetBaseSubobjectType

Retorna o tipo de subobjeto que corresponde à classe base do tipo de subobjeto passado.

## <a name="syntax"></a>Sintaxe


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SubobjectType* 
</dt> <dd>

Tipo: **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE**

Um valor de enumeração que especifica o tipo de subobjeto no qual você está interessado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE**

Se *SubobjectType* corresponder a um tipo de dados de subobjeto derivado de outro tipo de dados subobjeto, o tipo de subobjeto do tipo de dados de subobjeto base será retornado; caso contrário, o tipo de subobjeto passado será retornado. Por exemplo, se **D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT \_ TYPE DEPTH \_ \_ STENCIL1** for passado, **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE DEPTH \_ \_ STENCIL** será retornado.

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 






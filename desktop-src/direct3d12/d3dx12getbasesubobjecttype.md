---
title: Função D3DX12GetBaseSubobjectType (D3dx12. h)
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
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771477"
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

*Subobjecttype* 
</dt> <dd>

Tipo: **\_ \_ \_ \_ tipo de subobjeto de estado de pipeline D3D12**

Um valor de enumeração que especifica o tipo de subobjeto no qual você está interessado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **\_ \_ \_ \_ tipo de subobjeto de estado de pipeline D3D12**

Se *subobjecttype* corresponder a um tipo de dados de subobjeto derivado de outro tipo de dados de subobjeto, o tipo de subobjeto do tipo de dados de subobjeto base será retornado; caso contrário, o tipo de subobjeto passado é retornado. Por exemplo, se **D3D12 \_ \_ profundidade de \_ tipo de subobjeto \_ \_ \_ STENCIL1** for passado, o **\_ \_ \_ \_ \_ \_ estêncil profundidade de tipo de subobjeto do estado do pipeline D3D12** será retornado.

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 






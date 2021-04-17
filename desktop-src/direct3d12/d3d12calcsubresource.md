---
title: Função D3D12CalcSubresource (D3dx12. h)
description: Calcula um índice de subrecurso para uma textura.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- Função D3D12CalcSubresource
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762431"
---
# <a name="d3d12calcsubresource-function"></a>Função D3D12CalcSubresource

Calcula um índice de subrecurso para uma textura.

## <a name="syntax"></a>Sintaxe


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MipSlice* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O índice de base zero para o nível de mipmap a ser abordado; 0 indica o primeiro e mais detalhado nível de mipmap.

</dd> <dt>

*ArraySlice* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O índice de base zero para o nível de matriz a ser abordado; Sempre use 0 para texturas de volume (3D).

</dd> <dt>

*PlaneSlice* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O índice de base zero para o nível de plano a ser abordado.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de níveis de mipmap no recurso.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de elementos na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O índice que é igual a MipSlice + (ArraySlice \* MipLevels).

## <a name="remarks"></a>Comentários

Um buffer é um recurso não estruturado e, portanto, é definido como contendo um único subrecurso. As APIs que usam buffers não precisam de um índice de subrecurso. Uma textura por outro lado é altamente estruturada. Cada objeto de textura pode conter um ou mais subrecursos, dependendo do tamanho da matriz e do número de níveis de mipmap.

Para texturas de volume (3D), todas as fatias de um determinado nível de mipmap são um índice de subrecurso único.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Sub-recursos](subresources.md)
</dt> </dl>

 


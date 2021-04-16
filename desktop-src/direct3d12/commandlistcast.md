---
title: Função CommandListCast (D3dx12. h)
description: Esse modelo de função converte um ponteiro constante para qualquer lista de comandos em um ponteiro const para um ID3D12CommandList.
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- Função CommandListCast
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772504"
---
# <a name="commandlistcast-function"></a>Função CommandListCast

Esse modelo de função converte um ponteiro constante para qualquer lista de comandos em um ponteiro const para um ID3D12CommandList.

Essa conversão é útil para passar ponteiros de lista de comandos fortemente tipados para o [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

## <a name="syntax"></a>Sintaxe


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PP* 
</dt> <dd>

Tipo: **t \_ CommandListType \* const \***

A lista de comandos fortemente tipados a ser convertida.

O argumento de modelo **t \_ CommandListType** Especifica qualquer objeto de lista de comandos fortemente tipados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **ID3D12CommandList \* const \***

A lista de comandos com rigidez de tipos, reinterpreta como um [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).

## <a name="remarks"></a>Comentários

CommandListCast executa uma **\_ conversão de reinterpretação**. A conversão é válida, contanto que const-qualidade da lista de comandos seja respeitado.

A função CommandListCast é definida da seguinte maneira:


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



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

 

 






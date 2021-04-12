---
description: Usado com resultados compactados da versão de vértice do simulador de transferência radiante (PRT) de computação.
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: Função D3DXSHPRTCompSplitMeshSC (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 18742d12b6e1ae106dcf832baccccb2416465880
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370940"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a>Função D3DXSHPRTCompSplitMeshSC

Usado com resultados compactados da versão de vértice do simulador de transferência radiante (PRT) de computação. Depois que [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) tiver sido chamado, essa função poderá ser usada para dividir a malha em um grupo de faces/vértices por supercluster. Cada super cluster contém todas as faces que contêm qualquer vértice classificado em um de seus clusters. Todos os vértices conectados a esse conjunto de faces também estão incluídos na matriz retornada ppVertStatus indicando se o vértice pertence ou não ao Super cluster.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pClusterIDs* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

*NumVertices* IDs de cluster (extraídas de um buffer compactado).

</dd> <dt>

*NumVertices* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices na malha original.

</dd> <dt>

*NumCs* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de clusters (parâmetro de entrada para compactação).

</dd> <dt>

*pSClusterIDs* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Matriz de tamanho *NumCs* que conterá as IDs de supercluster.

</dd> <dt>

*NumSCs* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de superclusters alocados em [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).

</dd> <dt>

*pInputIB* \[ no\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Buffer de índice bruto para malha. O formato depende de *InputIBIs32Bit*.

</dd> <dt>

*InputIBIs32Bit* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se for **true**, o buffer de índice será definido como 32 bit; caso contrário, 16 bits.

</dd> <dt>

*NumFaces* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de rostos na malha original (*pInputIB* é 3 vezes esse comprimento.)

</dd> <dt>

*ppIBData* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer de índice bruto que conterá as faces divididas resultantes. Formato determinado por *InputIBIs32Bit*. Alocada por função.

</dd> <dt>

*pIBDataLength* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Comprimento de *ppIBData*, atribuído na função.

</dd> <dt>

*OutputIBIs32Bit* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **for true**, alocará uma matriz de inteiros sem sinal; caso contrário, o aloca uma matriz curta não assinada.

</dd> <dt>

*ppFaceRemap* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mapeamento de cada face em *ppIBData* para faces originais. O comprimento é \* *pIBDataLength*/3.

</dd> <dt>

*ppVertData* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Nova estrutura de dados de vértice. Tamanho de *pVertDataLength*.

</dd> <dt>

*pVertDataLength* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Número de novos vértices na malha dividida. Atribuído na função.

</dd> <dt>

*pSCClusterList* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Matriz de comprimento *NumCs* quais índices *PSCData* (campos *pClusterIDs* \* ) para cada supercluster, contém clusters classificados por supercluster.

</dd> <dt>

*pSCData* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***

Estrutura por supercluster. Contém índices em *ppIBData*, *pSCClusterList* e *ppVertData*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de transferência radiante preputadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 

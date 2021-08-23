---
description: Função D3DXSHPRTCompSplitMeshSC – usada com resultados compactados da versão de vértice do simulador de PRT (transferência de radiance pré-comutada).
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: Função D3DXSHPRTCompSplitMeshSC (D3DX9Mesh.h)
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
ms.openlocfilehash: 14b138ae4c1b61b70147726d1a320e8dca1c0a57ffb11dd742419a46f9d131b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630866"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a>Função D3DXSHPRTCompSplitMeshSC

Usado com resultados compactados da versão de vértice do simulador de PRT (transferência de radiance pré-comutada). Depois [**que D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) tiver sido chamado, essa função poderá ser usada para dividir a malha em um grupo de faces/vértices por super cluster. Cada super cluster contém todos os rostos que contêm qualquer vértice classificado em um de seus clusters. Todos os vértices conectados a esse conjunto de faces também são incluídos com a matriz retornada ppVertStatus, indicando se o vértice pertence ou não ao super cluster.

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

*pClusterIDs* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

IDs de cluster *numVertices* (extraídas de um buffer compactado.)

</dd> <dt>

*NumVertices* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vértices na malha original.

</dd> <dt>

*NumCs* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de clusters (parâmetro de entrada para compactação.)

</dd> <dt>

*pSClusterIDs* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Matriz de *numCs de tamanho* que conterão IDs de super cluster.

</dd> <dt>

*NumSCs* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de super clusters alocados [**em D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).

</dd> <dt>

*pInputIB* \[ Em\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Buffer de índice bruto para malha. O formato depende de *InputIBIs32Bit.*

</dd> <dt>

*InputIBIs32Bit* \[ Em\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Se **TRUE**, o buffer de índice será definido como 32 bits; caso contrário, 16 bits.

</dd> <dt>

*NumFaces* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de faces na malha original (*pInputIB* tem três vezes esse comprimento.)

</dd> <dt>

*ppIBData* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer de índice bruto que conterá as faces divididas resultantes. Formato determinado por *InputIBIs32Bit.* Alocado por função.

</dd> <dt>

*pIBDataLength* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Comprimento de *ppIBData*, atribuído na função .

</dd> <dt>

*OutputIBIs32Bit* \[ in, out\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Se **TRUE**, alocará uma matriz de inteiros sem sinal; caso contrário, alocará uma matriz curta sem assinatura.

</dd> <dt>

*ppFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mapeamento de cada rosto em *ppIBData para* rostos originais. Length é \* *pIBDataLength*/3.

</dd> <dt>

*ppVertData* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Nova estrutura de dados de vértice. Tamanho de *pVertDataLength.*

</dd> <dt>

*pVertDataLength* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Número de novos vértices na malha dividida. Atribuído na função .

</dd> <dt>

*pSCClusterList* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Matriz de *NumCs de* comprimento em que *pSCData* indexa (*campos pClusterIDs)* para cada \* supercluster, contém clusters classificação por supercluster.

</dd> <dt>

*pSCData* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***

Estrutura por super cluster. Contém índices em *ppIBData,* *pSCClusterList* e *ppVertData.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de transferência de Radiance pré-comutadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 

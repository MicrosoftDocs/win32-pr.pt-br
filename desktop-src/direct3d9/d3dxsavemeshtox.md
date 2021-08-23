---
description: Salva uma malha em um arquivo .x.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: Função D3DXSaveMeshToX (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 668131237def6078d775d0002f624b035ad29e21b9a49399b673933dc63e5b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988427"
---
# <a name="d3dxsavemeshtox-function"></a>Função D3DXSaveMeshToX

Salva uma malha em um arquivo .x.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFilename* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados de cadeia de caracteres será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*pMesh* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para uma interface [**ID3DXMesh,**](id3dxmesh.md) que representa a malha a ser salva em um arquivo .x.

</dd> <dt>

*pAdjacency* \[ Em\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada rosto na malha. Esse parâmetro pode ser **NULL.**

</dd> <dt>

*pMaterials* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***

Ponteiro para uma matriz de [**estruturas D3DXMATERIAL,**](d3dxmaterial.md) contendo informações de material a serem salvas no arquivo .x.

</dd> <dt>

*pEffectInstances* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

Ponteiro para uma matriz de instâncias de efeito, uma por grupo de atributos na malha. Esse parâmetro pode ser **NULL.** Uma instância de efeito é uma instância específica de informações de estado usadas para inicializar um efeito. Para obter mais informações, [**consulte D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

*NumMaterials* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de [**estruturas D3DXMATERIAL**](d3dxmaterial.md) na *matriz pMaterials.*

</dd> <dt>

*Formato* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação de opções de formato de arquivo e salvar ao salvar um arquivo .x. Consulte [Constantes de arquivo D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para D3DXSaveMeshToXW. Caso contrário, a chamada de função será resolvida para D3DXSaveMeshToXA porque as cadeias de caracteres ANSI estão sendo usadas.

O formato de arquivo padrão é binário; no entanto, se um arquivo for especificado como um binário e um arquivo de texto, ele será salvo como um arquivo de texto. Independentemente do formato de arquivo, você também pode usar o formato compactado para reduzir o tamanho do arquivo.

Veja a seguir um exemplo de código típico de como usar essa função.


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 

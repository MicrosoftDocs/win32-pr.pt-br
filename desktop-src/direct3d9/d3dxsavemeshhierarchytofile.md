---
description: Cria um arquivo .x e salva a hierarquia de malha e as animações correspondentes nele.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: Função D3DXSaveMeshHierarchyToFile (D3dx9varm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 892d27e305badc2cf1b21de41a1f9d37da13f36c1521135a79a65619e31903f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298524"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a>Função D3DXSaveMeshHierarchyToFile

Cria um arquivo .x e salva a hierarquia de malha e as animações correspondentes nele.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFilename* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo .x que identifica a malha salva. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados de cadeia de caracteres será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*XFormat* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Formato do arquivo .x (texto ou binário, compactado ou não). Consulte \_ FILEFORMAT D3DXF. FILEFORMAT COMPRESSED D3DXF pode ser combinado (usando um OR lógico) com os sinalizadores \_ \_ D3DXF \_ FILEFORMAT BINARY ou \_ D3DXF \_ FILEFORMAT \_ TEXT para reduzir o tamanho do arquivo de saída.

</dd> <dt>

*pFrameRoot* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Nó raiz da hierarquia a ser salva. Consulte [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pAnimController* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

Controlador de animação que tem conjuntos de animação a serem armazenados. Consulte [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> <dt>

*pUserDataSaver* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**

Interface fornecida pelo aplicativo que permite salvar dados do usuário. Consulte [**ID3DXSaveUserData**](id3dxsaveuserdata.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para D3DXSaveMeshHierarchyToFileW. Caso contrário, a chamada de função será resolvida para D3DXSaveMeshHierarchyToFileA.

Essa função não salva conjuntos de animação compactados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de animação](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[Referência de arquivo X](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 

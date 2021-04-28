---
description: Função D3DXLoadMeshHierarchyFromX – carrega a primeira hierarquia de quadro de um arquivo. x.
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: Função D3DXLoadMeshHierarchyFromX (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f6f08e10155509df800cca3cb3788d6b27e520
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114354"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a>Função D3DXLoadMeshHierarchyFromX

Carrega a primeira hierarquia de quadros de um arquivo. x.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do arquivo* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR. Caso contrário, o tipo de dados String será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*Malhas* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) que especificam as opções de criação para a malha.

</dd> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o objeto de dispositivo associado à malha.

</dd> <dt>

*pAlloc* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Ponteiro para uma interface [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .

</dd> <dt>

*pUserDataLoader* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Interface fornecida pelo aplicativo que permite o carregamento de dados do usuário. Consulte [**ID3DXLoadUserData**](id3dxloaduserdata.md).

</dd> <dt>

*ppFrameHierarchy* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***

Retorna um ponteiro para a hierarquia de quadro carregada. Consulte [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*ppAnimController* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Retorna um ponteiro para o controlador de animação correspondente à animação no arquivo. x. Isso é criado com rastreamentos e eventos padrão. Consulte [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como D3DXLoadMeshHierarchyFromXW. Caso contrário, a chamada de função será resolvida como D3DXLoadMeshHierarchyFromXA.

Todas as malhas no arquivo serão recolhidas em uma malha de saída. Se o arquivo contiver uma hierarquia de quadros, todas as transformações serão aplicadas à malha.

**D3DXLoadMeshHierarchyFromX** carrega os dados de animação e a hierarquia de quadros de um arquivo. x. Ele examina o arquivo. x e cria uma hierarquia de quadros e um controlador de animação de acordo com o objeto derivado de [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)passado para ele por meio de pAlloc. O carregamento dos dados requer várias etapas da seguinte maneira:

1.  Derive [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementando cada método. Isso controla como os quadros e as malhas são alocados e liberados.
2.  Derive [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementando cada método. Se o arquivo. x não tiver dados inseridos definidos pelo usuário ou se você não precisar dele, poderá ignorar essa parte.
3.  Crie um objeto da classe [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) e, opcionalmente, da classe loaduserdata. Você não precisa chamar nenhum método desses objetos por conta própria.
4.  Chame **D3DXLoadMeshHierarchyFromX**, passando o objeto [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) e o objeto [**ID3DXLoadUserData**](id3dxloaduserdata.md) (ou **NULL**) para criar a hierarquia de quadros e o controlador de animação. Todos os conjuntos de animação e quadros são automaticamente registrados no controlador de animação.

Durante a carga, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) e [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) são chamados de volta em cada quadro para controlar o carregamento e a alocação do quadro. O aplicativo define esses métodos para controlar como os quadros são armazenados. [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) e [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) são chamados de volta em cada objeto de malha para controlar o carregamento e a alocação de objetos de malha. [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) é chamado de volta para cada objeto de nível superior que não é carregado por outros métodos.

Para liberar esses dados, chame ID3DXAnimationController:: Release para liberar os conjuntos de animação e [**D3DXFRAMEDestroy**](d3dxframedestroy.md), passando o nó raiz da hierarquia de quadros e um objeto de sua classe [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) derivada. [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) e [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) serão chamados para cada objeto de quadro e malha na hierarquia de quadros. Sua implementação do **DestroyFrame** deve liberar tudo alocado pelo [**CreateFrame**](id3dxallocatehierarchy--createframe.md)e, da mesma forma, para os métodos de contêiner de malha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções de animação](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 

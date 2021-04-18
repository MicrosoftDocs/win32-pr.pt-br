---
description: Essa interface é implementada pelo aplicativo para salvar os dados de usuário adicionais inseridos nos arquivos. x.
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: Interface ID3DXLoadUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb07ba9351e5f6c23dd86c8147151932b3972ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772532"
---
# <a name="id3dxloaduserdata-interface"></a>Interface ID3DXLoadUserData

Essa interface é implementada pelo aplicativo para salvar os dados de usuário adicionais inseridos nos arquivos. x. Uma instância dessa interface é passada para [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)e D3DX chama o método apropriado nessa interface sempre que os dados apropriados são encontrados. Por exemplo, para cada objeto de quadro no arquivo. x, [**ID3DXLoadUserData:: LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) é chamado e passado os dados filho.

## <a name="members"></a>Membros

A interface **ID3DXLoadUserData** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXLoadUserData** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXLoadUserData** tem esses métodos.



| Método                                                              | Descrição                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) | Carregar dados filho do quadro de um arquivo. x.<br/> |
| [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md)   | Carregar dados filho de malha de um arquivo. x.<br/>  |
| [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md)     | Carregar dados de nível superior de um arquivo. x.<br/>   |



 

## <a name="remarks"></a>Comentários

O tipo LPD3DXLOADUSERDATA é definido como um ponteiro para essa interface.


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

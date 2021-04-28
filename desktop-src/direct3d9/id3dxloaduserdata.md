---
description: Interface ID3DXLoadUserData – essa interface é implementada pelo aplicativo para salvar os dados de usuário adicionais inseridos nos arquivos. x.
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
ms.openlocfilehash: 83d603d2ec5fde00ef0b29d84368e04a1276f992
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093624"
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

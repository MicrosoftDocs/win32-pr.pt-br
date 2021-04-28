---
description: Interface ID3DXSaveUserData – essa interface é implementada pelo aplicativo para salvar os dados de usuário adicionais inseridos nos arquivos. x.
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: Interface ID3DXSaveUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5dbdc71239455772809e44f535634a0d06cc0653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107174"
---
# <a name="id3dxsaveuserdata-interface"></a>Interface ID3DXSaveUserData

Essa interface é implementada pelo aplicativo para salvar os dados de usuário adicionais inseridos nos arquivos. x. Uma instância dessa interface é passada para [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)e D3DX chama o método apropriado nessa interface sempre que os dados apropriados são encontrados. Por exemplo, para cada objeto de quadro no arquivo. x, [**ID3DXSaveUserData:: AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) é chamado e passado os dados filho.

## <a name="members"></a>Membros

A interface **ID3DXSaveUserData** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSaveUserData** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXSaveUserData** tem esses métodos.



| Método                                                                              | Descrição                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md)                   | Adicione dados filho ao quadro.<br/>                            |
| [**AddMeshChildData**](id3dxsaveuserdata--addmeshchilddata.md)                     | Adicione dados filho à malha.<br/>                             |
| [**AddTopLevelDataObjectsPost**](id3dxsaveuserdata--addtopleveldataobjectspost.md) | Adicione um objeto de nível superior após a hierarquia de quadros.<br/>       |
| [**AddTopLevelDataObjectsPre**](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | Adicione um objeto de nível superior antes da hierarquia de quadros.<br/>      |
| [**RegisterTemplates**](id3dxsaveuserdata--registertemplates.md)                   | Um retorno de chamada para o usuário registrar um modelo de arquivo. x.<br/> |
| [**SaveTemplates**](id3dxsaveuserdata--savetemplates.md)                           | Um retorno de chamada para o usuário salvar um modelo de arquivo. x.<br/>     |



 

## <a name="remarks"></a>Comentários

O tipo LPD3DXSAVEUSERDATA é definido como um ponteiro para essa interface.


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
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

 

 

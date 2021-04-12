---
description: Os aplicativos usam os métodos da interface ID3DXFileData para criar ou acessar a hierarquia imediata do objeto de dados. As restrições de modelo determinam a hierarquia.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: Interface ID3DXFileData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173084"
---
# <a name="id3dxfiledata-interface"></a>Interface ID3DXFileData

Os aplicativos usam os métodos da interface ID3DXFileData para criar ou acessar a hierarquia imediata do objeto de dados. As restrições de modelo determinam a hierarquia.

## <a name="members"></a>Membros

A interface **ID3DXFileData** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileData** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXFileData** tem esses métodos.



| Método                                            | Descrição                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**GetChild**](id3dxfiledata--getchild.md)       | Recupera um objeto filho neste objeto de dados de arquivo.<br/>                                                        |
| [**GetChildren**](id3dxfiledata--getchildren.md) | Recupera o número de filhos neste objeto de dados de arquivo.<br/>                                                |
| [**Getenum**](id3dxfiledata--getenum.md)         | Recupera o objeto de enumeração neste objeto de dados de arquivo.<br/>                                                |
| [**GetId**](id3dxfiledata--getid.md)             | Recupera o GUID deste objeto de dados de arquivo.<br/>                                                              |
| [**GetName**](id3dxfiledata--getname.md)         | Recupera o nome deste objeto de dados de arquivo.<br/>                                                              |
| [**GetType**](id3dxfiledata--gettype.md)         | Recupera a ID do modelo neste objeto de dados de arquivo.<br/>                                                       |
| [**IsReference**](id3dxfiledata--isreference.md) | Indica se este objeto de dados de arquivo é um objeto de referência que aponta para outro objeto de dados filho.<br/>   |
| [**Bloquear**](id3dxfiledata--lock.md)               | Acessa os dados do arquivo. x.<br/>                                                                                |
| [**Unlock**](id3dxfiledata--unlock.md)           | Termina o ciclo de vida do ponteiro *ppData* retornado por [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).<br/> |



 

## <a name="remarks"></a>Comentários

Os tipos de dados permitidos pelo modelo são chamados de membros opcionais. Os membros opcionais não são necessários, mas um objeto pode perder informações importantes sem eles. Esses membros opcionais são salvos como filhos do objeto de dados. Um filho pode ser outro objeto de dados ou uma referência a um objeto de dados anterior.

O GUID da interface ID3DXFileData é ID3DXFileData IID \_ .

O tipo LPD3DXFILEDATA é definido como um ponteiro para essa interface.


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces de arquivo D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 

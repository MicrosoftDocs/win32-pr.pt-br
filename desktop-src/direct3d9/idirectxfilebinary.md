---
description: Os aplicativos usam os métodos da interface IDirectXFileBinary para ler e recuperar informações sobre dados binários. Preterido.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: Interface IDirectXFileBinary (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: b6707e4e685289f16b85ab85c2cce13dcd1da962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172964"
---
# <a name="idirectxfilebinary-interface"></a>Interface IDirectXFileBinary

Os aplicativos usam os métodos da interface IDirectXFileBinary para ler e recuperar informações sobre dados binários. Preterido.

## <a name="members"></a>Membros

A interface **IDirectXFileBinary** herda de [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileBinary** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDirectXFileBinary** tem esses métodos.



| Método                                                 | Descrição                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetMimeType**](idirectxfilebinary--getmimetype.md) | Recupera o tipo MIME (Multipurpose Internet Mail Extensions) para os dados binários. Preterido.<br/> |
| [**GetSize**](idirectxfilebinary--getsize.md)         | Recupera o tamanho dos dados binários. Preterido.<br/>                                               |
| [**Ler**](idirectxfilebinary--read.md)               | Lê os dados binários. Preterido.<br/>                                                               |



 

## <a name="remarks"></a>Comentários

O GUID da interface IDirectXFileBinary é IDirectXFileBinary IID \_ .

O tipo LPDIRECTXFileBinary é definido como um ponteiro para essa interface.


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[X interfaces de arquivo](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 





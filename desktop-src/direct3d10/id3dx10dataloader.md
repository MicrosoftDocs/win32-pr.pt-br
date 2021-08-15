---
description: Objeto de carregamento de dados usado pela interface ID3DX10ThreadPump para carregar dados de forma assíncrona.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: Interface ID3DX10DataLoader (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 86da40dd581c10d9f567f6011cd3987710a9aa36e41f360dc4ffc2662f909c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128349"
---
# <a name="id3dx10dataloader-interface"></a>Interface ID3DX10DataLoader

Objeto de carregamento de dados usado pela [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para carregar dados de forma assíncrona.

## <a name="members"></a>Membros

A interface **ID3DX10DataLoader** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10DataLoader** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX10DataLoader** tem esses métodos.



| Método                                             | Descrição                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Descompactar**](id3dx10dataloader-decompress.md) | Usado para descompactar dados codificados. Normalmente, isso seria usado para carregar recursos de sistemas de arquivos, como arquivos ZIP. Ao carregar de um recurso descompactado, o estágio de descompactação não precisa fazer nenhum trabalho.<br/> |
| [**Destruir**](id3dx10dataloader-destroy.md)       | Usado por uma [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para destruir o carregador após a conclusão de um item de trabalho.<br/>                                                                                                   |
| [**Carregar**](id3dx10dataloader-load.md)             | Usado por uma [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para carregar dados de um disco.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser herdado e seus membros são redefinidos. Isso permitiria que você personalize a API para carregar e descompactar seus próprios formatos de arquivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

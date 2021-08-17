---
description: Objeto de processamento de dados usado pela interface ID3DX10ThreadPump para processar dados carregados de forma assíncrona.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Interface ID3DX10DataProcessor (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ddb192a0591ce241e216b3bd0471212fc4801fbf1c901430c187f5370237049d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128365"
---
# <a name="id3dx10dataprocessor-interface"></a>Interface ID3DX10DataProcessor

Objeto de processamento de dados usado pela [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para processar dados carregados de forma assíncrona.

## <a name="members"></a>Membros

A interface **ID3DX10DataProcessor** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10DataProcessor** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX10DataProcessor** tem esses métodos.



| Método                                                                | Descrição                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md) | Crie um objeto de dispositivo.<br/>                                                                                                  |
| [**Destruir**](id3dx10dataprocessor-destroy.md)                       | Usado por uma [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para destruir o processador após a conclusão de um item de trabalho.<br/> |
| [**Processar**](id3dx10dataprocessor-process.md)                       | Processe alguns dados.<br/>                                                                                                       |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser herdado e seus membros redefinidos. Isso permite que você personalize a API para processar seus próprios formatos de arquivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

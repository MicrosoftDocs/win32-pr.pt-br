---
description: Objeto de processamento de dados usado pela interface ID3DX10ThreadPump para processar dados carregados de forma assíncrona.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Interface ID3DX10DataProcessor (D3DX10. h)
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
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837986"
---
# <a name="id3dx10dataprocessor-interface"></a>Interface ID3DX10DataProcessor

Objeto de processamento de dados usado pela [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para processar dados carregados de forma assíncrona.

## <a name="members"></a>Membros

A interface **ID3DX10DataProcessor** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10DataProcessor** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX10DataProcessor** tem esses métodos.



| Método                                                                | Descrição                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**Deviceobject**](id3dx10dataprocessor-createdeviceobject.md) | Crie um objeto de dispositivo.<br/>                                                                                                  |
| [**Destruir**](id3dx10dataprocessor-destroy.md)                       | Usado por uma [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) para destruir o processador após a conclusão de um item de trabalho.<br/> |
| [**Processar**](id3dx10dataprocessor-process.md)                       | Processar alguns dados.<br/>                                                                                                       |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser herdado e seus membros são redefinidos. Isso permitiria que você personalize a API para processar seus próprios formatos de arquivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

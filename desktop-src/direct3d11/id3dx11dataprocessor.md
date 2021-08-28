---
title: Interface ID3DX11DataProcessor (D3DX11core.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Objeto de processamento de dados usado pela interface ID3DX11ThreadPump para carregar dados de forma assíncrona.
ms.assetid: ab893879-416f-4b17-9035-a7f03a62b753
keywords:
- Interface ID3DX11DataProcessor Direct3D 11
- Interface ID3DX11DataProcessor Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 808c7d1bf1bdef1223e5b57e40ea5e6a90878101
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469343"
---
# <a name="id3dx11dataprocessor-interface"></a>Interface ID3DX11DataProcessor

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Objeto de processamento de dados usado pela [**interface ID3DX11ThreadPump**](id3dx11threadpump.md) para carregar dados de forma assíncrona.

## <a name="members"></a>Membros

A interface **ID3DX11DataProcessor** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11DataProcessor** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11DataProcessor** tem esses métodos.




| Método | Descrição | 
|--------|-------------|
| <a href="id3dx11dataprocessor-createdeviceobject.md"><strong>CreateDeviceObject</strong></a> | <blockquote>[!Note]<br />A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.</blockquote><br /> Cria um objeto de dispositivo.<br /> | 
| <a href="id3dx11dataprocessor-destroy.md"><strong>Destruir</strong></a> | <blockquote>[!Note]<br />A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.</blockquote><br /> Destrói o processador depois que um item de trabalho é concluído.<br /> | 
| <a href="id3dx11dataprocessor-process.md"><strong>Processar</strong></a> | <blockquote>[!Note]<br />A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.</blockquote><br /> Processa dados.<br /> | 




 

## <a name="remarks"></a>Comentários

Esse objeto pode ser herdado e seus membros redefinidos para processar formatos de arquivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>D3DX11core.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 


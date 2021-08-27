---
title: Interface ID3DX11DataLoader (D3DX11core.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Objeto de carregamento de dados usado pela interface ID3DX11ThreadPump para carregar dados de forma assíncrona.
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- Interface ID3DX11DataLoader Direct3D 11
- Interface ID3DX11DataLoader Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11DataLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b688fcbeff21edf23f6a3be1b39be5a9cf0000
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471642"
---
# <a name="id3dx11dataloader-interface"></a>Interface ID3DX11DataLoader

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Objeto de carregamento de dados usado [**pela interface ID3DX11ThreadPump**](id3dx11threadpump.md) para carregar dados de forma assíncrona.

## <a name="members"></a>Membros

A interface **ID3DX11DataLoader** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11DataLoader** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11DataLoader** tem esses métodos.




| Método | Descrição | 
|--------|-------------|
| <a href="id3dx11dataloader-decompress.md"><strong>Descomprimir</strong></a> | <blockquote>[!Note]<br />A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.</blockquote><br /> Descompacta dados codificados.<br /> | 
| <a href="id3dx11dataloader-destroy.md"><strong>Destruir</strong></a> | <blockquote>[!Note]<br />A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.</blockquote><br /> Destrói o carregador depois que um item de trabalho é concluído.<br /> | 
| <a href="id3dx11dataloader-load.md"><strong>Carregar</strong></a> | <blockquote>[!Note]<br />A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.</blockquote><br /> Carrega dados de um disco.<br /> | 




 

## <a name="remarks"></a>Comentários

Esse objeto pode ser herdado e seus membros redefinidos. Isso permite que você personalize a API para carregar e descompactar seus próprios formatos de arquivo personalizados.

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

 


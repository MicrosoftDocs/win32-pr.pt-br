---
title: Interface ID3DX11DataProcessor (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Objeto de processamento de dados usado pela interface ID3DX11ThreadPump para carregar dados de forma assíncrona.
ms.assetid: ab893879-416f-4b17-9035-a7f03a62b753
keywords:
- Interface ID3DX11DataProcessor Direct3D 11
- Interface ID3DX11DataProcessor Direct3D 11, descrita
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
ms.openlocfilehash: 5e421a6e840665220311e5a27c0692cd7f347e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104967256"
---
# <a name="id3dx11dataprocessor-interface"></a>Interface ID3DX11DataProcessor

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Objeto de processamento de dados usado pela [**interface ID3DX11ThreadPump**](id3dx11threadpump.md) para carregar dados de forma assíncrona.

## <a name="members"></a>Membros

A interface **ID3DX11DataProcessor** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11DataProcessor** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11DataProcessor** tem esses métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataprocessor-createdeviceobject.md"><strong>Deviceobject</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/> Cria um objeto de dispositivo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11dataprocessor-destroy.md"><strong>Destruir</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/> Destrói o processador após a conclusão de um item de trabalho.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataprocessor-process.md"><strong>Processar</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/> Processa dados.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser herdado e seus membros redefinidos para processar formatos de arquivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 


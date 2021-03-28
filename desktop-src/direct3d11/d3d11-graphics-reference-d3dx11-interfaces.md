---
title: Interfaces D3DX (gráficos do Direct3D 11)
description: Esta seção contém informações de referência para as interfaces de modelo de objeto de componente (COM) fornecidas pela biblioteca do utilitário D3DX.
ms.assetid: 0d3be1e6-b558-4586-9440-251a5611d7cd
keywords:
- Interfaces D3DX, Direct3D 11
- interfaces, Direct3D 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da2890c3c55d1bac9eba09c046927e432b1a27f8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008687"
---
# <a name="d3dx-interfaces-direct3d-11-graphics"></a>Interfaces D3DX (gráficos do Direct3D 11)

Esta seção contém informações de referência para as interfaces de modelo de objeto de componente (COM) fornecidas pela biblioteca do utilitário D3DX.

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 


## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="id3dx11dataloader.md"><strong>ID3DX11DataLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/> Objeto de carregamento de dados usado pela <a href="id3dx11threadpump.md"><strong>interface ID3DX11ThreadPump</strong></a> para carregar dados de forma assíncrona.<br/></td>
</tr>
<tr class="even">
<td><a href="id3dx11dataprocessor.md"><strong>ID3DX11DataProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/> Objeto de processamento de dados usado pela <a href="id3dx11threadpump.md"><strong>interface ID3DX11ThreadPump</strong></a> para carregar dados de forma assíncrona.<br/></td>
</tr>
<tr class="odd">
<td><a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/> Uma bomba de thread executa tarefas de forma assíncrona. Ele é criado chamando <a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a>. Há várias APIs que usam uma bomba de thread opcional como um parâmetro, como <a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a> e <a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a>; Se você passar uma interface de bombeamento de thread para essas APIs, as funções serão executadas de forma assíncrona em um thread separado. Especialmente em máquinas com vários processadores, uma bomba de thread pode carregar recursos e processar dados sem uma diminuição perceptível no desempenho.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

 






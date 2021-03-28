---
title: Funções D3DX (gráficos do Direct3D 11)
description: Esta seção contém informações sobre as funções do D3DX 11.
ms.assetid: 7548c02e-c8c2-4629-95ac-d21ca7a39f0a
keywords:
- funções, DirectX 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b76c1764f464461b4800a9161ac37dcff8c539a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369054"
---
# <a name="d3dx-functions-direct3d-11-graphics"></a>Funções D3DX (gráficos do Direct3D 11)

Esta seção contém informações sobre as funções do D3DX 11.

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
<td><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> .
</blockquote>
<br/> Compilar um sombreador ou um efeito de um arquivo.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .
</blockquote>
<br/> Compile um sombreador ou um efeito que é carregado na memória.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use <a href="/windows/desktop/menurc/resources-functions">funções de recurso</a>e, em seguida, compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .
</blockquote>
<br/> Compilar um sombreador ou um efeito de um recurso.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>ComputeNormalMap</strong>.
</blockquote>
<br/> Converte um mapa de altura em um mapa normal. Os componentes (x, y, z) de cada normal são mapeados para os canais (r, g, b) da textura de saída.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações.
</blockquote>
<br/> Crie um processador de dados assíncronos para um sombreador.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações.
</blockquote>
<br/> Crie um carregador de arquivo assíncrono.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações.
</blockquote>
<br/> Crie um carregador de memória assíncrona.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações.
</blockquote>
<br/> Crie um carregador de recurso assíncrono.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações.
</blockquote>
<br/> Crie um processador de dados para um sombreador de forma assíncrona.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações.
</blockquote>
<br/> Crie um processador de dados para ser usado com uma <a href="id3dx11threadpump.md"><strong>bomba de thread</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações.
</blockquote>
<br/> Crie um processador de dados para ser usado com uma <a href="id3dx11threadpump.md"><strong>bomba de thread</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações.
</blockquote>
<br/> Crie um processador de dados que carregará um recurso e, em seguida, crie uma exibição de recurso de sombreador para ele. Os processadores de dados são um componente do recurso de carregamento de dados assíncronos no D3DX11 que usa <a href="id3dx11threadpump.md"><strong>bombas de thread</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Em vez de usar essa função, recomendamos que você as use:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (Runtime), <strong>CreateXXXTextureFromFile</strong> (em que xxx é DDS ou WIC)</li>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (ferramentas), <strong>LoadFromXXXFile</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e, em seguida, <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Criar um sombreador – modo de exibição de recursos de um arquivo.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Em vez de usar essa função, recomendamos que você as use:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (Runtime), <strong>CreateXXXTextureFromMemory</strong> (em que xxx é DDS ou WIC)</li>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (ferramentas), <strong>LoadFromXXXMemory</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e, em seguida, <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Criar um sombreador – modo de exibição de recursos de um arquivo na memória.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Em vez de usar essa função, recomendamos que você use <a href="/windows/desktop/menurc/resources-functions">funções de recurso</a>e, em seguida, estas:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (Runtime), <strong>CreateXXXTextureFromMemory</strong> (em que xxx é DDS ou WIC)</li>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (ferramentas), <strong>LoadFromXXXMemory</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e, em seguida, <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Criar um sombreador – modo de exibição de recursos de um recurso.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Em vez de usar essa função, recomendamos que você as use:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (Runtime), <strong>CreateXXXTextureFromFile</strong> (em que xxx é DDS ou WIC)</li>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (ferramentas), <strong>LoadFromXXXFile</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> Crie um recurso de textura a partir de um arquivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Em vez de usar essa função, recomendamos que você as use:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (Runtime), <strong>CreateXXXTextureFromMemory</strong> (em que xxx é DDS ou WIC)</li>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (ferramentas), <strong>LoadFromXXXMemory</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> Crie um recurso de textura a partir de um arquivo que reside na memória do sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Em vez de usar essa função, recomendamos que você use <a href="/windows/desktop/menurc/resources-functions">funções de recurso</a>e, em seguida, estas:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (Runtime), <strong>CreateXXXTextureFromMemory</strong> (em que xxx é DDS ou WIC)</li>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (ferramentas), <strong>LoadFromXXXMemory</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> Crie uma textura de outro recurso.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações.
</blockquote>
<br/> Criar uma bomba de thread.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GenerateMipMaps</strong> e <strong>GenerateMipMaps3D</strong>.
</blockquote>
<br/> Gera cadeia de mipmap usando um filtro de textura específico.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GetMetadataFromXXXFile</strong> (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).
</blockquote>
<br/> Recupera informações sobre um determinado arquivo de imagem.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GetMetadataFromXXXMemory</strong> (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).
</blockquote>
<br/> Obtenha informações sobre uma imagem já carregada na memória.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use <a href="/windows/desktop/menurc/resources-functions">funções de recurso</a>e, em seguida, use <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (Tools), <strong>LoadFromXXXMemory</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).
</blockquote>
<br/> Recupera informações sobre uma determinada imagem em um recurso.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>redimensione</strong>, <strong>converta</strong>, <strong>compacte</strong>, <strong>Descompacte</strong>e/ou <strong>CopyRectangle</strong>.
</blockquote>
<br/> Carregar uma textura de uma textura.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use a API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .
</blockquote>
<br/> Crie um sombreador de um arquivo sem compilá-lo.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use a API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .
</blockquote>
<br/> Crie um sombreador da memória sem compilá-lo.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use a API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .
</blockquote>
<br/> Crie um sombreador de um recurso sem compilá-lo.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> , <strong>SaveToXXXFile</strong> (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos). Para o cenário simplificado de criação de uma captura de tela de uma textura de destino de renderização, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> , <strong>SaveDDSTextureToFile</strong> ou <strong>SaveWICTextureToFile</strong>.
</blockquote>
<br/> Salvar uma textura em um arquivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> , <strong>SaveToXXXMemory</strong> (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).
</blockquote>
<br/> Salve uma textura na memória.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">matemática de harmônicas esféricas</a> , <strong>SHProjectCubeMap</strong>.
</blockquote>
<br/> Projeta uma função representada em um mapa de cubo em harmônicas esféricas.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Em vez de usar essa função, recomendamos que você use o método <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>ID3D11DeviceContext:: clearstate</strong></a> .
</blockquote>
<br/> Remove todos os recursos do dispositivo definindo seus ponteiros como <strong>NULL</strong>. Isso deve ser chamado durante o desligamento do seu aplicativo. Ele ajuda a garantir que, quando um estiver liberando todos os seus recursos, nenhum deles esteja associado ao dispositivo.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 


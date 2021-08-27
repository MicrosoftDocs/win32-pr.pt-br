---
title: 'Interfaces de sombreador (elementos gráficos do Direct3D 11) '
description: Esta seção contém informações sobre as interfaces do sombreador.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- interfaces, sombreador Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fcecdff6f35b634ecbbeca0b85bc5ba42fd1e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479452"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a>Interfaces de sombreador (elementos gráficos do Direct3D 11) 

Esta seção contém informações sobre as interfaces do sombreador.

Cada uma dessas interfaces de sombreador gerencia um sombreador compilado. A interface é criada quando um sombreador é compilado e, em seguida, é passada para várias APIs que precisam de acesso a um sombreador compilado; por exemplo, ao vincular um sombreador a um estágio de pipeline ou obter uma assinatura de sombreador.


## <a name="in-this-section"></a>Nesta seção




| Tópico | Descrição | 
|-------|-------------|
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a><br /> | Essa interface encapsula uma classe HLSL.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a><br /> | Essa interface encapsula uma vinculação dinâmica HLSL.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a><br /> | Uma interface de sombreador de computação gerencia um programa executável (um sombreador de computação) que controla o estágio do sombreador de computação.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a><br /> | Uma interface de sombreador de domínio gerencia um programa executável (um sombreador de domínio) que controla o estágio do sombreador de domínio.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a><br /> | Uma interface de grafo de vinculação de função é usada para construir sombreadores que consistem em uma sequência de chamadas de função pré-compiladas que passam valores entre si. <br /><blockquote>[!Note]<br />Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de operação.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a><br /> | Uma interface de reflexão de função acessa informações de função. <br /><blockquote>[!Note]<br />Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de operação.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a><br /> | Uma interface function-parameter-reflection acessa informações de parâmetro de função. <br /><blockquote>[!Note]<br />Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de operação.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a><br /> | Uma interface de sombreador de geometria gerencia um programa executável (um sombreador de geometria) que controla o estágio de sombreador de geometria.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a><br /> | Uma interface de sombreador de chassi gerencia um programa executável (um sombreador de chassi) que controla o estágio do sombreador de chassi.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a><br /> | Uma interface de reflexão de biblioteca acessa informações da biblioteca. <br /><blockquote>[!Note]<br />Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de operação.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a><br /> | Uma interface do vinculador é usada para vincular um módulo de sombreador. <br /><blockquote>[!Note]<br />Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de operação.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a><br /> | Uma interface de nó de vinculação é usada para vinculação de sombreador. <br /><blockquote>[!Note]<br />Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de operação.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a><br /> | Uma interface de módulo cria uma instância de um módulo que é usada para a reabinagem de recursos. <br /><blockquote>[!Note]<br />Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de operação.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a><br /> | Uma interface de instância de módulo é usada para a reabinagem de recursos. <br /><blockquote>[!Note]<br />Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de operação.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a><br /> | Uma interface de sombreador de pixel gerencia um programa executável (um sombreador de pixel) que controla o estágio do sombreador de pixel.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a><br /> | Uma interface de reflexão de sombreador acessa informações de sombreador.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a><br /> | Essa interface de reflexão de sombreador fornece acesso a um buffer constante.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a><br /> | Essa interface sombreador-reflexão fornece acesso ao tipo de variável.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a><br /> | Essa interface de reflexão de sombreador fornece acesso a uma variável.<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a><br /> | Uma interface <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> implementa métodos para obter rastreamentos de execuções de sombreador.<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a><br /> | Uma interface <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> implementa um método para gerar objetos de informações de rastreamento do sombreador.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a><br /> | Uma interface de sombreador de vértice gerencia um programa executável (um sombreador de vértice) que controla o estágio de sombreador de vértice.<br /> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do sombreador](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 


---
title: Funções de compilador (referência de HLSL)
description: Esta seção contém informações sobre as seguintes funções do compilador do Direct3D HLSL
ms.assetid: aacc5207-3ec8-4031-b5c9-f7c0fb7b7095
keywords:
- funções, compilador
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 43d9bf2feb572d7b410d702dbc456af7c18be0ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465803"
---
# <a name="compiler-functions-hlsl-reference"></a>Funções de compilador (referência de HLSL)

Esta seção contém informações sobre as seguintes funções do compilador do Direct3D HLSL:

## <a name="in-this-section"></a>Nesta seção




| Tópico | Descrição | 
|-------|-------------|
| <a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a><br /> | Obtém um ponteiro para uma interface de reflexão.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a><br /> | Compile o código de HLSL ou um arquivo de efeito no código de bytes para um determinado destino.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a><br /> | Compila o código de HLSL (linguagem de sombreamento de alto nível) da Microsoft em bytes de um determinado destino.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a><br /> | <blockquote>[!Note]<br />você pode usar essa API para desenvolver seus aplicativos da Windows store, mas não pode usá-los em aplicativos que você envia para o repositório de Windows. Consulte a seção "compilando sombreadores para UWP", em comentários para <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</blockquote><br /> Compila o código de HLSL em bytes para um determinado destino.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a><br /> | <blockquote>[!Note]<br />você pode usar essa API para desenvolver seus aplicativos da Windows store, mas não pode usá-los em aplicativos que você envia para o repositório de Windows.</blockquote><br /> Compacta um conjunto de sombreadores em uma forma mais compacta. <br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a><br /> | Cria um buffer.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a><br /> | Cria uma interface de grafo de vinculação de função. <br /><blockquote>[!Note]<br />Essa função faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a><br /> | Cria uma interface de vinculador. <br /><blockquote>[!Note]<br />Essa função faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a><br /> | <blockquote>[!Note]<br />você pode usar essa API para desenvolver seus aplicativos da Windows store, mas não pode usá-los em aplicativos que você envia para o repositório de Windows.</blockquote><br /> Descompacta um ou mais sombreadores de um conjunto compactado. <br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a><br /> | Desmonta o código HLSL compilado.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a><br /> | Desmonta o código HLSL compilado de um efeito de Direct3D10.<br /> | 
| <a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a><br /> | Desmonta uma seção do código HLSL compilado que é especificada pelas etapas de rastreamento do sombreador.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a><br /> | Desmonta uma região específica do código HLSL compilado.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a><br /> | Recupera uma parte específica de um resultado de compilação.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a><br /> | <blockquote>[!Note]<br />você pode usar essa API para desenvolver seus aplicativos da Windows store, mas não pode usá-los em aplicativos que você envia para o repositório de Windows.</blockquote><br /> Obtém informações de depuração do sombreador.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a><br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> pode ser alterado ou indisponível para versões após Windows 8.1. Em vez disso, use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> com o valor <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> .</blockquote><br /> Obtém as assinaturas de entrada e saída de um resultado de compilação.<br /> | 
| [<strong>D3DGetInputSignatureBlob</strong>](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)<br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> pode ser alterado ou indisponível para versões após Windows 8.1. Em vez disso, use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> com o valor <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> .</blockquote><br /> Obtém a assinatura de entrada de um resultado de compilação.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a><br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> pode ser alterado ou indisponível para versões após Windows 8.1. Em vez disso, use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> com o valor <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> .</blockquote><br /> Obtém a assinatura de saída de um resultado de compilação.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a><br /> | Recupera os deslocamentos de byte para obter instruções em uma seção de código de sombreador.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a><br /> | Cria uma interface de módulo do sombreador a partir dos dados de origem do módulo do sombreador. <br /><blockquote>[!Note]<br />Essa função faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a><br /> | Pré-processa o código HLSL não compilado.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a><br /> | <blockquote>[!Note]<br />você pode usar essa API para desenvolver seus aplicativos da Windows store, mas não pode usá-los em aplicativos que você envia para o repositório de Windows.</blockquote><br /> Lê um arquivo que está no disco na memória.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a><br /> | Obtém um ponteiro para uma interface de reflexão.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a><br /> | Cria uma interface de reflexão de biblioteca a partir de dados de origem que contém uma biblioteca HLSL de funções. <br /><blockquote>[!Note]<br />Essa função faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a><br /> | Define informações em um resultado de compilação.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a><br /> | Remove BLOBs indesejados de um resultado de compilação.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a><br /> | <blockquote>[!Note]<br />você pode usar essa API para desenvolver seus aplicativos da Windows store, mas não pode usá-los em aplicativos que você envia para o repositório de Windows.</blockquote><br /> Grava um blob de memória em um arquivo no disco.<br /> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de D3DCompiler](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>


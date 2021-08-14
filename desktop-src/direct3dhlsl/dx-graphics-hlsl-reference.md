---
title: Referência para HLSL
description: A documentação de referência do HLSL especifica as características da linguagem. Ele é dividido em várias seções.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 425dc1d56801bbbd6b73429d8d17024a78dffe47a045ec6b34d5cd45b752bcca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513837"
---
# <a name="reference-for-hlsl"></a>Referência para HLSL

A documentação de referência do HLSL especifica as características da linguagem. Ele é dividido em várias seções.

-   [Sintaxe de linguagem (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) -os sombreadores de programação no HLSL exigem que você compreenda a sintaxe da linguagem, ou seja, como você escreve o código HLSL. Isso inclui código para declarar e inicializar variáveis, gravar funções de sombreador definidas pelo usuário e adicionar instruções de controle de fluxo para tornar suas funções mais poderosas.
-   [Modelos de sombreador vs. perfis de sombreador](dx-graphics-hlsl-models.md) – o compilador HLSL implementa regras e restrições com base em modelos de sombreador. O código em cada sombreador de vértice, o sombreador de geometria (se você estiver usando o Direct3D 10) e o sombreador de pixel são validados em relação a um modelo de sombreador que você fornece no momento da compilação.
-   [**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) -HLSL tem muitas funções intrínsecas. Eles são implementados e testados para que você possa usá-los sabendo que eles já estão depurados e têm um bom desempenho. Se você optar por escrever suas próprias funções, consulte a seção sintaxe de linguagem para gravar funções definidas pelo usuário.
-   [Referência de sombreador ASM](dx9-graphics-reference-asm.md) -instruções de assembly que você pode usar para programar e depurar sombreadores.
-   [Referência de D3DCompiler](dx-graphics-d3dcompiler-reference.md) – compila a fonte HLSL bruta.
-   [Referência de conversão de formato embutido](inline-format-conversion-reference.md) -o \_ arquivo D3DX DXGIFormatConvert. inl contém funções de conversão de formato embutido que você pode usar no sombreador de computação ou sombreador de pixel no hardware do Direct3D 11. Você pode usar essas funções em seu aplicativo para, simultaneamente, ler e gravar em uma textura. Ou seja, você pode executar a edição de imagem in-loco. Para usar essas funções de conversão de formato embutido, inclua o \_ arquivo D3DX DXGIFormatConvert. inl em seu aplicativo.
-   [Apêndice (DirectX HLSL)](dx-graphics-hlsl-appendix.md) -o apêndice está incluído para fins de integridade. Ele inclui uma listagem das palavras-chave e das senhas reservadas; essas palavras não podem ser usadas como identificadores em seus programas. Ele também inclui uma lista da gramática de idioma para referência.
-   [**Erros e avisos do HLSL**](hlsl-errors-and-warnings.md) -fornece códigos de erro e de aviso que um sombreador pode retornar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[HLSL](dx-graphics-hlsl.md)
</dt> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 





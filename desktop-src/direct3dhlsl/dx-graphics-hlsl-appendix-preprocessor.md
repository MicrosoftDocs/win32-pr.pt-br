---
title: Diretivas de pré-processador (HLSL)
description: As diretivas de pré-processador, como \ definir e \ ifdef, normalmente são usadas para facilitar a alteração e a facilidade dos programas de origem em ambientes de execução diferentes.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f2d9e51926d2a1b7bf374653becec4fe3de3daa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644082"
---
# <a name="preprocessor-directives-hlsl"></a>Diretivas de pré-processador (HLSL)

As diretivas de pré-processador, como [ \# definir](dx-graphics-hlsl-appendix-pre-define.md) e [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), normalmente são usadas para tornar os programas de origem fáceis de alterar e fáceis de Compilar em ambientes de execução diferentes. As políticas no arquivo de origem mandam o pré-processador realizar ações específicas. Por exemplo, o pré-processador pode substituir tokens no texto, inserir o conteúdo de outros arquivos no arquivo de origem ou suprimir a compilação de parte do arquivo removendo seções de texto. As linhas do pré-processador são reconhecidas e executadas antes de expansão macro. Portanto, se uma macro se expandir até algo que se pareça com um comando do pré-processador, esse comando não será reconhecido pelo pré-processador.

As instruções do pré-processador usam o mesmo conjunto de caracteres das instruções de arquivo de origem, com exceção das sequências de escape, que não têm suporte. O conjunto de caracteres usado em instruções do pré-processador é igual ao conjunto de caracteres de execução. O pré-processador também reconhece valores negativos de caracteres.

O pré-processador HLSL reconhece as seguintes diretivas:

-   [\#definir](dx-graphics-hlsl-appendix-pre-define.md)
-   [\#elif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#else](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#endif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#ao](dx-graphics-hlsl-appendix-pre-error.md)
-   [\#que](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#ifndef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#incluir](dx-graphics-hlsl-appendix-pre-include.md)
-   [\#descritos](dx-graphics-hlsl-appendix-pre-line.md)
-   [\#pragma](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [\#undef](dx-graphics-hlsl-appendix-pre-undef.md)

O sinal numérico ( \# ) deve ser o primeiro caractere que não seja de espaço em branco na linha que contém a diretiva; caracteres de espaço em branco podem aparecer entre o sinal numérico e a primeira letra da diretiva. Algumas políticas incluem argumentos ou valores. Qualquer texto que segue uma diretiva (exceto um argumento ou valor que faça parte da diretiva) deve ser precedido pelo delimitador de comentário de linha única (//) ou colocado em delimitadores de comentário (/ \* \* /). As linhas que contêm diretivas de pré-processador podem ser continuadas imediatamente antes do marcador de fim de linha com uma barra invertida ( \) .

As políticas do pré-processador podem aparecer em qualquer lugar do arquivo de origem, mas se aplicam somente ao restante dele.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Apêndice (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 





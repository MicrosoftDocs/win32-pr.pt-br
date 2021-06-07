---
title: Diretivas de pré-processador (HLSL)
description: Diretivas de pré-processador, como \ define e \ ifdef, normalmente são usadas para tornar os programas de origem fáceis de alterar e fáceis de compilar em ambientes de execução diferentes.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8efdd996ddeb58c09d1c8250f174c21bb939f082
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386825"
---
# <a name="preprocessor-directives-hlsl"></a>Diretivas de pré-processador (HLSL)

Diretivas de pré-processador, como [ \# define](dx-graphics-hlsl-appendix-pre-define.md) e [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), normalmente são usadas para facilitar a alteração dos programas de origem e fácil de compilar em ambientes de execução diferentes. As políticas no arquivo de origem mandam o pré-processador realizar ações específicas. Por exemplo, o pré-processador pode substituir tokens no texto, inserir o conteúdo de outros arquivos no arquivo de origem ou suprimir a compilação de parte do arquivo removendo seções de texto. As linhas do pré-processador são reconhecidas e executadas antes de expansão macro. Portanto, se uma macro se expandir até algo que se pareça com um comando do pré-processador, esse comando não será reconhecido pelo pré-processador.

As instruções do pré-processador usam o mesmo conjunto de caracteres das instruções de arquivo de origem, com exceção das sequências de escape, que não têm suporte. O conjunto de caracteres usado em instruções do pré-processador é igual ao conjunto de caracteres de execução. O pré-processador também reconhece valores negativos de caracteres.

O pré-processador HLSL reconhece as seguintes diretivas:

-   [\#Definir](dx-graphics-hlsl-appendix-pre-define.md)
-   [\#elif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#else](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#endif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#Erro](dx-graphics-hlsl-appendix-pre-error.md)
-   [\#Se](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#Ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#Ifndef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#Incluem](dx-graphics-hlsl-appendix-pre-include.md)
-   [\#line](dx-graphics-hlsl-appendix-pre-line.md)
-   [\#Pragma](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [\#undef](dx-graphics-hlsl-appendix-pre-undef.md)

O sinal de número ( ) deve ser o primeiro caractere de espaço não branco na linha que contém a diretiva ; os caracteres de espaço em branco podem aparecer entre o sinal de número e a primeira letra da \# diretiva. Algumas políticas incluem argumentos ou valores. Qualquer texto que siga uma diretiva (exceto um argumento ou valor que faz parte da diretiva) deve ser precedido pelo delimitador de comentário de linha única (//) ou incluído nos delimitadores de comentário (/ \* \* /). As linhas que contêm diretivas de pré-processador podem ser continuadas precedendo imediatamente o marcador de fim de linha com uma faixa invertida ( \\ ).

As políticas do pré-processador podem aparecer em qualquer lugar do arquivo de origem, mas se aplicam somente ao restante dele.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Apêndice (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




